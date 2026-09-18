# Список графических ассетов и предметов для отрисовки: проект «Грошик»

Данный документ содержит полный перечень 2D-графики, иллюстраций, предметов, персонажей и UI-элементов, необходимых для создания финальной визуальной версии детского финансового сервиса «Грошик» (целевая аудитория 7–11 лет, стиль: тёплая сказочная стилизация, русский фольклор в современном дружелюбном прочтении).

---

## 1. Главный герой — Кот Грошик

Грошик — озорной, любознательный зверек. В начале игры он ничего не смыслит в деньгах, но с заботой и грамотными решениями ребёнка взрослеет и умнеет.

### 1.1. Базовая кастомизация (экран создания питомца 02)
- **3 расцветки шерсти**:
  - `pet_fur_gray` — классический дымчато-серый с белой грудкой.
  - `pet_fur_ginger` — солнечный тёплый рыжик с полосками.
  - `pet_fur_white` — пушистый белоснежный / светло-кремовый.
- **3 цвета шейного платка / шарфика**:
  - `pet_scarf_light` — льняной светлый с золотистой каймой.
  - `pet_scarf_blue` — васильково-синий сказочный с узором.
  - `pet_scarf_red` — традиционный алый с вышивкой.
- *Итого базовых вариаций*: 9 уникальных комбинаций питомца (требование раздела 2.6 ТЗ).

### 1.2. Стадии эволюции / взросления питомца (раздел 2.5.10 ТЗ)
1. `pet_stage_1_kitten` — **Малыш**: круглый, неуклюжий котёнок, широко распахнутые глаза.
2. `pet_stage_2_teen` — **Подросток**: подросший ловкий кот с походной кожаной сумкой для монет через плечо.
3. `pet_stage_3_scholar` — **Младший учёный кот**: статный уверенный кот с маленькими круглыми очками на лбу, пером за ухом или нарядным жилетом.

### 1.3. Эмоциональные состояния и анимации (экраны 03, 03.1, 13, 14)
- `pet_state_idle` — спокойная стойка / приветливое покачивание хвостом (базовое состояние).
- `pet_state_joy_high` — радостный, сияющий, прыгает от счастья (радость >70 или при получении награды).
- `pet_state_joy_low` — грустный, поникшие ушки, хвост опущен (радость <40, нехватка внимания или развлечений).
- `pet_state_hungry` — урчащий животик, держит в лапках пустую деревянную ложку (сытость <30).
- `pet_state_fed` — сытый, довольный, довольно облизывается лапкой (после покупки каши).
- `pet_state_sick` — простуженный: сидит в тёплом шарфе, чихает, термометр во рту или компресс на голове (событие болезни без страховки, здоровье 60).
- `pet_state_recovered` — бодрый, здоровый, скидывает компресс и машет лапой (после бесплатного ухода или защиты).
- `pet_state_sleep` — свернулся калачиком под лоскутным одеялом на лежанке (экран завершения дня 13/14).
- `pet_state_thinking` — чешет за ушком, озадаченный вид (при принятии решений в квесте или бюджете).

---

## 2. Сказочные артефакты (Цели накопления и квестовые награды)

Каждый артефакт олицетворяет ключевую концепцию финансовой грамотности. Артефакты отображаются в магазине (20), карточке цели (10, 21), окне получения (12) и коллекции персонажа (03.1).

### 2.1. Семь основных игровых артефактов
Для каждого артефакта требуется:
- **Полноразмерная иллюстрация** (512 × 512 px) для карточки и витрины.
- **Иконка коллекции** (128 × 128 px) в 2 состояниях: *получен* (цветной с эффектом сияния) и *заблокирован* (серый силуэт с замком).

1. `artifact_cloth` — **Скатерть-самобранка** (*Тема: Финансовая подушка безопасности*):
   - Белая льняная скатерть с красной славянской вышивкой, на которой сами собой появляются горшочек каши, румяный пирожок и яблоки.
2. `artifact_water` — **Склянка с живой водой** (*Тема: Резерв на случай непредвиденных ошибок*):
   - Изящный гранёный стеклянный флакон с деревянной пробкой, внутри мерцает бирюзовая живая вода со светящимися пузырьками.
3. `artifact_clew` — **Путеводный клубок** (*Тема: Вложения в знания и навыки*):
   - Мягкий клубок золотисто-жёлтой волшебной шерсти, от которого тянется светящаяся нить, указывающая верную дорогу.
