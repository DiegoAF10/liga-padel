# liga-padel
Sistema de gestión de liga de pádel con ranking individual
markdown# Liga de Pádel - Sistema de Ranking Individual

## 📖 Descripción del Proyecto

Sistema web completo para gestionar ligas de pádel con ranking individual de jugadores. 
Permite crear torneos, gestionar partidos, calcular rankings automáticamente y exportar datos.

**Características principales:**
- Ranking individual por jugador (no por pareja)
- Sistema de torneos flexible (Ligas, Copas, Especiales)
- Cálculo automático de puntos con decaimiento temporal
- Gestión de partidos con validación de marcadores de tenis
- Sistema de walkovers y penalizaciones
- Almacenamiento local en navegador (LocalStorage)

---

## ✅ FUNCIONALIDADES IMPLEMENTADAS (Módulos 1-5 + Datos)

### Módulo 1: Estructura Base
- ✅ Header con logo y selector de temporada
- ✅ Navegación por tabs (9 secciones)
- ✅ Sistema de temas (oscuro/claro) con toggle manual
- ✅ LocalStorage funcional para persistencia de datos
- ✅ Dashboard con estadísticas principales
- ✅ 16 jugadores pre-cargados

### Módulo 2: Gestión de Jugadores
- ✅ CRUD completo (Crear, Leer, Actualizar, Eliminar)
- ✅ Modal profesional para agregar/editar
- ✅ Validación de nombres duplicados
- ✅ Activar/Desactivar jugadores
- ✅ Búsqueda en tiempo real
- ✅ Notificaciones de éxito/error

### Módulo 3: Sistema de Torneos
- ✅ Wizard de 5 pasos para crear torneos
- ✅ Tipos: Liga Regular (1.0x), Copa Express (0.7x), Especial (1.5x)
- ✅ Opción de 1 o 2 vueltas para ligas
- ✅ Soporte para 4, 6, 8, 10, 12 parejas
- ✅ Sistema de bombos (seeding) para copas por ranking
- ✅ Formación de parejas manual
- ✅ Botón "Seleccionar Todos" (jugadores)
- ✅ Botón "Repetir Parejas del Último Torneo"
- ✅ Grupos automáticos para copas según bombos

### Módulo 4: Cálculo de Ranking Individual
- ✅ Fórmula completa implementada: (Base × Peso × Multiplicador) + Victorias + Bonos - Penalizaciones
- ✅ Puntos base dinámicos según número de parejas
- ✅ Multiplicador de rendimiento: 1.0 + (Victorias/Total × 0.3)
- ✅ Sistema de decaimiento temporal (6, 12, 18, 24, 30 meses)
- ✅ Torneos especiales sin decaimiento
- ✅ Badges por categoría: 👑💎🔴🟠🟡🟢🔵
- ✅ Ranking de parejas (informativo, por promedio)
- ✅ Top 5 en dashboard
- ✅ Botón "Recalcular Rankings"

### Módulo 5: Gestión de Partidos y Calendario
- ✅ Generación automática de fixtures con circle rotation
- ✅ Distribución por rondas (cada pareja juega 1 vez por ronda)
- ✅ Compatible con fixtures antiguos (week/round)
- ✅ Modal para registrar resultados set por set
- ✅ Validación completa de marcadores de tenis (6-4, 7-5, 7-6, etc.)
- ✅ Opción de partido incompleto por tiempo
- ✅ Sistema de walkovers con razones:
  - Atraso 5-14 min: -2 puntos
  - Atraso 15+ min: -3 puntos + W.O. 6-0, 6-0
  - No se presentó: -3 puntos + W.O.
  - Lesión
  - Otra razón (personalizable)
- ✅ Actualización automática de estadísticas de parejas
- ✅ Vista de calendario por rondas
- ✅ Progreso por ronda (X/Y completados)
- ✅ Estados visuales: Pendiente, Jugado (verde), W.O. (naranja)

### Sección de Datos (Gestión)
- ✅ Dashboard de estado del sistema
- ✅ Exportar backup completo (JSON)
- ✅ Importar backup desde archivo
- ✅ Borrar datos de temporada actual
- ✅ Borrar todos los datos (todas las temporadas)
- ✅ Limpiar LocalStorage completo
- ✅ Confirmaciones fuertes para acciones destructivas

---

## 🔧 ESTRUCTURA DEL CÓDIGO

### HTML
- Single-page application con secciones ocultas/visibles
- Navegación por tabs
- 3 modales: Jugadores, Torneo Wizard, Resultado de Partido

### CSS (Inline)
- Variables CSS para temas
- Sistema de grid responsivo
- Componentes: cards, botones, modales, badges, alertas
- Animaciones suaves (fadeIn, slideIn)
- Soporte para modo oscuro

