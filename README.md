# Ivet · Tréning

Hotová statická webová aplikácia pripravená pre GitHub Pages.

## Nastavenie
- Supabase project: `nragtrsgbvrnmbwlowoi`
- `CLIENT_ID = 'wife'`
- aktívny tréningový plán sa číta zo Supabase
- frontend používa iba publishable key, nie service role
- appka je určená pre čistý HTML/CSS/JS hosting cez GitHub Pages

## Nahratie do GitHubu
Nahraj celý obsah tohto priečinka do koreňa repozitára, aby `index.html` bol priamo v root-e.

Potom v GitHub repozitári:
1. Settings
2. Pages
3. Build and deployment: Deploy from a branch
4. Branch: `main`
5. Folder: `/ (root)`

## Dôležité
Táto verzia je oddelená cez `client_id = wife`.

Legacy `workout_logs` a `body_measurements` nie sú pre Ivet používané, pretože tieto existujúce tabuľky nemajú `client_id` a obsahujú Dávidove osobné dáta. Vďaka tomu sa v Ivet appke nezmiešajú Dávidove historické tréningy ani telesné merania.

Ak má Ivet používať vlastný Supabase účet namiesto účtu, ktorý dnes vlastní jej plán, treba následne nastaviť vlastníctvo/RLS tak, aby jej používateľ mal k riadkom `wife` prístup.

## UX/UI
Finálna verzia drží:
- spodnú navigáciu Tréning / História / Progres / Profil
- A/B tréningy z aktívneho plánu
- jeden scrollovateľný aktívny workout
- RAMP
- MINULE / KG / REPS / HOTOVO
- autosave
- sticky rest timer
- 4 možnosti ukončenia tréningu
- históriu
- progres cvikov, tonáž, grafy a odhad 1RM
- editáciu cviku a náhradu cviku
