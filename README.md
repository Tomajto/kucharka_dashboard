# Kuchařka Dashboard

Admin panel pro správu receptů s napojením na Supabase.

## Jak to používat

### Buď jdi na stránku `https://kucharkadashboard.netlify.app/`

### 1. Instalace

```powershell
npm install
```

### 2. Spuštění vývojového serveru

```powershell
npm run dev
```

Aplikace se otevře v prohlížeči (obvykle na `http://localhost:5173`).

### 3. Přihlášení

- Otevři aplikaci v prohlížeči
- Zadej přihlašovací údaje (email a heslo do Supabase Auth)
- Po úspěšném přihlášení se zobrazí admin panel

### 4. Přidání nového receptu

1. **Základní informace:**
   - Název receptu (povinné)
   - Popis
   - Obtížnost (lehké/střední/těžké)
   - Kategorie (hlavní jídlo, dezert, polévka, salát, snídaně)
   - Doba přípravy v minutách

2. **Ingredience:**
   - Zadej název a množství pro každou ingredienci
   - Použij tlačítko "+ Přidat ingredienci" pro další položky
   - Odeber nepotřebné tlačítkem "✕"

3. **Postup přípravy:**
   - Zadej jednotlivé kroky postupu
   - Použij tlačítko "+ Přidat krok" pro další kroky
   - Odeber nepotřebné tlačítkem "✕"

4. **Obrázky:**
   - Vyber jeden nebo více obrázků
   - Zobrazí se náhled před nahráním
   - Můžeš odebrat vybraný obrázek tlačítkem "✕"

5. Klikni na **"Uložit recept"**

### 5. Správa receptů

- Všechny recepty se zobrazují pod formulářem
- Každý recept má náhledový obrázek a název
- Kliknutím na **"Smazat"** odstraníš recept (včetně všech obrázků ze Storage)

### 6. Odhlášení

Klikni na tlačítko **"Odhlásit se"** v pravém horním rohu.

## Build pro produkci

```powershell
npm run build
```

Vytvoří se složka `dist/` s optimalizovanými soubory připravenými k nasazení.

## Poznámky

- Obrázky se ukládají do Supabase Storage v bucketu `kucharkaObrazky`
- Databáze má 4 tabulky: `recipes`, `recipe_ingredients`, `recipe_steps`, `recipe_images`
- Přístup k admin funkcím je chráněn přihlášením (Supabase Auth)