4. `artifact_shield` — **Богатырский щит** (*Тема: Защита от обмана и сомнительных сделок*):
   - Круглый деревянный щит с металлической кованой оковкой и чеканным знаком солнца/богатыря в центре.
5. `artifact_gusli` — **Гусли-самогуды** (*Тема: Регулярный доход и позитивная мотивация*):
   - Деревянные крыловидные гусли с тонкой резьбой, струны вибрируют, вокруг вьются золотистые нотки и искры.
6. `artifact_house` — **Расписной терем** (*Тема: Большая долгосрочная финансовая цель*):
   - Сказочный терем с резными ставнями, коньком на крыше, крыльцом и светящимися тёплыми окнами.
7. `artifact_boots` — **Сапоги-скороходы** (*Тема: Качественный переход на новый уровень / Тридевятое царство*):
   - Пара ярко-красных сафьяновых сапожек с загнутыми носками, золотым тиснением и маленькими летящими крылышками на пятках.

### 2.2. Дополнительные артефакты сказочного мира (из дизайн-документа и расширения)
8. `artifact_chest_morozko` — **Сундук Морозко**: ледяной кованый ларчик, покрытый кристаллами инея.
9. `artifact_feather_firebird` — **Перо Жар-птицы**: сияющее тёплое золотисто-огненное перо.
10. `artifact_silver_hoof` — **Серебряное копытце**: серебряная подковка или миниатюрный оленёнок с россыпью самоцветов.
11. `artifact_golden_egg` — **Золотое яичко**: яйцо чистого золота на резной дубовой подставке.
12. `artifact_unspent_ruble` — **Неразменный рубль**: старинная круглая монета с витиеватой чеканкой.
13. `artifact_magic_apple` — **Молодильное яблоко**: румяное сочное яблоко с золотым бочком и зелёным листком.
14. `artifact_magic_mirror` — **Серебряное блюдечко и наливное яблочко**: блюдечко с каёмочкой, по которому катится яблоко.

---

## 3. Сюжетные персонажи квестов (NPC)

Персонажи представляют 5 образовательных тем. Для них требуются:
- **Крупная сюжетная иллюстрация** (~2/3 экрана смартфона, вертикальная, соотношение 4:3 или 16:9) для карточки и диалога квеста (экраны 23, 24).
- **Круглый портрет-аватар** (128 × 128 px) для маркеров на карте (экран 22).

1. `hero_fish` — **Золотая рыбка** (*Тема 1: Планирование бюджета и приоритеты*):
   - Сказочная волшебная рыбка с добрыми выразительными глазами, короной на голове и прозрачными струящимися плавниками, выглядывает из чистой речной заводи среди кувшинок.
2. `hero_morozko` — **Морозко** (*Тема 2: Накопления и отложенная награда*):
   - Добрый величественный старец с пушистой седой бородой, в богато расшитой морозной сине-серебряной шубе и шапке, в руке резной ледяной посох.
3. `hero_raja` — **Раджа** (*Тема 3: Импульсивные траты и изменение цен*):
   - Колоритный восточный торговец-гость в шёлковом тюрбане с брошью, окружённый блестящими побрякушками, расписными тканями и яркими товарами.
4. `hero_peasant_and_barin` — **Смекалистый мужик и барин** (*Тема 4: Инвестиции в навыки и труд*):
   - Композиция из двух персонажей: находчивый мужичок в опрятной холщовой рубахе с хитрым прищуром и дородный барин в богатом кафтане.
5. `hero_fox` — **Хитрый Лис** (*Тема 5: Критическое мышление и защита от мошенников*):
   - Лис в нарядном купеческом картузе и жилете, с широкой льстивой улыбкой и пушистым рыжим хвостом; держит шкатулку с «чудо-зерном».

---

## 4. Локации, фоны и окружение

### 4.1. Домик Грошика (экран 03)
- `bg_house_starter` — **Стартовая лесная избушка**:
  - Уютная деревянная изба, бревенчатые стены, небольшое окно с простыми занавесками, деревянная лежанка с ковриком, печка на заднем плане.
- `bg_house_terem` — **Расписной терем** (трансформация после получения артефакта «Терем»):
  - Просторная светлая палата, изразцовая печь, резные дубовые лавки, праздничные узоры, сундучок с резьбой, витражное окно с видом на сказочный лес.

### 4.2. Интерактивная карта заданий (экран 22)
- `bg_map_full` — **Карта Тридевятого царства**:
  - Стилизованная карта в виде пергамента со сказочной географией: извилистые тропинки, речка, лесные массивы, горы вдалеке.
