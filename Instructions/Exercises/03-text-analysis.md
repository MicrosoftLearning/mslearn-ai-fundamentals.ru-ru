---
lab:
  title: Анализ текста на портале Azure AI Foundry
---

# Анализ текста на портале Azure AI Foundry

Язык ИИ Azure включает Анализ текста с такими возможностями, как распознавание сущностей, извлечение ключевых фраз, сводка и анализ тональности. Например, предположим, что вымышленный агент по путешествиям Марги призывает клиентов отправлять отзывы о пребывании в отеле. Вы можете использовать языковую службу для извлечения именованных сущностей, определения ключевых фраз, суммирования текста и многого другого.

В этом упражнении вы будете использовать язык ИИ Azure на портале Azure AI Foundry, платформе Майкрософт для создания интеллектуальных приложений для анализа отзывов об отелях. 

Это упражнение занимает около **20** минут.

## Создание проекта на портале Azure AI Foundry

1. В веб-браузере откройте [портал](https://ai.azure.com) `https://ai.azure.com` Azure AI Foundry и войдите с помощью учетных данных Azure. Закройте все советы или панели быстрого запуска, открываемые при первом входе, и при необходимости используйте **логотип Azure AI Foundry** в левом верхнем углу, чтобы перейти на домашнюю страницу, которая выглядит следующим образом (закройте **панель справки** , если она открыта):

    ![Снимок экрана: домашняя страница портала Azure AI Foundry.](./media/ai-foundry-portal.png)

1. Прокрутите страницу до нижней части страницы и выберите плитку **"Обзор служб** ИИ Azure".

    ![Снимок экрана: плитка "Обзор служб ИИ Azure".](./media/ai-services.png)

1. На странице "Службы искусственного интеллекта Azure" выберите плитку **"Язык и переводчик** ".

    ![Снимок экрана: плитка Language + Translator.](./media/language-tile.png)

1. **На странице "Язык и переводчик"** выберите "**Попробовать языковую площадку**". Затем при появлении запроса создайте проект со следующими параметрами:
    - **Имя проекта: *введите допустимое имя** проекта.*
    - **Дополнительные параметры**:
        - **Подписка**: *ваша подписка Azure*
        - **Группа** ресурсов. *Создание или выбор группы ресурсов*
        - **Регион**: *выберите любой рекомендуемый** **регион AI Foundry*
        - **Ai Foundry или Azure OpenAI** *Create a new Azure AI Foundry resource with a valid name*

1. Нажмите кнопку **создания**. Дождитесь создания проекта. Это может занять несколько минут.

1. При создании проекта вы перейдете на языковую **** площадку (если нет, в области задач слева выберите **"Площадки**" и откройте языковую площадку.

    Языковая площадка — это пользовательский интерфейс, который позволяет попробовать некоторые возможности языка искусственного интеллекта Azure.  

## Использование языка ИИ Azure для анализа текста

Язык ИИ Azure предлагает широкий спектр возможностей анализа текста.

### Извлечение именованных сущностей с помощью языка ИИ Azure на портале Azure AI Foundry

*Именованные сущности* — это слова, описывающие людей, места и объекты с правильными именами. Давайте используем функцию извлечения именованных сущностей языка ИИ Azure, чтобы определить типы информации в обзоре.

1. На языковой площадке выберите **"Извлечь сведения**". Затем выберите плитку **"Извлечь именованные сущности** ". 

1. В разделе " *Пример"* введите следующую проверку:

    ```
    Tired hotel with poor service
    The Royal Hotel, London, United Kingdom
    5/6/2018
    This is an old hotel (has been around since 1950's) and the room furnishings are average - becoming a bit old now and require changing. The internet didn't work and had to come to one of their office rooms to check in for my flight home. The website says it's close to the British Museum, but it's too far to walk.
    ```

1. Выберите **Выполнить**. Просмотрите выходные данные.

    ![Снимок экрана: интерфейс извлечения именованных сущностей на языковой площадке.](./media/entity-extraction.png)

    Обратите внимание в *разделе сведений* о том, как извлеченные сущности содержат дополнительные сведения, такие как типы и оценки достоверности. Оценка достоверности представляет вероятность того, что тип, определенный фактически, принадлежит этой категории.

### Извлечение ключевых фраз с помощью языка ИИ Azure на портале Azure AI Foundry

*Ключевые фразы* являются наиболее важными фрагментами информации в тексте. Давайте используем возможность извлечения ключевых фраз языка ИИ Azure для извлечения важных сведений из обзора.

1. На языковой площадке выберите **"Извлечь сведения**". Затем выберите плитку **"Извлечь ключевые фразы** ". 

1. В разделе " *Пример"* введите следующую проверку:

    ```
    Good Hotel and staff
    The Royal Hotel, London, UK
    3/2/2018
    Clean rooms, good service, great location near Buckingham Palace and Westminster Abbey, and so on. We thoroughly enjoyed our stay. The courtyard is very peaceful and we went to a restaurant which is part of the same group and is Indian ( West coast so plenty of fish) with a Michelin Star. We had the taster menu which was fabulous. The rooms were very well appointed with a kitchen, lounge, bedroom and enormous bathroom. Thoroughly recommended.
    ```

1. Выберите **Выполнить**. Просмотрите выходные данные.

    ![Снимок экрана: интерфейс извлечения ключевых фраз на языковой площадке.](./media/key-phrases.png)

    Обратите внимание на различные фразы, извлеченные в *разделе сведений* . Эти фразы должны способствовать больше всего значению текста.

### Сводка текста с помощью языка ИИ Azure на портале Azure AI Foundry
 
Давайте рассмотрим возможности сводные данные языка ИИ Azure.

1. На игровой площадке языка выберите **"Сводка сведений**", а затем щелкните плитку **"Суммировать текст** ".

1. В разделе " *Пример"* введите следующую проверку:
    
    ```
    Very noisy and rooms are tiny
    The Lombard Hotel, San Francisco, USA
    9/5/2018
    Hotel is located on Lombard street which is a very busy SIX lane street directly off the Golden Gate Bridge. Traffic from early morning until late at night especially on weekends. Noise would not be so bad if rooms were better insulated but they are not. Had to put cotton balls in my ears to be able to sleep--was too tired to enjoy the city the next day. Rooms are TINY. I picked the room because it had two queen size beds--but the room barely had space to fit them. With family of four in the room it was tight. With all that said, rooms are clean and they've made an effort to update them. The hotel is in Marina district with lots of good places to eat, within walking distance to Presidio. May be good hotel for young stay-up-late adults on a budget
    ```

1. Выберите **Выполнить**. Просмотрите выходные данные.

    ![Снимок экрана: текстовый интерфейс "Сводка" на языковой площадке.](./media/summarize-text.png)

    Обратите внимание, что *сводка* по извлечению данных содержит ** оценки ранжирования для наиболее важных предложений.

### Анализ тональности в тексте

Анализ тональности является общей задачей при анализе текста, например отзывов о отелях.

1. На детской площадке языка выберите **классифицировать текст**. Затем выберите плитку **"Анализ тональности** ".

1. В разделе " *Пример"* введите следующую проверку:
    
    ```
    Disappointing Stay at The City Hotel
    The City Hotel, London
    9/5/2018
    My experience at The City Hotel in London was far from pleasant. The constant noise from nearby train tracks made it nearly impossible to sleep, with vibrations felt throughout the building. The rooms were outdated, dusty, and poorly maintained—dripping faucets, squeaky beds, and broken fixtures were just the beginning. Sound insulation was nonexistent, so every conversation from neighboring rooms was clearly audible. While the location near public transport was convenient and the staff were friendly, these positives couldn't make up for the overall discomfort and lack of value. I wouldn’t recommend this hotel to anyone seeking a restful or enjoyable stay.
    ```

1. Выберите **Выполнить**. Просмотрите выходные данные.

    ![Снимок экрана: интерфейс анализа Seniment на языковой площадке.](./media/sentiment-analysis.png)

    Обратите внимание, что анализ создает общую оценку тональности и отдельные оценки для каждого предложения.

## Обнаружение языка и перевод текста

Язык ИИ Azure позволяет обнаруживать язык, на котором написан текст. Кроме того, Azure AI Translator позволяет легко переводить текст с одного языка на другой.

### Определение языка

Начнем с определения языка, в который написана проверка.

1. **В области "Классифицировать текст**" выберите плитку **"Определить язык**".

1. В разделе " *Пример"* введите следующую проверку:
    
    ```
    Un séjour mémorable à l’Hôtel d’Ville
    l’Hôtel d’Ville, Paris
    9/5/2018
    J’ai passé un excellent séjour à l’Hôtel d’Ville à Paris. L’emplacement est idéal, en plein cœur de la ville, ce qui permet de découvrir facilement les principaux sites touristiques. Le personnel était chaleureux, professionnel et toujours prêt à aider. La chambre était propre, confortable et bien équipée, avec une vue charmante sur les rues parisiennes. Le petit-déjeuner était varié et délicieux, parfait pour commencer la journée. Je recommande vivement cet hôtel à tous ceux qui recherchent une expérience parisienne authentique et agréable.
    ```

1. Выберите **Выполнить**. Просмотрите выходные данные.

    ![Снимок экрана: интерфейс обнаружения языка на детской площадке языка.](./media/detect-language.png)

    Обратите внимание, что язык обнаруживается как французский. 

### Перевод текста

Теперь давайте переводим французский обзор на английский.

1. В верхней части страницы используйте ссылку (назад) рядом **&larr;** с заголовком страницы языковой площадки** eht**, чтобы просмотреть все доступные игровые площадки.
1. В списке игровых площадок откройте детскую площадку **** Переводчика.
1. На игровой площадке переводчика выберите **"** Перевод текста".
1. **В области "Настройка"** выберите следующие языковые параметры:
    - **Перевод с французского языка**
    - **Перевод на**: английский
1. В разделе "Пример *"* введите проверку на французском языке:
    
    ```
    Un séjour mémorable à l’Hôtel d’Ville
    l’Hôtel d’Ville, Paris
    9/5/2018
    J’ai passé un excellent séjour à l’Hôtel d’Ville à Paris. L’emplacement est idéal, en plein cœur de la ville, ce qui permet de découvrir facilement les principaux sites touristiques. Le personnel était chaleureux, professionnel et toujours prêt à aider. La chambre était propre, confortable et bien équipée, avec une vue charmante sur les rues parisiennes. Le petit-déjeuner était varié et délicieux, parfait pour commencer la journée. Je recommande vivement cet hôtel à tous ceux qui recherchent une expérience parisienne authentique et agréable.
    ```

1. Выберите **"Перевод**". Просмотрите выходные данные.

    ![Снимок экрана: интерфейс преобразования текста на игровой площадке Переводчика.](./media/text-translation.png)

    Обратите внимание, что французский обзор переведен на английский.

## Очистка

Если вы не собираетесь выполнять больше упражнений, удалите все ресурсы, которые больше не нужны. Это позволяет избежать каких-либо ненужных затрат.

1. **Откройте портал Azurehttps://portal.azure.com** [](https://portal.azure.com) и выберите группу ресурсов, содержащую созданные ресурсы.
1. Выберите **"Удалить группу ресурсов", а затем **введите имя** группы** ресурсов, чтобы подтвердить. Затем группа ресурсов удаляется.

## Подробнее

Дополнительные сведения о том, что можно сделать с помощью этой службы, см. на [странице языковой службы](https://learn.microsoft.com/azure/ai-services/language-service/overview).
