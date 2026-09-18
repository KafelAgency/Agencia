# KAFEL Agency Admin Dashboard

Una plataforma de administración completa para gestionar vendedores, programadores, clientes y ventas de KAFEL Agency.

## 🚀 Características

### Dashboard Principal
- **Estadísticas en tiempo real**: Total de vendedores, programadores, clientes y ganancias del mes
- **Gráfico de ventas por categoría**: Visualización de ingresos por tipo de producto/servicio
- **Top 5 Vendedores**: Ranking de los mejores vendedores del mes
- **Resumen mensual**: Total de ventas, número de operaciones y promedio por venta

### Gestión de Vendedores
- **Lista de vendedores**: Con filtrado por nombre en tiempo real
- **Información detallada**: Datos personales y comisión de cada vendedor
- **Historial de ventas**: Seguimiento completo de todas las operaciones
- **Sistema de bonificación**: Indicador de bonos por referidos (5% por cada referencia)

### Gestión de Programadores
- **Similar a vendedores**: Tracking de proyectos realizados
- **Historial de proyectos**: Con fechas, montos y estado de cada proyecto
- **Comisiones**: Sistema de comisión por proyecto completado

### Registro de Ventas
- **Tabla completa de ventas**: Empresa, encargado, categoría, monto, estado y vendedor
- **Filtrado avanzado**: Por empresa, vendedor y estado de pago
- **Estados de pago**: Anticipo (40/50%), balance (50%), pago completo (100%)

### Gestión de Clientes
- **Registro de clientes**: Empresa, contacto, teléfono, redes sociales
- **Tipos de cliente**: Premium, normal, básico, donado
- **Filtrado rápido**: Buscar por empresa o nombre de contacto

### Sistema de Distribución
- **Desglose de ingresos**: Distribución automática de ventas mensuales
  - 5% Operaciones
  - 5% Inversor
  - 20% Fondo KAFEL
  - 35% Vendedores
  - 30% Programadores
- **Gráfico de distribución**: Visualización tipo donut del desglose
- **Detalles del Fondo KAFEL**: Split 60% Miguel / 40% Memo

### Catálogo de Productos
- **Catálogos Interactivos**: Base ($400k), Normal ($600k), Premium ($900k)
- **Inventario Automático**: Normal ($1M), Avanzado ($1.5M)
- **Agenda Automática**: $700k
- **Términos de pago**: 50% anticipo / 50% al recibir

### Registro de Usuarios
- **Registro dual**: Toggle entre vendedor y programador
- **Campos requeridos**:
  - Nombre completo
  - Cédula
  - Correo
  - Celular
  - Fecha de contrato
  - Referido de (vendedores solo, con dropdown automático)

## 📦 Stack Tecnológico

- **Frontend**: HTML5, CSS3, JavaScript Vanilla
- **Backend**: Supabase (PostgreSQL)
- **Visualizaciones**: Chart.js
- **Autenticación**: OpenAccess (sin contraseña)

## 🔧 Configuración

### Requisitos
- Navegador moderno (Chrome, Firefox, Safari, Edge)
- Conexión a internet
- Acceso a Supabase (credenciales ya incluidas)

### Instalación
1. Clonar el repositorio
2. Abrir `index.html` en el navegador
3. El dashboard se conectará automáticamente a Supabase

## 📊 Estructura de Datos

### Tabla: vendedores
```sql
id, nombre, cedula, correo, celular, fecha_contrato
nivel_comision (1 o 2), total_ventas, cantidad_ventas
bono_referido, referido_de (FK), estado
```

### Tabla: programadores
```sql
Mismo que vendedores + cantidad_proyectos, total_ganado
```

### Tabla: ventas
```sql
id, id_vendedor (FK), id_cliente (FK)
fecha_venta, monto_total, descripcion_servicio
estado_pago, nombre_empresa, nombre_encargado, nombre_vendedor
```

### Tabla: clientes
```sql
id, nombre_empresa, nombre_completo, telefono
instagram, tipo_cliente, estado
```

### Tabla: proyectos
```sql
id, id_programador (FK), nombre_proyecto
fecha_inicio, monto, estado
```

## 🎯 Funcionalidades Principales

### 1. Dashboard Principal
- Carga automática de estadísticas al abrir
- Gráfico dinámico que se actualiza con nuevas ventas
- Ranking de vendedores en tiempo real

### 2. Filtrado de Datos
- **Vendedores**: Búsqueda por nombre
- **Programadores**: Búsqueda por nombre
- **Clientes**: Búsqueda por empresa o contacto
- **Ventas**: Filtro por empresa, vendedor y estado

### 3. Detalles en Modal
- Información completa del vendedor/programador
- Historial de ventas/proyectos
- Estados de pago documentados

### 4. Registro de Nuevos Usuarios
- Validación de campos requeridos
- Toggle automático entre vendedor/programador
- Dropdown de referidos con datos en tiempo real

### 5. Distribución de Ingresos
- Cálculo automático por mes seleccionado
- Visualización gráfica
- Desglose detallado por categoría

## 📝 Notas de Desarrollo

### Estado de Implementación
✅ **Completado**:
- Sidebar de navegación
- Todas las tablas con filtrado
- Sistema de modales
- Gráficos Chart.js
- Distribución de ingresos

⏳ **En Progreso**:
- Sistema de comisiones avanzado
- Métricas de performance

❌ **Pendiente**:
- Eliminar vendedor (con contraseña)
- Sistema de referidos avanzado
- Reportes exportables
- Dark mode

### Credenciales Supabase
- URL: `https://vkagxzxthfwxmfcwlvrr.supabase.co`
- Las credenciales están en el código (considera variables de entorno)

### Políticas de RLS Requeridas
Las tablas deben tener políticas que permitan:
- SELECT para usuarios públicos
- INSERT para agregar nuevos registros
- UPDATE para actualizar datos
- DELETE para eliminar registros (con protección)

## 🚨 Troubleshooting

### Dashboard no carga
1. Verifica conexión a internet
2. Abre console (F12) y revisa errores
3. Verifica que Supabase esté disponible

### Tablas sin datos
1. Verifica que existan registros en Supabase
2. Revisa las políticas de RLS
3. Comprueba que los campos de la tabla coincidan

### Gráficos no se muestran
1. Verifica que Chart.js esté cargado
2. Revisa console para errores JavaScript
3. Asegúrate que hay datos en la tabla ventas

## 📞 Soporte

Para reportar problemas o solicitar mejoras, contacta al equipo de desarrollo.

## 📄 Licencia

© 2024 KAFEL Agency. Todos los derechos reservados.