- **5 маркеров локаций на карте**:
  - `loc_pond` — **Пруд желаний** (заводь с кувшинками и камышами).
  - `loc_glade` — **Снежная поляна** (зимний остров с сугробами и ёлками в снегу).
  - `loc_bazaar` — **Шумная ярмарка** (шатры, флажки, торговые ряды).
  - `loc_yard` — **Двор смекалки** (деревенское подворье с амбаром и мельницей).
  - `loc_crossroad` — **Перекрёсток обещаний** (распутье трёх дорог с путевым камнем).
- `map_locked_fog` — область облаков/тумана, закрывающая неизведанные дали до покупки сапог-скороходов.

### 4.3. Магазин и Стол Подорожника (экран 08)
- `bg_shop_interior` — деревянная сказочная ярмарочная лавка с резными полками для товаров.
- `shop_podorozhnik_stand` — **Стол Подорожника**:
  - Выделенный уголок с навесом, связками целебных трав, свежими зелёными листьями подорожника, табличкой с зелёным крестиком/листком и чистым свитком правил защиты.

---

## 5. Товары магазина и предметы повседневного обихода (экраны 08, 09)

Товары разделены на категории «Надо» (обязательные базовые нужды) и «Хочу» (желания и радость):

### 5.1. Категория «Надо» (Обязательные расходы)
- `item_food_porridge` — **Каша в глиняном горшочке** (10 монет):
  - Пузатый глиняный горшочек с горячей пшённой кашей, кусочком сливочного масла, деревянной расписной ложкой и ароматным паром.
- `item_insurance_leaf` — **Страховка «Подорожник»** (5 монет):
  - Крупный глянцевый изумрудный лист подорожника, перевязанный золотой тесьмой со знаком щита/сердца.

### 5.2. Категория «Хочу» (Необязательные расходы)
- `item_toy_horse` — **Деревянная игрушка** (15 монет):
  - Традиционная деревянная точёная лошадка-качалка с яркой росписью (радость +25).
- `item_ribbon` — **Лента для домика** (5 монет):
  - Свёрнутый рулончик нарядной шёлковой ленты с геометрическим узором (радость +10).
- `item_gingerbread` — *Дополнительно*: медовый печатный пряник в форме птички.
- `item_whistle` — *Дополнительно*: глиняная свистулька в форме петушка.

---

## 6. Предметы интерактивных квестовых сцен

Графика для карточек выбора и интерактивных решений внутри пяти учебных историй (экран 24):

### 6.1. Квест «Золотая рыбка» (Приоритеты и ремонт дома)
- `quest_card_roof` — **Крыша** (10 монет, *Надо*): доски, связка соломы/дранки, инструмент.
- `quest_card_bed` — **Кровать** (10 монет, *Надо*): уютная деревянная кровать с мягким сенником и подушкой.
- `quest_card_crown` — **Корона** (15 монет, *Хочу*): блестящая золотая корона с рубинами.
- `quest_card_garland` — **Украшение** (5 монет, *Хочу*): венок из полевых цветов или гирлянда флажков.
- `quest_scene_rain_good` — уютный тёплый дом, за окном дождь, в доме сухо и топится печь.
- `quest_scene_rain_leak` — капли дождя капают в подставленный тазик сквозь дырявую крышу, кот с зонтиком.

### 6.2. Квест «Морозко» (Шаги к цели и отложенная награда)
- `quest_piggy_empty` — пустой резной ледяной сундучок (0 из 30).
- `quest_piggy_step1` — сундучок с горсткой монет (10 из 30).
- `quest_piggy_step2` — сундучок наполовину полон (20 из 30).
- `quest_piggy_full` — переливающийся сундучок с сияющими гуслями (30 из 30).
- `quest_card_cracker` — **Хлопушка** (5 монет): праздничная зимняя хлопушка с серпантином (соблазн сиюминутной траты).

### 6.3. Квест «Раджа» (Импульсивные покупки и рост цен)
- `quest_cart_item_bread` — буханка подового хлеба / каша (еда для дороги).
- `quest_cart_item_ticket` — проездной жетон / колокольчик для повозки (проезд).
- `quest_tempt_beads` — нитка сверкающих разноцветных стеклянных бус (соблазн Раджи).
- `quest_tempt_feather` — переливающееся павлинье перо (соблазн Раджи).
- `quest_tempt_fan` — резной восточный веер с золотым тиснением (соблазн Раджи).
- `quest_price_tag_old_new` — плашка сравнения ценников (старая цена зачёркнута, новая написана красным).

