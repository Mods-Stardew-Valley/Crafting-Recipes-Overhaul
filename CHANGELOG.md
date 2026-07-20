# Changelog

Todas as mudanças importantes deste projeto serão documentadas neste arquivo.


## Unreleased



### Outras alterações


- Add files via upload

- Initialize README with project overview

Add project guide and change log for recipes

- Alterações iniciadas

- Inicio das modificacoes

Pensar melhor no que fazer nas proximas mudanças

- Mudanças muito grandes

versão 3.0.0 para acompanhar a alteração tão grande

- Inicial updates

GMCM translation

- Melhorias

- Traducao parcial

- Create CHANGELOG.md

- Adicionei link para o changelog no Readme

- Translations added

Some translations added
English
Portuguese
Brasilian

- Spanish ans French added

- Add i18n language translations

Add 14 new translation files for internationalization support: Czech, German, Hungarian, Italian, Japanese, Korean, Dutch, Polish, Russian, Thai, Turkish, Ukrainian, Vietnamese, and Chinese (Simplified). Each file includes localized strings for all mod features (chests, fertilizers, sprinklers, fences, rings, baits, hooks, lighting, flooring, totems, bombs, and signs).

- Consolidate recipes and fix typos

Move unchanged items to dedicated section in README. Update crafting recipes with adjusted costs and materials. Fix typo condition names (Ilumination→Lighting, Floring→Flooring, Totens→Totems). Add explanatory comments to recipes. Update Portuguese translations for Sprinklers and Baits features.

- Adjust crafting recipes for totems, bombs, and signs

Update crafting recipes in content.json to rebalance costs and outputs. Modified Warp Totem (Farm, Mountains, Beach, Desert, Island), Rain Totem and Treasure Totem entries (recipe changes and cost reductions). Adjusted explosives: Cherry Bomb, Bomb and Mega Bomb now produce different quantities and have reduced costs. Reduced resource costs for Wood, Stone and Dark Signs; Text Sign recipe also changed. Removed a stray TODO comment and cleaned up trailing blank lines; inline comments added to document changes.

- Add config namespace to i18n keys

Update all localization key paths in ConfigSchema to use the 'config.' namespace prefix. This organizes configuration-related strings within the i18n system.

- Add ConfigSchema translation guide to README

Document best practices for translating ConfigSchema in Content Patcher mods, including correct i18n key formatting and Android compatibility notes. This guide demonstrates the proper approach using the Crafting Recipes Overhaul mod as a tested example.

- Simplify ConfigSchema formatting

Remove i18n Name and Description fields from all ConfigSchema entries and reformat with consistent indentation. Each config option now contains only AllowValues and Default fields.

- Standardize i18n keys: rename .desc to .description

Rename all `.desc` keys to `.description` across all language files for consistency. Additionally, add `config.` prefix to all keys in pt-BR.json to match configuration key naming convention.

- Prefix config translation keys with namespace

Add 'config.' prefix to all translation keys across all language files (English, French, German, Spanish, Czech) to properly namespace configuration-related strings.

- Remove Tub o' Flowers and Fairy Dust recipes, namespace i18n keys

Removed crafting recipes for 'Tub o' Flowers' and 'Fairy Dust' from content.json as these items are no longer being modified. Updated README to list them under unchanged items. Added 'config.' prefix to all internationalization keys across 12 language files to properly namespace configuration strings.

- Toggle Moss recipe flag to false; bump version

Update content.json: change the "Moss" Data/CraftingRecipes entry from .../true/... to .../false/... (adjusting its boolean flag). Update manifest.json: bump Version from 3.0.0 to 3.0.1.

- Add automated changelog generation

Set up git-cliff to automatically generate and maintain CHANGELOG.md on commits to main branch. Includes GitHub Actions workflow that uses conventional commits to organize changes by type (features, fixes, performance, refactoring, etc.) with Portuguese-localized category names.


