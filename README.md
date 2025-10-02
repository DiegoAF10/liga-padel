# liga-padel
Sistema de gestión de liga de pádel con ranking individual
# 🎾 Sistema de Gestión de Liga de Pádel

> Sistema completo para gestionar ligas de pádel con ranking individual, torneos, playoffs y estadísticas detalladas.

![Version](https://img.shields.io/badge/version-2.0-green)
![Status](https://img.shields.io/badge/status-completo-success)
![License](https://img.shields.io/badge/license-MIT-blue)

---

## 📋 Tabla de Contenidos

- [Características Principales](#-características-principales)
- [Módulos Implementados](#-módulos-implementados)
- [Instalación](#-instalación)
- [Guía de Uso](#-guía-de-uso)
- [Sistema de Ranking](#-sistema-de-ranking)
- [Tipos de Torneos](#-tipos-de-torneos)
- [Tecnologías](#-tecnologías)
- [Roadmap Futuro](#-roadmap-futuro)
- [FAQ](#-faq)

---

## ✨ Características Principales

### 🎯 Gestión Integral
- ✅ **16 jugadores precargados** con estado activo/inactivo
- ✅ **CRUD completo** de jugadores (crear, editar, eliminar)
- ✅ **Validación de duplicados** y campos requeridos
- ✅ **Búsqueda en tiempo real** por nombre

### 🏆 Sistema de Torneos
- ✅ **3 tipos de torneos**: Liga Regular, Copa Express, Campeonato Especial
- ✅ **Wizard de 5 pasos** para creación guiada
- ✅ **Sorteo por bombos** (basado en ranking)
- ✅ **Fixtures automáticos** con algoritmo round-robin
- ✅ **1 o 2 vueltas** (ida y vuelta)
- ✅ **Validaciones inteligentes**: duplicados, torneos activos, fechas

### 📊 Calendario y Resultados
- ✅ **Vista por rondas/semanas** con progreso
- ✅ **Registro de resultados** set por set
- ✅ **Edición de resultados** con recalculo automático
- ✅ **Validación de marcadores** de tenis (6-0, 7-5, 7-6, etc.)
- ✅ **Walkovers** con penalizaciones automáticas
- ✅ **Partidos incompletos** por tiempo

### 🥇 Sistema de Playoffs (NUEVO - Módulo 7)
- ✅ **Generación automática** al completar grupos
- ✅ **Bracket visual** interactivo
- ✅ **Semifinales + Final + 3er Lugar**
- ✅ **Clasificación automática** (1º y 2º de cada grupo)
- ✅ **Actualización del bracket** en tiempo real
- ✅ **Asignación de posiciones** finales (1º a 8º)
- ✅ **Finalización automática** del torneo

### 📈 Ranking Individual
- ✅ **Sistema de puntos** multinivel
- ✅ **Decay temporal** (decaimiento por antigüedad)
- ✅ **Multiplicadores** por desempeño
- ✅ **Badges de rango**: 👑 💎 🔴 🟠 🟡 🟢 🔵
- ✅ **Desglose detallado** por torneo (click en jugador)
- ✅ **Filtros avanzados**: búsqueda, estado, puntos

### 📋 Tablas de Posiciones
- ✅ **Estadísticas completas**: PJ, PG, PP, Pts, SF, SC, GF, GC
- ✅ **Diferencia de sets y games**
- ✅ **Ordenamiento por criterios** de desempate
- ✅ **Indicadores de clasificación** a playoffs
- ✅ **Vista por grupos** (en Copas)

### 💾 Gestión de Datos
- ✅ **LocalStorage** para persistencia
- ✅ **Exportar backup** (JSON)
- ✅ **Importar backup** con validación
- ✅ **Borrado selectivo** (temporada o todo)
- ✅ **Dashboard de estadísticas** del sistema

### 🎨 Interfaz de Usuario
- ✅ **Modo oscuro/claro** persistente
- ✅ **Responsive design** (móvil, tablet, desktop)
- ✅ **Navegación por tabs** intuitiva
- ✅ **Notificaciones toast** elegantes
- ✅ **Loading states** con spinners
- ✅ **Modales y wizards** guiados
- ✅ **Validaciones visuales** en tiempo real

---

## 📦 Módulos Implementados

### ✅ Módulo 1: Gestión de Jugadores
- CRUD completo de jugadores
- Estado activo/inactivo
- Búsqueda y filtros
- 16 jugadores precargados

### ✅ Módulo 2: Sistema de Torneos
- Wizard de creación (5 pasos)
- 3 tipos de torneos
- Configuración de parejas
- Validaciones completas

### ✅ Módulo 3: Generación de Fixtures
- Algoritmo round-robin
- Sorteo por bombos (copas)
- Grupos automáticos
- 1 o 2 vueltas

### ✅ Módulo 4: Calendario de Partidos
- Vista por rondas
- Progreso visual
- Estados de partidos
- Navegación por torneo

### ✅ Módulo 5: Registro de Resultados
- Validación de marcadores
- Walkovers con penalizaciones
- Partidos incompletos
- **NUEVO**: Edición de resultados

### ✅ Módulo 6: Sistema de Ranking
- Cálculo multinivel de puntos
- Decay temporal
- Desglose por torneo
- **NUEVO**: Filtros avanzados

### ✅ Módulo 7: Playoffs (NUEVO)
- Generación automática
- Bracket visual
- Semifinales + Final + 3er Lugar
- Actualización en tiempo real
- Finalización de torneos

---

## 🚀 Instalación

### Opción 1: Uso Directo (Recomendado)
```bash
# 1. Descarga el archivo
wget [URL del archivo HTML]

# 2. Abre en tu navegador
# Doble clic en liga-padel-completo.html
```

### Opción 2: Servidor Local
```bash
# Con Python
python -m http.server 8000

# Con Node.js
npx http-server

# Luego abre: http://localhost:8000
```

### Requisitos
- ✅ Navegador moderno (Chrome, Firefox, Safari, Edge)
- ✅ JavaScript habilitado
- ✅ LocalStorage disponible
- ❌ No requiere servidor
- ❌ No requiere instalación
- ❌ No requiere dependencias

---

## 📖 Guía de Uso

### 1️⃣ Gestión de Jugadores

#### Agregar Jugador
1. Ve a **"👥 Jugadores"**
2. Click en **"➕ Agregar Jugador"**
3. Ingresa el nombre
4. Click en **"Guardar"**

#### Editar/Eliminar
- **Editar**: Click en botón "✏️ Editar"
- **Activar/Desactivar**: Click en botón de estado
- **Eliminar**: Click en "🗑️ Eliminar" (confirmación requerida)

### 2️⃣ Crear Torneo

#### Paso 1: Información Básica
- Nombre del torneo
- Fecha de inicio

#### Paso 2: Tipo de Torneo
- **Liga Regular** (1.0x): Todos contra todos + playoffs
- **Copa Express** (0.7x): Grupos + eliminación directa
- **Campeonato Especial** (1.5x): Mayor prestigio, sin decay
- Selecciona **1 o 2 vueltas**

#### Paso 3: Cantidad de Parejas
- 4 parejas (8 jugadores)
- 6 parejas (12 jugadores)
- 8 parejas (16 jugadores)
- 10 parejas (20 jugadores)

#### Paso 4: Seleccionar Jugadores
- Selecciona exactamente N jugadores (según parejas)
- Usa "✓ Seleccionar Todos" para auto-selección

#### Paso 5: Formar Parejas
- Asigna jugadores a cada pareja manualmente
- O usa "🔄 Repetir Parejas del Último Torneo"

### 3️⃣ Generar Fixture

1. Ve a **"📅 Calendario"**
2. Selecciona el torneo
3. Click en **"⚡ Generar Fixture"**
4. El sistema crea automáticamente todos los partidos

### 4️⃣ Registrar Resultados

#### Resultado Normal
1. Click en **"Registrar"** en un partido
2. Ingresa marcador set por set:
   - Set 1: Obligatorio
   - Set 2: Obligatorio
   - Set 3: Opcional
3. ✅ Validación automática de marcadores
4. Click en **"Guardar Resultado"**

#### Editar Resultado
1. Click en **"✏️ Editar"** en partido completado
2. Modifica los sets
3. El sistema recalcula automáticamente estadísticas

#### Walkover
1. Marca checkbox **"Walkover (W.O.)"**
2. Selecciona pareja ganadora
3. Selecciona razón:
   - Atraso 5-14 min (-2 pts)
   - Atraso 15+ min (-3 pts)
   - No se presentó (-3 pts)
   - Lesión (sin penalización)
   - Otra razón (personalizada)

### 5️⃣ Ver Posiciones

1. Ve a **"📋 Posiciones"**
2. Selecciona torneo
3. Visualiza tabla completa con:
   - Posiciones
   - Partidos jugados/ganados/perdidos
   - Puntos
   - Sets/Games a favor y en contra
   - Diferencias

### 6️⃣ Playoffs (Copas)

1. Completa **todos los partidos de grupos**
2. El sistema pregunta si quiere generar playoffs
3. Ve a **"🥇 Playoffs"** para ver bracket
4. Registra resultados de:
   - Semifinal 1 (1º Grupo A vs 2º Grupo B)
   - Semifinal 2 (1º Grupo B vs 2º Grupo A)
   - Partido 3er Lugar (perdedores de semis)
   - Final (ganadores de semis)
5. El torneo se completa automáticamente

### 7️⃣ Consultar Ranking

1. Ve a **"⭐ Ranking"**
2. Usa filtros:
   - 🔍 Buscar por nombre
   - Estado (activos/inactivos)
   - Rango de puntos
3. Click en un jugador para ver **desglose detallado**

### 8️⃣ Gestión de Datos

#### Exportar Backup
1. Ve a **"💾 Datos"**
2. Click en **"📥 Exportar Backup (JSON)"**
3. Guarda el archivo

#### Importar Backup
1. Click en **"📤 Importar Backup"**
2. Selecciona archivo `.json`
3. Confirma importación

---

## 🏅 Sistema de Ranking

### Cálculo de Puntos

El ranking individual se calcula con esta fórmula:

```
Puntos Totales = Σ [(Puntos Base × Peso × Multiplicador × Decay) + Puntos por Victoria]
```

### Componentes

#### 1. Puntos Base (por posición final)
**Liga Regular (8 parejas)**
- 🥇 1º lugar: 1000 pts
- 🥈 2º lugar: 700 pts
- 🥉 3-4º lugar: 500 pts
- 5-6º lugar: 300 pts
- 7-8º lugar: 150 pts

**Copa Express (6+ parejas)**
- 🥇 1º lugar: 700 pts
- 🥈 2º lugar: 490 pts
- 🥉 3-4º lugar: 350 pts
- 5º+ lugar: 210 pts

#### 2. Peso del Torneo
- **Liga Regular**: 1.0x
- **Copa Express**: 0.7x
- **Campeonato Especial**: 1.5x

#### 3. Multiplicador por Desempeño
```
Multiplicador = 1.0 + (Victorias / Partidos Jugados × 0.3)
```
- 100% victorias: 1.3x
- 50% victorias: 1.15x
- 0% victorias: 1.0x

#### 4. Puntos por Victoria
- Partidos regulares: 30 pts
- Fase de grupos: 30 pts
- Preliminares: 50 pts
- Semifinales: 75 pts
- Final: 100 pts
- 3er lugar: 50 pts

#### 5. Decay Temporal
Solo para Ligas y Copas (Especiales no decaen):
- < 12 meses: 100%
- 12-18 meses: 75%
- 18-24 meses: 50%
- 24-30 meses: 25%
- > 30 meses: 0%

### Rangos y Badges
- 👑 **Élite**: 5000+ pts
- 💎 **Diamante**: 4000-4999 pts
- 🔴 **Platino**: 3000-3999 pts
- 🟠 **Oro**: 2000-2999 pts
- 🟡 **Plata**: 1000-1999 pts
- 🟢 **Bronce**: 500-999 pts
- 🔵 **Inicial**: 0-499 pts

### Ejemplo de Cálculo

**Jugador gana Liga Regular de 8 parejas en 1º lugar**
- Partidos: 14 jugados, 11 ganados, 3 perdidos

```
Puntos Base = 1000
Peso = 1.0
Multiplicador = 1.0 + (11/14 × 0.3) = 1.236
Decay = 1.0 (torneo reciente)
Puntos Victoria = 11 × 30 = 330

Puntos Posición = 1000 × 1.0 × 1.236 × 1.0 = 1,236
Puntos Totales = 1,236 + 330 = 1,566 puntos
```

---

## 🏆 Tipos de Torneos

### 🎯 Liga Regular (Peso: 1.0x)

**Características:**
- Fase regular: Todos contra todos
- 1 o 2 vueltas (ida y vuelta)
- Sistema de puntos: 3 pts victoria, 0 pts derrota
- Criterios de desempate:
  1. Puntos
  2. Diferencia de sets
  3. Diferencia de games
- **Playoffs**: Los mejores clasifican

**Ideal para:**
- Torneos largos y competitivos
- Determinar el mejor de forma justa
- Ligas mensuales o semestrales

### 🥤 Copa Express (Peso: 0.7x)

**Características:**
- Fase de grupos (2 grupos)
- Sorteo por bombos (ranking)
- Todos contra todos en cada grupo
- Clasifican: 1º y 2º de cada grupo
- **Playoffs automáticos**:
  - SF1: 1º Grupo A vs 2º Grupo B
  - SF2: 1º Grupo B vs 2º Grupo A
  - Final: Ganadores semis
  - 3er Lugar: Perdedores semis

**Ideal para:**
- Torneos rápidos (1-2 semanas)
- Eventos especiales
- Muchos participantes en poco tiempo

### ⭐ Campeonato Especial (Peso: 1.5x)

**Características:**
- Mismo formato que Liga Regular
- **Mayor prestigio**: 1.5x puntos
- **Sin decay temporal**: Puntos permanentes
- Otorga más puntos por victoria

**Ideal para:**
- Torneos anuales importantes
- Campeonatos de fin de año
- Eventos destacados

---

## 🛠 Tecnologías

### Frontend
- **HTML5**: Estructura semántica
- **CSS3**: Diseño moderno y responsive
  - Variables CSS para temas
  - Flexbox y Grid
  - Animaciones y transiciones
- **JavaScript Vanilla**: Lógica de negocio
  - ES6+ features
  - LocalStorage API
  - FileReader API

### Características Técnicas
- ✅ **100% cliente**: Sin backend necesario
- ✅ **SPA**: Single Page Application
- ✅ **Offline-first**: Funciona sin internet
- ✅ **Progressive**: Mejora según capacidades
- ✅ **Responsive**: Móvil, tablet, desktop

### Arquitectura de Datos
```javascript
{
  version: "2.0",
  currentSeason: "2025",
  seasons: {
    "2025": {
      players: [
        {
          id: "p1",
          name: "Nombre",
          rankingPoints: 0,
          tournaments: [],
          totalWins: 0,
          totalLosses: 0,
          titles: 0,
          runnerUps: 0,
          active: true,
          rankingBreakdown: []
        }
      ],
      tournaments: [
        {
          id: "t1",
          name: "Torneo",
          date: "2025-01-01",
          type: "league|cup|special",
          weight: 1.0,
          rounds: 1,
          status: "pending|active|completed",
          pairs: [],
          matches: [],
          groups: [],
          playoffs: null,
          penalties: []
        }
      ]
    }
  }
}
```

---

## 🗺 Roadmap Futuro

### 🔵 En Consideración

#### Funcionalidades
- [ ] Sistema de sanciones y fair play
- [ ] Historial completo de enfrentamientos
- [ ] Estadísticas avanzadas (racha, form)
- [ ] Predictor de resultados (ML)
- [ ] Chat/comentarios en partidos
- [ ] Notificaciones push
- [ ] Calendario Google integrado

#### Mejoras Técnicas
- [ ] Progressive Web App (PWA)
- [ ] Sincronización multi-dispositivo
- [ ] Base de datos remota (opcional)
- [ ] Exportar a PDF/Excel
- [ ] Compartir en redes sociales
- [ ] API REST para integraciones

#### Reportes
- [ ] Informe de temporada
- [ ] Top 10 estadísticas
- [ ] Gráficos de evolución
- [ ] Comparativa de jugadores
- [ ] MVP del torneo

---

## ❓ FAQ

### ¿Necesito instalar algo?
**No.** Solo necesitas un navegador web moderno. El sistema funciona 100% en el navegador sin necesidad de servidor.

### ¿Dónde se guardan los datos?
Los datos se almacenan en el **LocalStorage** de tu navegador. Es importante:
- ✅ Hacer backups regularmente
- ✅ No borrar caché del navegador
- ⚠️ Los datos son locales al dispositivo

### ¿Puedo usar esto en mi móvil?
**Sí.** El sistema es completamente responsive y funciona en móviles, tablets y escritorio.

### ¿Cómo hago backup?
1. Ve a "💾 Datos"
2. Click en "📥 Exportar Backup (JSON)"
3. Guarda el archivo en un lugar seguro
4. Para restaurar: "📤 Importar Backup"

### ¿Puedo tener múltiples temporadas?
Actualmente el sistema maneja la temporada 2025. En futuras versiones se podrá cambiar de temporada desde el selector.

### ¿Qué pasa si borro un torneo?
Al borrar un torneo:
- ✅ Se eliminan todos sus partidos
- ✅ Se recalculan los rankings
- ✅ Se actualizan las estadísticas de jugadores
- ⚠️ **No se puede deshacer** - Haz backup primero

### ¿Cómo funciona el sorteo por bombos?
En Copas Express:
1. Las parejas se ordenan por ranking promedio
2. Se distribuyen alternadamente en 2 grupos
3. Ejemplo con 8 parejas:
   - Grupo A: 1º, 4º, 5º, 8º
   - Grupo B: 2º, 3º, 6º, 7º

### ¿Puedo editar un resultado después de guardarlo?
**Sí.** Desde la versión 2.0:
1. Ve al partido completado
2. Click en "✏️ Editar"
3. Modifica los sets
4. El sistema recalcula todo automáticamente

### ¿Qué es el "DEMO" en torneos?
Es una función para completar automáticamente un torneo con resultados simulados. Útil para:
- ✅ Probar el sistema
- ✅ Ver cómo funciona el ranking
- ✅ Generar datos de ejemplo

### ¿Cómo se desempatan las posiciones?
Criterios en orden:
1. **Puntos** (3 por victoria)
2. **Diferencia de sets** (SF - SC)
3. **Diferencia de games** (GF - GC)
4. En caso de empate total: se mantiene el orden actual

---

## 📊 Estadísticas del Proyecto

- **Líneas de código**: ~3,500
- **Funciones**: ~50+
- **Módulos**: 7 completos
- **Tipos de torneos**: 3
- **Tiempo de desarrollo**: Modular e incremental
- **Testing**: Funcional completo
- **Browser support**: Chrome, Firefox, Safari, Edge

---

## 📝 Notas de Versión

### v2.0 (Actual)
- ✅ Módulo 7: Playoffs completo
- ✅ Edición de resultados
- ✅ Vista detallada de torneos
- ✅ Validaciones mejoradas
- ✅ Loading states
- ✅ Filtros en ranking
- ✅ Mejoras visuales

### v1.0
- ✅ Módulos 1-6 completos
- ✅ Sistema base funcional
- ✅ CRUD de jugadores y torneos
- ✅ Fixtures automáticos
- ✅ Ranking individual
- ✅ Posiciones y calendario

---

## 🤝 Contribuciones

Este es un proyecto personal, pero si tienes sugerencias:
1. Documenta la mejora propuesta
2. Explica el caso de uso
3. Si es técnica, incluye pseudocódigo

---

## 📄 Licencia

**MIT License** - Uso libre para proyectos personales y comerciales.

---

## 👨‍💻 Autor

Sistema desarrollado para gestión de ligas de pádel amateur/profesional.

**Contacto**: [Tu información de contacto]

---

## 🙏 Agradecimientos

- A la comunidad de pádel por el feedback
- A los testers por reportar bugs
- A los jugadores por usar el sistema

---

<div align="center">

**⭐ ¡Si te gusta el proyecto, dale una estrella! ⭐**

Made with ❤️ and 🎾

</div>
const blob = new Blob([html], { type: 'text/html' });
const url = URL.createObjectURL(blob);
const a = document.createElement('a');
a.href = url;
a.download = 'liga-padel.html';
a.click();