### 6.4. Квест «Смекалистый мужик и барин» (Инвестиции в навыки)
- `quest_scroll_lesson` — свёрнутый берестяной свиток / грамота урока смекалки (5 монет).
- `quest_grain_bag` — холщовый мешок с зерном, перевязанный бечёвкой (набор из 5 перемещаемых мешков).
- `quest_zone_seed` — амбар «На семена урожая».
- `quest_zone_food` — печь «На пропитание».
- `quest_zone_sell` — телега «На продажу».

### 6.5. Квест «Хитрый Лис» (Защита от мошенничества)
- `quest_magic_grain` — крошечное зёрнышко, испускающее неестественный золотой дым, в роскошной бархатной шкатулке.
- **4 карточки настораживающих признаков (красных флагов)**:
  - `flag_huge_profit` — значок «Гора золота из одной монеты» (нереалистичные обещания).
  - `flag_hurry` — горящие песочные часы / таймер (давление временем и спешка).
  - `flag_give_all` — вывернутый пустой кошелёк (просьба отдать все накопления).
  - `flag_no_rules` — свиток с вопросительными знаками (отсутствие ясных условий и гарантий).

---

## 7. Элементы интерфейса (UI Design System, Icons & Badges)

### 7.1. Игровая валюта и кошельки
- `ui_coin_single` — золотая монета «Грошик» (с тиснением силуэта кошачьей лапки или колоска).
- `ui_coin_stack` — небольшая аккуратная стопка золотых монет.
- `ui_coin_bag` — плотный пузатый мешочек с монетами, перевязанный лентой.
- `ui_wallet` — традиционный кожаный кошелёк-калита на поясе.
- `ui_piggybank` — сказочная деревянная или керамическая копилка.

### 7.2. Шкалы и индикаторы состояния питомца (экран 03.1)
- `ui_stat_hunger` — иконка сытости (глиняная мисочка / колосок).
- `ui_stat_joy` — иконка радости (сияющее солнышко / золотой бубенец).
- `ui_stat_health` — иконка здоровья (зелёный росток / сердце с листом).
- `ui_progress_bar_frame` — резная деревянная рамка для шкал прогресса (состояния наполнения: зелёное, жёлтое, красное).

### 7.3. Нижняя навигационная панель (Bottom Navigation Bar)
Для каждого таба требуется 2 состояния: *Inactive* (контурный/монохромный) и *Active* (яркий, акцентный с подсветкой):
- `tab_home_active` / `tab_home_inactive` — Избушка / Домик.
- `tab_map_active` / `tab_map_inactive` — Развёрнутая карта с компасом.
- `tab_shop_active` / `tab_shop_inactive` — Ярмарочный прилавок с флажком.
- `tab_savings_active` / `tab_savings_inactive` — Копилка / Сундучок с монеткой.

### 7.4. Системные и управляющие пиктограммы
- `icon_settings` — резная деревянная шестерёнка.
- `icon_sound_on` / `icon_sound_off` — дудочка/рожок со звуковыми волнами и перечёркнутый.
- `icon_music_on` / `icon_music_off` — нотный знак / гусельки.
- `icon_text_large` — иконка лупы или буквы «АА» для режима крупного шрифта (доступность).
- `icon_info_help` — берестяная грамота со знаком вопроса.
- `icon_back_arrow` — резная стрелка «Назад».
- `icon_close_cross` — деревянный крестик закрытия модального окна.
- `icon_check_mark` — зелёная галочка подтверждения / выполненного задания.
- `icon_calendar_day` — сказочный календарь с номером текущего дня.
- `icon_lock_closed` / `icon_lock_open` — навесной амбарный замок (раздел взрослого и PIN).
- `icon_parent_gate` — значок совы в очках или взрослой лапы с маленькой лапкой.

---

## 8. Полноэкранные иллюстрации системных экранов (Story & Modal Screens)

1. `ill_welcome_book` — **Экран знакомства (01)**:
   - Раскрытая старинная книга сказок, из страниц которой поднимается золотистое волшебное сияние, и маленький Грошик с любопытством выглядывает наружу.