### JavaScript (Vanilla)
**Estructura de datos:**
```javascript
appData = {
  version: '1.0',
  currentSeason: '2025',
  seasons: {
    '2025': {
      players: [...],  // Array de jugadores
      tournaments: [...] // Array de torneos
    }
  }
}
Funciones principales:

loadData() / saveData() - LocalStorage
showSection() - Navegación
renderDashboard(), renderPlayersTable(), etc. - Renderizado
generateLeagueFixture() / generateCupFixture() - Generación de partidos
calculatePlayerRanking() - Cálculo de puntos
saveMatchResult() - Registro de resultados


🎨 DECISIONES DE DISEÑO
Colores

Primary: #2E7D32 (verde pádel)
Secondary: #FF6F00 (naranja)
Accent: #FFC107 (amarillo)
Success: #4CAF50
Warning: #FF9800
Error: #F44336

Estilo

Profesional/Deportivo mix
Cards con sombras sutiles
Badges para estados
Gradientes en stat cards
Modo oscuro completo

Lógica de Rankings

Individual (no por pareja) para permitir flexibilidad
Peso por tipo de torneo (Liga 1.0x, Copa 0.7x, Especial 1.5x)
Decaimiento temporal para mantener ranking dinámico
Bonificaciones por versatilidad (ganar con diferentes parejas)

Fixtures

Sistema de rondas (no semanas) por simplicidad
Circle rotation algorithm para distribución balanceada
Compatible con datos antiguos (week vs round)


📝 FUNCIONALIDADES PENDIENTES
Módulo 6: Tabla de Posiciones en Tiempo Real

Ordenamiento automático (Puntos → Diff Sets → Diff Games → H2H)
Código de colores para clasificación a playoffs
Tabla por grupo para copas
Actualización automática post-partido

Módulo 7: Sistema de Playoffs Automático

Generación automática al finalizar fase regular
Bracket visual
Ronda preliminar (3º vs 6º, 4º vs 5º)
Semifinales y final
Partido por 3er lugar

Módulo 8: Exportación Avanzada

PDF de tabla de posiciones
CSV de estadísticas
Calendario exportable a WhatsApp por pareja
Compartir resultados (imagen)

Módulo 9: Visualización de Penalizaciones

Log completo de penalizaciones
Filtros por jugador/torneo
Historial de walkovers

Módulo 10: Estadísticas Avanzadas

Gráfico de evolución de ranking
Distribución de puntos por torneo (pie chart)
Matriz H2H entre parejas
Comparación entre temporadas

Módulo 11: Criterios del Ranking (Documentación)

Explicación detallada de fórmulas
Ejemplos de cálculo
FAQs

Refinamiento UI/UX

Pulir modo oscuro
Animaciones adicionales
Responsive para móviles
Loading states


⚠️ DETALLES TÉCNICOS IMPORTANTES
LocalStorage

Key: padelLeagueData
Límite: ~5-10MB
Formato: JSON string
Compatibilidad: Chrome/Edge/Firefox/Safari

Validación de Sets
Marcadores válidos de tenis:

6-0, 6-1, 6-2, 6-3, 6-4
7-5, 5-7
7-6, 6-7 (tie-break)
Si "incompleto por tiempo": permite cualquier marcador

Circle Rotation Algorithm
Para N parejas:

Genera N-1 rondas
Cada ronda: N/2 partidos simultáneos
Rotación: primer elemento fijo, demás rotan
Resultado: distribución perfectamente balanceada

Compatibilidad Fixtures
El código lee ambos:
javascriptconst roundNum = match.round || match.week || 1;
Así funciona con datos antiguos y nuevos.

🐛 BUGS CONOCIDOS / SOLUCIONES
"Ronda undefined"
Problema: Matches antiguos tienen campo week en lugar de round
Solución: Código actualizado lee ambos campos
Fix: const roundNum = match.round || match.week || 1;
Fixtures mal distribuidos
Problema: Algoritmo anterior no balanceaba bien
Solución: Implementado circle rotation correcto
Status: ✅ Resuelto

📚 REFERENCIAS
Algoritmos Usados

Circle Rotation (Round-Robin): Para generación de fixtures
Berger Tables: Base teórica de la rotación
Seeding (Bombos): Clasificación por ranking para sorteo justo

Inspiración de Diseño

ATP/WTA Rankings (tenis profesional)
ESPN/DAZN dashboards deportivos
Material Design (Google)


🚀 PRÓXIMOS PASOS RECOMENDADOS

Implementar Módulo 6 (Tabla de Posiciones)
Implementar Módulo 7 (Playoffs)
Testear con datos reales de torneo completo
Implementar exportación a WhatsApp
Refinamiento de UI/UX
Testing en diferentes navegadores
Documentación de usuario final


Última actualización: 30 de Septiembre, 2025
Versión: 1.0 (Módulos 1-5 completados)
Estado: En desarrollo activo

---

## 2. ARCHIVO HTML COMPLETO ACTUALIZADO

El código está en el artifact actual. Para descargarlo:

**Opción A - Desde el navegador:**
1. Copia TODO el contenido del artifact
2. Pega en un archivo nuevo llamado `liga-padel.html`
3. Guárdalo

**Opción B - Usando la consola:**
```javascript
// Ejecuta esto en la consola del navegador
const html = document.documentElement.outerHTML;
const blob = new Blob([html], { type: 'text/html' });
const url = URL.createObjectURL(blob);
const a = document.createElement('a');
a.href = url;
a.download = 'liga-padel.html';
a.click();
