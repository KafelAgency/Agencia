# 🚀 Quick Start Guide

Get up and running with the KAFEL Admin Dashboard in 2 minutes.

## Installation

1. **Copy the file**
   ```bash
   # The dashboard is a single HTML file - no installation needed!
   cp index.html /your/web/server/
   ```

2. **Open in browser**
   ```
   http://localhost/index.html
   # or simply open index.html directly in your browser
   ```

3. **Verify connection**
   - Look for green checkmark: "✓ Conectado" in top-left
   - If red error appears, check internet connection and Supabase status

## First Time Setup

### Check Database
Ensure you have these tables in Supabase with proper RLS policies:
- `vendedores` - Vendor data
- `programadores` - Programmer data
- `clientes` - Client registry
- `ventas` - Sales transactions
- `proyectos` - Programmer projects

### Set RLS Policies
Each table needs policies allowing:
```sql
-- For public access (development)
SELECT, INSERT, UPDATE, DELETE for authenticated users
```

## Quick Navigation

### 📊 Dashboard
- View monthly statistics
- See sales by category
- Check top 5 vendors

**Keyboard shortcut**: Click "Dashboard" in sidebar

### 👥 Vendedores
- View all vendors
- Click "Ver" to see sales history
- Delete vendor with password (Ukeyo/24398As+-)

**Search**: Type vendor name in search box

### 💰 Ventas
- Browse all sales
- Filter by empresa, vendedor, estado

**Three filters**: Company search + Vendor dropdown + Status dropdown

### 💻 Programadores
- Similar to vendedores
- Track projects instead of sales
- Same delete functionality

### 📋 Clientes
- Browse all clients
- Search by company or contact name

### 📈 Distribución
1. Select month from dropdown
2. Click "Cargar" button
3. View breakdown chart
4. See 60/40 split between Miguel and Memo

### 📦 Catálogo
- View all product pricing
- Check payment terms (50/50)

### ➕ Registrar
1. Toggle between "Vendedor" and "Programador"
2. Fill in form fields
3. For vendors: Select referrer (optional)
4. Click "Registrar"

## Common Tasks

### Add New Vendor
1. Click "➕ Registrar"
2. Keep toggle on "👥 Vendedor"
3. Fill: Nombre, Cédula, Correo, Celular, Fecha Contrato
4. Optionally select "Referido de" (referrer)
5. Click "Registrar"

### Delete Vendor
1. Click "👥 Vendedores"
2. Find vendor in list
3. Click "Ver" button
4. Click red "🗑️ Eliminar" button
5. Enter password: `Ukeyo/24398As+-`
6. Confirm deletion

### Search Vendor
1. Go to section (Vendedores, Programadores, Clientes)
2. Type in search box
3. List filters automatically

### View Monthly Distribution
1. Click "📈 Distribución"
2. Pick month from dropdown
3. Click "Cargar"
4. See chart and breakdown

### Check Product Pricing
1. Click "📦 Catálogo"
2. View all 3 product lines:
   - Catálogos Interactivos ($400k-$900k)
   - Inventario Automático ($1M-$1.5M)
   - Agenda Automática ($700k)

## Troubleshooting

### "✗ Conectado" appears
**Problem**: Not connected to Supabase
- Check internet connection
- Verify Supabase is running
- Wait 5 seconds, refresh page

### No data appears in tables
**Problem**: Database is empty or RLS policies blocking
- Add test records to Supabase
- Verify RLS policies are set to allow INSERT
- Check browser console (F12) for errors

### Filters not working
**Problem**: Event listeners not attached
- Refresh the page
- Check browser console for JavaScript errors

### Delete button not working
**Problem**: Wrong password or no Supabase connection
- Verify password: `Ukeyo/24398As+-` (exact match)
- Check green connection indicator
- Try password again (case-sensitive)

### Charts not showing
**Problem**: Chart.js not loaded or no data
- Refresh page
- Check that ventas table has data
- Verify Chart.js CDN is accessible

## Browser Requirements

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

**Mobile**: Responsive design works on tablets (not optimized for phones)

## Credentials

**Dashboard**: No login required (open access)

**Delete password**: `Ukeyo/24398As+-` (Memo's password)

**Supabase**:
- URL: `https://vkagxzxthfwxmfcwlvrr.supabase.co`
- Public key: Embedded in code

## Pro Tips

1. **Bookmark the page** for quick access
2. **Use Chrome DevTools** (F12) to debug issues
3. **Check the console** for status messages
4. **Filters are instant** - no need to click search
5. **Modals show** - click X or "Cerrar" to close
6. **Deletion is final** - no undo, requires password

## What's Next?

After initial setup:
1. ✅ Add some test vendors/programmers
2. ✅ Create sample sales data
3. ✅ Try filtering and searching
4. ✅ View distribution for current month
5. ✅ Test delete vendor (with password)

## Files Included

- **index.html** - Complete dashboard application
- **README.md** - Detailed feature documentation
- **PROGRESS.md** - Implementation status
- **IMPLEMENTATION_SUMMARY.md** - Session summary
- **QUICKSTART.md** - This file

## Need Help?

1. Check **README.md** for detailed features
2. Check **PROGRESS.md** for technical details
3. Check browser console (F12) for error messages
4. Verify Supabase is connected (green indicator)

---

**Last Updated**: September 18, 2024  
**Status**: ✅ Production Ready