2. `ill_onboarding_1` — **Онбординг шаг 1**: Грошик держит кошелёк и показывает, как монеты попадают в кошелёк.
3. `ill_onboarding_2` — **Онбординг шаг 2**: Грошик показывает на своё настроение и здоровье, объясняя важность заботы.
4. `ill_onboarding_3` — **Онбординг шаг 3**: Грошик с блокнотом и карандашом раскладывает монетки по трём кучкам (Надо / Хочу / Цель).
5. `ill_night_summary` — **Экран подведения итогов дня (14)**:
   - Тёплый ночной пейзаж за окном, месяц на небе, спящий сытый Грошик, на столе лежит раскрытый свиток с итогами и монетка-награда.
6. `ill_goal_achieved` — **Экран триумфа / достижение цели (12)**:
   - Праздничные конфетти, сияющий долгожданный артефакт в центре, счастливый Грошик подбрасывает колпак вверх.
7. `ill_diploma_passport` — **Цифровой «Паспорт Хранителя» / Грамота финансового успеха**:
   - Красиво оформленная грамота в русском стиле с вензелями, именем питомца, итоговыми сбережениями и печатью Кота Учёного (для сохранения и демонстрации родителям).

---

## 9. Маркетинговые и публикационные материалы (RuStore)

Требования раздела 3.3 Технического задания:
1. `app_icon_512` — **Основная иконка приложения** (512 × 512 px, PNG):
   - Выразительная круглая мордочка улыбающегося Грошика в платочке на тёплом фоне с золотой сияющей монеткой.
2. `feature_banner_1024_500` — **Промо-баннер для магазина** (1024 × 500 px):
   - Грошик на фоне сказочного терема и карты Тридевятого царства с ключевыми артефактами.
3. **Серия скриншотов для витрины RuStore** (не менее 4 экранов, 1080 × 1920 px):
   - Скриншот 1: Создание уникального питомца и выбор сложности.
   - Скриншот 2: Главный экран-домик и распределение бюджета.
   - Скриншот 3: Карта сказочных заданий и диалоги с героями.
   - Скриншот 4: Магазин, стол подорожника и сундучок с накоплениями.

---

## 10. Технические требования к форматам файлов

| Тип графики | Формат | Разрешение / Масштаб | Примечания |
|---|---|---|---|
| **Иконки интерфейса** | SVG (вектор) + PNG | 24×24 dp, 48×48 dp | Минимальный кликабельный размер по ТЗ — 48×48 dp |
| **Предметы и товары** | PNG с прозрачностью / WebP | 256×256 px (@2x, @3x) | Чёткий контур, контрастность к светлому фону |
| **Артефакты** | PNG с прозрачностью / WebP | 512×512 px | Отдельно цветная версия и монохромный силуэт |
| **Иллюстрации квестов** | PNG / WebP | 800×600 px (или 1200×900 px) | Соотношение сторон 4:3 под карточку квеста |
| **Фоны экранов** | PNG / JPG / WebP | 1080×1920 px (9:16) | Бесшовное масштабирование под разные экраны |
| **Иконка приложения** | PNG (без прозрачности) | 512×512 px | Под требования RuStore |

---

## 11. Руководство по промптам для ИИ (AI Prompt Engineering Guide)

Ниже приведены готовые англоязычные промпты для генерации графики через современные диффузионные модели (Midjourney v6, Stable Diffusion XL / SD3, DALL-E 3, Flux).

### Общий стилевой модификатор (Master Style Modifier)
Добавляйте в конец каждого промпта для изолированных предметов и персонажей:
> `, cute stylized 2D digital art illustration, cozy Slavic fairytale aesthetic, warm friendly storybook style, soft volumetric lighting, vibrant charming colors, clean smooth outlines, gentle watercolor & gouache texture, children's mobile game asset, high detail, isolated on neutral white background`

### Отрицательный промпт (Negative Prompt)
> `photorealistic, 3d realistic render, dark, horror, grotesque, deformed anatomy, distorted limbs, extra paws, ugly, text, watermark, logo, signature, noisy background, blurry, cropped, low quality`

---

### Категория 1: Питомец Грошик (Hero Character Prompts)

- **Котёнок-малыш (базовый образ)**:
  ```text
  A charming cute little cartoon kitten-creature named Groshik, rounded chubby body, big innocent curious glossy eyes, joyful welcoming expression, standing on two hind legs, soft gray fur with a fluffy cream chest, no accessories, stylized 2D storybook illustration, clean vector outlines, warm pastel colors, isolated on plain white background --ar 1:1
  ```
- **Вариации окраса**:
  - *Рыжий*: `Cute little ginger cat creature with warm orange tabby stripes, cheerful playful expression, fluffy cheeks, large glossy emerald eyes, stylized 2D storybook art, isolated on white background --ar 1:1`
  - *Белый*: `Adorable pure white fluffy cartoon kitten creature, delicate pink nose, soft cream fur accents, large sapphire blue eyes, friendly pose, stylized 2D storybook art, isolated on white background --ar 1:1`
