---
lab:
  title: Анализ текста на портале Azure AI Foundry
---

# Анализ текста на портале Azure AI Foundry

Обработка естественного языка (NLP) — это ветвь ИИ, которая занимается письменным и речным языком. Вы можете использовать NLP для создания решений, которые извлекают семантические значения из текста или речи или формулируют значимые ответы на естественном языке.

Служба языка искусственного интеллекта Azure включает Анализ текста с такими возможностями, как распознавание сущностей, извлечение ключевых фраз, сводка и анализ тональности. Например, предположим, что вымышленный агент по путешествиям Марги призывает клиентов отправлять отзывы о пребывании в отеле. Вы можете использовать языковую службу для извлечения именованных сущностей, определения ключевых фраз, суммирования текста и многого другого.

В этом упражнении вы будете использовать язык ИИ Azure на портале Azure AI Foundry, платформе Майкрософт для создания интеллектуальных приложений для анализа отзывов об отелях. 

## Создание проекта на портале Azure AI Foundry

1. В веб-браузере откройте [портал](https://ai.azure.com) `https://ai.azure.com` Azure AI Foundry и войдите с помощью учетных данных Azure. Закройте все советы или панели быстрого запуска, открываемые при первом входе. 

1. В браузере перейдите к разделу и нажмите кнопку `https://ai.azure.com/managementCenter/allResources` **"Создать**". Затем выберите параметр для создания *нового ресурса* Azure AI Foundry.

1. В мастере *создания проекта* введите допустимое имя проекта.

1. Разверните *дополнительные параметры* , чтобы указать следующие параметры для проекта:
    - **Подписка**: ваша подписка Azure.
    - **Группа** ресурсов. Создание или выбор группы ресурсов
    - **Регион**: выберите одно из следующих расположений:
        * Восточная часть США
        * Центральная Франция
        * Республика Корея, центральный регион
        * Западная Европа
        * западная часть США

    Дождитесь создания проекта и центра.

1. При создании проекта вы перейдете на страницу *обзора* сведений о проекте.

1. В меню слева на экране выберите **"Игровые площадки**".

1. *На странице "Игровые площадки"* выберите плитку **"Языковая площадка**", чтобы попробовать некоторые возможности языка искусственного интеллекта Azure.

## Извлечение именованных сущностей с помощью языка ИИ Azure на портале Azure AI Foundry

*Именованные сущности* — это слова, описывающие людей, места и объекты с правильными именами. Давайте используем функцию извлечения именованных сущностей языка ИИ Azure, чтобы определить типы информации в обзоре.

1. На языковой площадке выберите **"Извлечь сведения**". Затем выберите плитку **"Извлечь именованные сущности** ". 

1. В разделе " *Пример"* скопируйте и вставьте следующую проверку:

    ```
    Tired hotel with poor service
    The Royal Hotel, London, United Kingdom
    5/6/2018
    This is an old hotel (has been around since 1950's) and the room furnishings are average - becoming a bit old now and require changing. The internet didn't work and had to come to one of their office rooms to check in for my flight home. The website says it's close to the British Museum, but it's too far to walk.
    ```

1. Выберите **Выполнить**. Просмотрите выходные данные. Обратите внимание в *разделе сведений* о том, как извлеченные сущности содержат дополнительные сведения, такие как типы и оценки достоверности. Оценка достоверности представляет вероятность того, что тип, определенный фактически, принадлежит этой категории.

## Извлечение ключевых фраз с помощью языка ИИ Azure на портале Azure AI Foundry

*Ключевые фразы* являются наиболее важными фрагментами информации в тексте. Давайте используем возможность извлечения ключевых фраз языка ИИ Azure для извлечения важных сведений из обзора.

1. На языковой площадке выберите **"Извлечь сведения**". Затем выберите плитку **"Извлечь ключевые фразы** ". 

1. В разделе " *Пример"* скопируйте и вставьте следующую проверку:

    ```
    Good Hotel and staff
    The Royal Hotel, London, UK
    3/2/2018
    Clean rooms, good service, great location near Buckingham Palace and Westminster Abbey, and so on. We thoroughly enjoyed our stay. The courtyard is very peaceful and we went to a restaurant which is part of the same group and is Indian ( West coast so plenty of fish) with a Michelin Star. We had the taster menu which was fabulous. The rooms were very well appointed with a kitchen, lounge, bedroom and enormous bathroom. Thoroughly recommended.
    ```

1. Выберите **Выполнить**. Просмотрите выходные данные. Обратите внимание на различные фразы, извлеченные в *разделе сведений* . Эти фразы должны способствовать больше всего значению текста.

## Сводка текста с помощью языка ИИ Azure на портале Azure AI Foundry
 
1. Давайте рассмотрим возможности сводные данные языка ИИ Azure. На игровой площадке языка выберите *"Сводка сведений*", а затем щелкните плитку **"Суммировать текст** ".

1. В разделе " *Пример"* скопируйте и вставьте следующую проверку:
    
    ```
    Very noisy and rooms are tiny
    The Lombard Hotel, San Francisco, USA
    9/5/2018
    Hotel is located on Lombard street which is a very busy SIX lane street directly off the Golden Gate Bridge. Traffic from early morning until late at night especially on weekends. Noise would not be so bad if rooms were better insulated but they are not. Had to put cotton balls in my ears to be able to sleep--was too tired to enjoy the city the next day. Rooms are TINY. I picked the room because it had two queen size beds--but the room barely had space to fit them. With family of four in the room it was tight. With all that said, rooms are clean and they've made an effort to update them. The hotel is in Marina district with lots of good places to eat, within walking distance to Presidio. May be good hotel for young stay-up-late adults on a budget
    ```

1. Выберите **Выполнить**. Просмотрите выходные данные. Обратите внимание, что *сводка* по извлечению данных содержит ** оценки ранжирования для наиболее важных предложений.   

## Очистка

Если вы не собираетесь выполнять больше упражнений, удалите все ресурсы, которые больше не нужны. Это позволяет избежать каких-либо ненужных затрат.

1. **Откройте портал Azurehttps://portal.azure.com** [](https://portal.azure.com) и выберите группу ресурсов, содержащую созданные ресурсы.

1. Выберите ресурсы и нажмите кнопку **"Удалить** ", а затем **"Да** ", чтобы подтвердить. Затем ресурсы удаляются.

## Подробнее

Дополнительные сведения о том, что можно сделать с помощью этой службы, см. на [странице языковой службы](https://learn.microsoft.com/azure/ai-services/language-service/overview).
