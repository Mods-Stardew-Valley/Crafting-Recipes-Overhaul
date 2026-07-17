# Translating ConfigSchema in Content Patcher

If you're using `ConfigSchema` in a Content Patcher mod, you **don't need** to use `{{i18n:...}}` for option names.

## ❌ Incorrect

```json
"ConfigSchema": {
  "Chests": {
    "AllowValues": "true, false",
    "Default": false,
    "Name": "{{i18n:Chests.name}}",
    "Description": "{{i18n:Chests.desc}}"
  }
}
```

## ✅ Correct

```json
"ConfigSchema": {
  "Chests": {
    "AllowValues": "true, false",
    "Default": false
  }
}
```

Then, add the translation in `i18n/default.json` (or `i18n/pt.json`):

```json
{
  "config.Chests.name": "Chests",
  "config.Chests.description": "Reduces the amount of materials required to craft all chests."
}
```

For another language:

```json
{
  "config.Chests.name": "Baús",
  "config.Chests.description": "Reduz significativamente a quantidade de materiais necessária para fabricar qualquer um dos baús."
}
```

## Notes

- Use `config.<OptionName>.name` for the option label.
- Use `config.<OptionName>.description` for the description.
- Do **not** use `Name`, `Description`, or `{{i18n:...}}` inside `ConfigSchema`.
- Boolean options (`true/false`) are displayed as checkboxes by Generic Mod Config Menu.
- Some GMCM versions (especially Android ports) may not display descriptions, but keeping the `config.<OptionName>.description` entries is recommended for compatibility.


## Tested Example

This translation system has been tested with:

- Stardew Valley 1.6
- Content Patcher 2.8.1
- Generic Mod Config Menu
- Android-compatible setup

The example above was validated using a real Content Patcher mod with **19 translation files** and translated configuration options.

If you'd like a complete working example, see:

**Crafting Recipes Overhaul**  
:contentReference[oaicite:0]{index=0}

This mod demonstrates:

- `ConfigSchema` with translated option names.
- The `config.<OptionName>.name` localization format.
- Multi-language support using the `i18n` folder.
- A complete project structure for Content Patcher.
- Android-compatible implementation without C#.

If you find this documentation useful, feel free to reference it in your own projects or contribute improvements.

### Android Compatibility

When using Generic Mod Config Menu with Content Patcher:

- ✅ `config.<Option>.name` works correctly.
- ❌ `config.<Option>.description` is currently ignored.
- ❌ `config.<Option>.tooltip` is currently ignored.

Tested behavior (Content Patcher 2.8.1 + GMCM 1.16.0):

 - ✅ config.<Option>.name works.
 - ❌ config.<Option>.description was not displayed.
 - ❌ config.<Option>.tooltip was not displayed.

This appears to be a current limitation of Content Patcher's ConfigSchema, not of the translation files themselves.


Guia do projeto Crafting Recipes Overhaul

Itens não alterados

   Torch
   Field Snack
   Bug Steak
   Garden Pot
   Seed Maker
   Mini-Jukebox
   Staircase
   Iron Fence
   Transmute (Fe)
   Transmute (Au)
   Jack-O-Lantern
   Wicked Statue
   Skull Brazier
   Marble Brazier
   Oil Of Garlic
   Life Elixir
   Farm Computer
   Geode Crusher
   Solar Panel
   Bone Mill
   Heavy Tapper
   Hopper
   Tub o' Flowers
   Fairy Dust

   Statue Of The Dwarf King

Alterações padrão feitas nos seguintes itens:

    * Chest - reduzido custo para 10 madeira
    * Fertilizers - Saida aumentada para 10 em todos


Compatibilidade com GMCM adicionada para Alterações Opcionais (por padrão estão desligadas)

 Chests
    Redução de recursos usados
 
 AltFertilizers
    Adição de receitas alternativas
 
 Sprinklers 
    Redução de recursos usados
 
 AddMoss
    Adição de receita 
 
 Fences
    Aumento na quantidade produzida
 
 Rings
    Redução de recursos usados

 Baits
    Aumento na quantidade produzida
    Redução de recursos usados
 
 FishHooks 
    Redução de recursos usados
 
 Ilumination
    Redução de recursos usados
 
 Floring
    Aumento na quantidade produzida
 
 Totens
    Redução de recursos usados
 
 Bombs 
    Aumento na quantidade produzida
    Redução de recursos usados
 
 Signs
    Redução de recursos usados



Receitas alternativas adicionadas com condição no GMCM
    Falta editar as receitas alternativas


    ## Changelog

Veja o histórico completo em [CHANGELOG.md]