- **Шейные платки (аксессуар)**:
  - *Светлый льняной*: `...wearing a neat rustic linen neckerchief tied with a tiny wooden bead, warm golden trim...`
  - *Синий васильковый*: `...wearing a cozy cornflower-blue folkloric neckerchief with delicate white Slavic snowflake embroidery...`
  - *Алый*: `...wearing a bright crimson-red embroidered fairytale neckerchief with traditional gold stitching...`
- **Стадии эволюции**:
  - *Подросток*: `Energetic young cartoon cat adventurer, slightly taller, proud smiling pose, wearing a woven folkloric neckerchief and a tiny rustic leather satchel bag for gold coins slung across shoulder, stylized 2D fairytale art, isolated on white background --ar 1:1`
  - *Младший учёный кот*: `Wise young scholar cat character, sitting upright, wearing small round golden spectacles pushed up on forehead, an elegant embroidered folkloric vest, feather quill pen tucked behind ear, confident kind smile, stylized 2D fairytale art, isolated on white background --ar 1:1`
- **Эмоциональные состояния**:
  - *Радость (>70)*: `Extremely happy playful little cat mascot, jumping in the air with paws outstretched, sparkling magical golden stars and hearts around, huge bright smile, pure joy and celebration, isolated on white background --ar 1:1`
  - *Голодный*: `Cute cartoon kitten holding a small empty wooden spoon, clutching its rumbling tummy, wide imploring sad puppy eyes, gentle comical hunger expression, isolated on white background --ar 1:1`
  - *Простуженный (болезнь)*: `Cute little sick cartoon cat, sitting wrapped snugly in a thick patchwork woolen blanket and warm knitted scarf, holding a hot ceramic mug with steam, comical mild cold expression, comforting and non-scary, isolated on white background --ar 1:1`
  - *Сон (итоги дня)*: `Adorable cartoon kitten sleeping peacefully curled up in a cozy wooden wicker basket under a colorful patchwork quilt, tiny floating Zzz bubbles, warm soothing bedtime mood, isolated on white background --ar 1:1`

---

### Категория 2: Сказочные артефакты (Artifact Prompts)

- **Скатерть-самобранка**:
  ```text
  Magical self-spreading tablecloth game icon, neatly folded embroidered white linen cloth with red traditional Slavic geometric patterns, glowing golden threads, tiny steaming clay bowl of porridge and crisp red apple sitting on top, magical sparkles, 2D mobile game inventory icon, isolated on white background --ar 1:1
  ```
- **Склянка с живой водой**:
  ```text
  Fairytale glass vial of living water, antique faceted crystal potion flask with carved wooden stopper, filled with luminous glowing cyan-turquoise elixir, radiant magical sparkles and floating bubbles, fantasy game item icon, isolated on white background --ar 1:1
  ```
- **Путеводный клубок**:
  ```text
  Enchanted guiding yarn ball, glowing sphere of spun golden wool, unwinding a shimmering trail of golden light ribbon, soft whimsical luminescence, magical quest item icon, isolated on white background --ar 1:1
  ```
- **Богатырский щит**:
  ```text
  Heroic Slavic bogatyr wooden shield, round sturdy oak plank shield with forged iron rim and rivets, embossed brass radiant sun emblem in the center, heroic and protective game asset, isolated on white background --ar 1:1
  ```
- **Гусли-самогуды**:
  ```text
  Self-playing enchanted gusli, traditional carved Russian wooden winged psaltery instrument with taut bronze strings, subtle golden musical notes and sparkles floating around, warm mahogany wood, fantasy item icon, isolated on white background --ar 1:1
  ```
- **Расписной терем**:
  ```text
  Miniature fairy-tale wooden terem mansion icon, Russian traditional carved architecture with ornate window shutters, decorative rooftop horse finial, welcoming glowing lantern at the porch, whimsical storybook building icon, isolated on white background --ar 1:1
  ```
- **Сапоги-скороходы**:
  ```text
  Pair of enchanted seven-league boots, stylish crimson red saffian leather fairy-tale boots with curled pointed toes, golden embroidery, small delicate golden wings fluttering at the heels, isolated on white background --ar 1:1
  ```

---

### Категория 3: Сюжетные персонажи квестов (NPC Character Prompts)

- **Золотая рыбка**:
  ```text
  The Golden Fish character portrait, graceful magical fairytale goldfish swimming in sunlit pond water, tiny ornate golden crown perched on its head, shimmering iridescent golden scales, translucent flowing fins, friendly smiling face, water lilies in background, storybook illustration --ar 4:3
  ```
- **Морозко**:
  ```text
  Father Frost Morozko character portrait, kind elderly winter wizard with a long fluffy white beard and laughing friendly eyes, wearing a magnificent deep blue caftan coat lined with white fur and silver snowflakes, holding an ice crystal wooden staff, snowy fir trees background --ar 4:3
  ```
- **Раджа**:
  ```text
  Opulent merchant Raja character portrait, jovial plump eastern merchant with a trimmed mustache and jolly smile, wearing a lavish silk turban adorned with a turquoise gemstone and peacock feather, holding out a shiny jewel, vibrant market stall background --ar 4:3
  ```
- **Смекалистый мужик и барин**:
  ```text
  Clever peasant and wealthy barin, dual character portrait: a smart cunning rustic peasant in a simple embroidered linen tunic smiling cleverly, standing beside a pompous round nobleman in a velvet embroidered coat and fur hat, humorous folk storybook illustration --ar 4:3
  ```
- **Хитрый Лис**:
  ```text
  Cunning Fox merchant character portrait, dapper sly anthropomorphic red fox wearing a colorful embroidered merchant vest and a jaunty cap, fluffy tail curled up, sly charming smile, holding an ornate velvet box with a glowing golden seed, market crossroads background --ar 4:3
  ```

---

### Категория 4: Локации и фоны (Environments & Backgrounds)

- **Стартовый домик-избушка**:
  ```text
  Interior of a cozy rustic Slavic log cabin, warm sunlight streaming through a small window with patterned curtains, traditional white brick stove in the corner, simple wooden floor, soft braided rug, wooden bench, peaceful home atmosphere, 2D mobile game background illustration --ar 9:16
  ```
- **Расписной терем (прокачанный дом)**:
  ```text
  Interior of a magical royal wooden terem chamber, richly decorated with painted floral folk ornaments, tiled izraztsy fireplace stove, intricately carved arches and furniture, panoramic stained glass window, warm celebratory lighting, 2D mobile game background --ar 9:16
  ```
- **Интерактивная карта Тридевятого царства**:
  ```text
  Enchanted storybook world map illustration, parchment paper aesthetic, winding cobbled forest paths connecting 5 whimsical fairy-tale landmarks: a glowing lotus pond, a snowy winter grove, a colorful village fair, a rustic farmyard, and a crossroads with a stone signpost, isometric perspective, game overworld map --ar 9:16
  ```
- **Магазин и Стол Подорожника**:
  ```text
  Interior of a fairy-tale village merchant shop, cozy wooden counter with shelves displaying clay pots and wooden toys, dedicated apothecary corner with fresh green plantain leaves, glass herbal bottles, clean parchment scroll with a green leaf shield emblem, warm lanterns --ar 9:16
  ```

---

### Категория 5: Товары магазина и повседневные расходники (Shop Props)

- **Каша в горшочке (Надо)**:
  ```text
  Cute steaming clay pot of hot golden millet porridge, topped with a melting pat of golden butter, carved wooden spoon resting inside, appetizing and cozy, mobile game food icon, isolated on white background --ar 1:1
  ```
- **Лист подорожника (Страховка, Надо)**:
  ```text
  Magical healing plantain leaf icon, crisp fresh broad green leaf tied with a delicate golden ribbon, small green glowing shield charm attached, health insurance symbol for children, isolated on white background --ar 1:1
  ```
- **Деревянная лошадка (Хочу)**:
  ```text
  Traditional Russian wooden carved Dymkovo rocking horse toy, painted with bright red, yellow and blue geometric folk patterns, joyful and charming, toy item icon, isolated on white background --ar 1:1
  ```
- **Праздничная лента (Хочу)**:
  ```text
  Decorative festive silk ribbon spool, roll of bright red and gold ribbon adorned with folk embroidery, tied in a pretty bow, isolated on white background --ar 1:1
  ```

---

### Категория 6: Квестовые предметы и механики (Quest Elements)

- **Набор карточек ремонта (Рыбка)**:
  ```text
  Set of fairytale building materials: bundle of pine roof shingles, sturdy wooden bed with linen pillow, shiny royal golden crown, and garland of meadow flowers, clean game card props, isolated on white background --ar 1:1
  ```
- **Копилка Морозко (3 стадии)**:
  ```text
  Fairytale carved ice piggybank chest in three stages: empty crystalline box, half-filled with golden coins, and overflowing with coins radiating soft frost magic, isolated on white background --ar 1:1
  ```
- **Мешки с зерном (Мужик и барин)**:
  ```text
  Burlap sack of grain tied with rope, stamped with a golden wheat ear symbol, rustic sack prop, clean game asset, isolated on white background --ar 1:1
  ```
- **«Волшебное зёрнышко» Лиса**:
  ```text
  Enchanted golden seed resting on a tiny red velvet cushion inside an open carved wooden box, glowing with a suspicious bright yellow aura, fairytale prop, isolated on white background --ar 1:1
  ```
- **Пиктограммы подозрительных признаков**:
  ```text
  Set of 4 flat cartoon cautionary warning badges: stopwatch timer in flames (urgency), mountain of gold coins (unrealistic gain), inverted empty coin pouch (excessive cost), question mark scroll (lack of terms), clean vector badge style, isolated on white background --ar 1:1
  ```

---

### Категория 7: UI-элементы и валюта (UI Design System)

- **Золотая монета «Грошик»**:
  ```text
  Shiny golden cartoon coin icon, thick chunky edge, engraved with a cute stylized paw print and wheat grain, bright golden specular highlights, mobile game currency icon, isolated on white background --ar 1:1
  ```
- **Кошелёк**:
  ```text
  Rustic brown leather coin purse pouch, tied with a braided golden cord, bulging pleasantly with gold coins, isolated on white background --ar 1:1
  ```
- **Копилка**:
  ```text
  Cute ceramic savings piggy bank styled like a fairytale wooden chest with a coin slot on top, cheerful folk pattern, isolated on white background --ar 1:1
  ```
- **Иконки шкал сытости, радости и здоровья**:
  ```text
  Set of 3 mobile game stat icons: cute bowl of porridge (hunger), beaming happy sun with a smile (joy), green leaf with a red heart badge (health), bold outlines, flat shaded 2D icons on transparent background --ar 3:1
  ```
- **Иконки нижней навигации (4 шт.)**:
  ```text
  Set of 4 cartoon mobile navigation icons: cozy wooden cabin (Home), folded map with compass (Map), village awning shop stall (Shop), treasure chest piggy bank (Savings), minimal vector style with active colorful and inactive monochrome variants --ar 4:1
  ```

---

### Категория 8: Полноэкранные иллюстрации (Fullscreen Story Scenes)

- **Экран знакомства с книгой**:
  ```text
  Whimsical storybook opening illustration, a large antique fairy tale book opening with pages glowing with golden magical light, a tiny curious kitten-creature peeking out with wide amazed eyes, magical stardust in the air, heartwarming scene, storybook art --ar 9:16
  ```
- **Ночной экран итогов дня**:
  ```text
  Cozy night bedroom scene, little fairytale kitten sleeping peacefully tucked under a quilted patchwork blanket in a warm wooden loft, crescent moon and stars smiling through the window, night budget ledger scroll lying closed on a bedside stool with a single shiny gold coin --ar 9:16
  ```
- **Экран триумфа и победы**:
  ```text
  Celebration triumph scene, cheerful little cat jumping in joy amid flying colorful confetti, holding up an illuminated golden artifact, fireworks of golden sparks, joyous victory feeling, vibrant game illustration --ar 9:16
  ```
- **Грамота «Паспорт Хранителя»**:
  ```text
  Ornate fairytale Certificate of Financial Wisdom for children, Slavic decorative folk floral border, vintage parchment paper, seal stamp of the Wise Cat, ribbon medallion, elegant proud diploma design --ar 3:4
  ```

---

### Категория 9: Маркетинговые материалы RuStore (Marketing Assets)

- **Иконка приложения (512 × 512 px)**:
  ```text
  Mobile game app icon, close-up of a charming smiling cartoon cat character with bright green eyes and a neat folkloric scarf, holding a large sparkling golden coin, vibrant warm teal and gold background, modern rounded app icon framing, 3D-styled 2D render, high contrast, clean readable silhouette --ar 1:1
  ```
- **Промо-баннер (1024 × 500 px)**:
  ```text
  Panoramic horizontal banner for mobile game, little hero cat standing proudly in front of an enchanted wooden palace, surrounded by magical items (winged boots, glowing water flask, golden yarn), lush green fairytale hills under sunny blue sky, spacious layout suitable for text overlay --ar 2:1
  ```
