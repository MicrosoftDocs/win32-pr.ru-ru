---
title: Сравнение подробной модели объектов
description: Сравнение подробной модели объектов
ms.assetid: 8f08e2a6-1944-4814-b3b7-680a3722e1a0
keywords:
- Проигрыватель Windows Media, объектная модель
- Объектная модель проигрывателя Windows Media, отличия версий
- Объектная модель, различия версий
- Элемент управления ActiveX проигрывателя Windows Media, различия версий
- Элемент управления ActiveX, различия версий
- Элемент управления ActiveX мобильных устройств проигрывателя Windows Media, различия версий
- Проигрыватель Windows Media Mobile, объектная модель
- рекомендации по миграции, отличия версий
- версии проигрывателя Windows Media, объектная модель
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086607a9d367f42479e155e3273c30d88425a457
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "104069513"
---
# <a name="detailed-object-model-comparison"></a>Сравнение подробной модели объектов

В следующей таблице сравниваются свойства объектной модели проигрывателя Windows Media 6,4 с объектной моделью проигрывателя Windows Media 7 или более поздней версии.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Свойство проигрывателя Windows Media 6,4</th>
<th>Проигрыватель Windows Media 7 или более поздней версии</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>. <strong>Алловчанжедисплайсизе</strong></td>
<td>При отображении проигрывателя Windows Media 7 или более поздней версии автоматически изменяется размер по размеру носителя. Свойства высоты и ширины можно задать в <OBJECT> теге или в скрипте.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Алловскан</strong></td>
<td><em>Элементы управления</em>. <strong>фастфорвард</strong> и <em>элементы управления</em>. <strong>фастреверсе</strong> автоматически включаются для типов файлов, поддерживающих эти методы.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Англесаваилабле</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Аниматионатстарт</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Аудиостреам</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>куррентаудиолангуажеиндекс</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Аудиостреамсаваилабле</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>аудиолангуажекаунт</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Ауторевинд</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>CurrentPosition</strong> в скрипте для указания или получения текущей позицией. Кроме того, можно использовать маркеры и <em>проигрыватель</em>. событие <strong>маркерхит</strong> .</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Автоподбор размеров</strong></td>
<td>Поведение по умолчанию — автоматическое изменение размера. Чтобы переопределить автоматическое изменение размера, задайте свойства Height и Width в <OBJECT> теге или в скрипте.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Автозапуск</strong></td>
<td>Используйте <em>Параметры</em>. <strong>Автозапуск</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Сбалансировать</strong></td>
<td>Используйте <em>Параметры</em>. <strong>баланс</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Пропускная способность</strong></td>
<td>Использовать <em>сеть</em>. <strong>пропускная способность</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>BaseURL</strong></td>
<td>Используйте <em>Параметры</em>. <strong>baseURL</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Буфферингкаунт</strong></td>
<td>Использовать <em>сеть.</em> <strong>буфферингкаунт</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Буфферингпрогресс</strong></td>
<td>Использовать <em>сеть</em>. <strong>буфферингпрогресс</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Буфферингтиме</strong></td>
<td>Использовать <em>сеть</em>. <strong>буфферингтиме</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Буттонсаваилабле</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Канпревиев</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Канскан</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>Available</strong>( &quot; Фастфорвард &quot; ) и <em>Controls</em>.<strong> Доступно</strong>( &quot; фастреверсе &quot; ).</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CanSeek</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>доступно</strong> для проверки возможности выполнения конкретного метода Seek.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Кансиктомаркерс</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>доступно</strong>( &quot; куррентмаркер &quot; ). Используйте <em>носитель</em>. <strong>маркеркаунт</strong> для получения числа маркеров в определенном элементе мультимедиа. Используйте <em>элементы управления</em>. <strong>куррентмаркер</strong> , чтобы указать или получить номер текущего маркера.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Каптионингид</strong></td>
<td>Используйте <em>клоседкаптион</em>. <strong>каптионингид</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Ккактиве</strong></td>
<td>Недоступно. Дополнительные сведения об изменении субтитров в проигрывателе Windows Media см. в разделе <a href="closed-captioning.md">Скрытые титры</a> .</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ChannelDescription</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ChannelName</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Чаннелурл</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Кликктоплай</strong></td>
<td>Недоступно. Для запуска воспроизведения необходимо предоставить элементы управления в пользовательском интерфейсе. Кроме того, пользователь может щелкнуть изображение видео правой кнопкой мыши, чтобы открыть всплывающее меню, содержащее выбор <strong>воспроизведения и паузы</strong> при открытии <em>проигрывателя</em>. <strong>енаблеконтекстмену</strong> имеет значение true.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ClientID</strong></td>
<td>Недоступно. Проигрыватель Windows Media 9 Series или более поздней версии позволяет пользователю выбрать, следует ли передавать уникальный идентификатор проигрывателя поставщикам содержимого.<br/> Если пользователь выбирает этот параметр, проигрыватель отправляет уникальный идентификатор на сервер Windows Media. Идентификатор заносится в файл журнала сервера, расположенный в папке. папка <em>system32\logfiles</em> по умолчанию. Имя поля журнала — &quot; c-плайерид &quot; . Ведение журнала сервера не включено по умолчанию в службах Windows Media.<br/> Если пользователь не выбирает этот параметр, сервер создает случайный идентификатор сеанса, уникальный для каждого клиента в данном сеансе.<br/> Дополнительные сведения см. в документации по сериям Windows Media Services 9.<br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Кодеккаунт</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ColorKey</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Коннектионспид</strong></td>
<td>Недоступно. Использовать <em>сеть</em>. <strong>скорость</strong> для определения текущей скорости.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Контактаддресс</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Контактемаил</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Контактфоне</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>CreationDate</strong></td>
<td>Используйте <em>медиаколлектион</em>. <strong>жетмедиаатом</strong>( &quot; CreationDate &quot; ) для получения индекса Atom даты создания. Используйте <em>носитель</em>. <strong>жетитеминфобятом</strong> получить метаданные.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Куррентангле</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Куррентаудиостреам</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>куррентаудиолангуажеиндекс</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Куррентбуттон</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Курренткксервице</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Куррентчаптер</strong></td>
<td>Получение текущего списка воспроизведения. Если текущий список воспроизведения не совпадает с списком воспроизведения, возвращенным <em>CDROM</em>. <strong>списка воспроизведения</strong>нет текущей главы. В противном случае текущий номер главы — это индекс текущего носителя в текущем списке воспроизведения.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Куррентдисксиде</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentDomain</strong></td>
<td>Используйте <em>DVD-диск</em>. <strong>домен</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Куррентмаркер</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>куррентмаркер</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentPosition</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>CurrentPosition</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Куррентсубпиктурестреам</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>CurrentTime</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>куррентпоситионтимекоде</strong>, <em>элементы управления</em>. <strong>куррентпоситионстринг</strong>или <em>элементы управления</em>. <strong>CurrentPosition.</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Курренттитле</strong></td>
<td>Получение текущего списка воспроизведения. Если текущий список воспроизведения совпадает с списком воспроизведения, возвращенным <em>CDROM</em>. <strong>список воспроизведения</strong>, а номер заголовка — это индекс текущего носителя в текущем списке воспроизведения.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Куррентволуме</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Примеры CursorType</strong></td>
<td>Недоступно. Вместо этого используйте стили Internet Explorer.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Дефаултфраме</strong></td>
<td>Используйте <em>Параметры</em>. <strong>дефаултфраме</strong>или используйте <PARAM> атрибут в <OBJECT> элементе: <pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Дисплайбаккколор</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Дисплайфореколор</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>DisplayMode</strong></td>
<td>Текущую точку можно получить в секундах с начала в виде <strong>числа</strong> с помощью <em>элементов управления</em>. <strong>CurrentPosition</strong>в виде <strong>строки</strong> в формате чч: мм: СС (часы, минуты, секунды) с помощью <em>элементов управления</em>. <strong>куррентпоситионстринг</strong>или в формате кода времени с помощью <em>элементов управления</em>. <strong>куррентпоситионтимекоде</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Дисплайсизе</strong></td>
<td>Изображение по умолчанию автоматически изменяется в соответствии с размером носителя. Можно задать свойства Height и Width в <OBJECT> теге или в скрипте. Используйте <em>проигрыватель</em>. <strong>полноэкранный</strong> режим, переключаясь в весь экран.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Длительность</strong></td>
<td>Используйте <em>носитель</em>. <strong>Длительность</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>DVD-диск</strong></td>
<td>Используйте <em>проигрыватель</em>. <strong>DVD-диск</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Енаблеконтекстмену</strong></td>
<td>Используйте <em>проигрыватель</em>. <strong>енаблеконтекстмену</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Включено</strong></td>
<td>Используйте <em>проигрыватель</em>. <strong>включено</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Енаблефуллскринконтролс</strong></td>
<td>При использовании проигрывателя Windows Media 9 Series или более поздних версий элементы управления для полноэкранного режима включаются автоматически, если <em>проигрыватель</em>не используется. <strong></strong>  =  uiMode &quot; нет &quot; .</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Енаблепоситионконтролс</strong></td>
<td>Недоступно. Вы можете предоставить настраиваемые элементы управления или использовать <em>проигрыватель</em>. <strong>UIMODE</strong> , чтобы выбрать конфигурацию по умолчанию.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Енаблетраккер</strong></td>
<td>Недоступно. Вы можете предоставить пользовательский элемент управления или использовать <em>проигрыватель</em>. <strong>UIMODE</strong> , чтобы выбрать конфигурацию по умолчанию.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Ентрикаунт</strong></td>
<td>Использовать <em>список воспроизведения</em>. <strong>количество</strong></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Код ошибки</strong></td>
<td>Используйте <em>ерроритем</em>. <strong>код ошибки</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Ерроркорректион</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ErrorDescription</strong></td>
<td>Используйте <em>ерроритем</em>. <strong>errorDescription</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Имя файла</strong></td>
<td>Используйте <em>проигрыватель</em>. <strong>URL-адрес</strong> или <em>проигрыватель</em>. <strong>куррентмедиа</strong>. Используйте <em>элементы управления</em>. <strong>currentItem</strong> при работе в списке воспроизведения.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Фрамесперсеконд</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>HasError</strong></td>
<td>Использовать <em>ошибку</em>. <strong>ерроркаунт</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Хасмултиплеитемс</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Имажесаурцехеигхт</strong></td>
<td>Используйте <em>носитель</em>. <strong>имажесаурцехеигхт</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Имажесаурцевидс</strong></td>
<td>Используйте <em>носитель</em>. <strong>имажесаурцевидс</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Инвокеурлс</strong></td>
<td>Используйте <em>Параметры</em>. <strong>инвокеурлс</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Трансляция</strong></td>
<td>Использовать <em>сеть</em>. <strong>саурцепротокол</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Исдуратионвалид</strong></td>
<td>Недоступно. <em>Носитель</em>. параметр <strong>Duration</strong> содержит допустимое значение при использовании с текущим объектом мультимедиа.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Языковая</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>куррентаудиолангуаже</strong></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Лостпаккетс</strong></td>
<td>Использовать <em>сеть</em>. <strong>лостпаккетс</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Маркеркаунт</strong></td>
<td>Используйте <em>носитель</em>. <strong>маркеркаунт</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Отключить звук</strong></td>
<td>Используйте <em>Параметры</em>. <strong>Отключить звук</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Опенстате</strong></td>
<td>Используйте <em>проигрыватель</em>. <strong>опенстате</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Плайкаунт</strong></td>
<td>Используйте <em>Параметры</em>. <strong>плайкаунт</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Плайстате</strong></td>
<td>Используйте <em>проигрыватель</em>. <strong>плайстате</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>PreviewMode</strong></td>
<td>Недоступно. Используйте структуру цикла скриптов с таймером HTML для дублирования этой функции.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Скорость передачи</strong></td>
<td>Используйте <em>Параметры</em>. <strong>ставка</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ReadyState</strong></td>
<td>Используйте <em>проигрыватель</em>. <strong>опенстате</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Рецеиведпаккетс</strong></td>
<td>Использовать <em>сеть</em>. <strong>рецеиведпаккетс</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Рецептионкуалити</strong></td>
<td>Использовать <em>сеть</em>. <strong>рецептионкуалити</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Рековередпаккетс</strong></td>
<td>Использовать <em>сеть</em>. <strong>рековередпаккетс</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Корневая папка</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Самифиленаме</strong></td>
<td>Используйте <em>клоседкаптион</em>. <strong>Самифиленаме</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Самиланг</strong></td>
<td>Используйте <em>клоседкаптион</em>. <strong>Самиланг</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Самистиле</strong></td>
<td>Используйте <em>клоседкаптион</em>. <strong>Самистиле</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Селектионенд</strong></td>
<td>Используйте <em>носитель</em>. <strong>Длительность</strong> для определения длины объекта <strong>мультимедиа</strong> . Используйте маркер с <em>элементами управления</em>. <strong>куррентмаркер</strong> , чтобы указать пользовательскую конечную точку.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Селектионстарт</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>CurrentPosition</strong> , чтобы начать воспроизведение из определенной должности или использовать маркер с <em>элементами управления</em>. <strong>куррентмаркер</strong> , чтобы указать пользовательскую начальную точку.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Сендерроревентс</strong></td>
<td>Ошибки помещаются в очередь. Для получения сведений об ошибке используйте объект <strong>Error</strong> и объект <strong>ерроритем</strong> .</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Сендкэйбоардевентс</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Сендмаусекликкевентс</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Сендмаусемовивентс</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Сендопенстатечанжеевентс</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Сендплайстатечанжеевентс</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Сендварнинжевентс</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Шоваудиоконтролс</strong></td>
<td>Недоступно. Вы можете предоставить настраиваемые элементы управления или использовать <em>проигрыватель</em>. <strong>UIMODE</strong> , чтобы выбрать конфигурацию по умолчанию.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Шовкаптионинг</strong></td>
<td>Недоступно. Можно задать пользовательский вывод закрытого заголовка.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Шовконтролс</strong></td>
<td>Недоступно. Вы можете предоставить настраиваемые элементы управления или использовать <em>проигрыватель</em>. <strong>UIMODE</strong> , чтобы выбрать конфигурацию по умолчанию.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Шовдисплай</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Шовготобар</strong></td>
<td>Недоступно. С помощью объекта мультимедиа можно предоставить пользовательские функции.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Шовпоситионконтролс</strong></td>
<td>Недоступно. Вы можете предоставить настраиваемые элементы управления или использовать <em>проигрыватель</em>. <strong>UIMODE</strong> , чтобы выбрать конфигурацию по умолчанию.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Шовстатусбар</strong></td>
<td>Недоступно. Вы можете предоставить настраиваемые элементы управления или использовать <em>проигрыватель</em>. <strong>UIMODE</strong> , чтобы выбрать конфигурацию по умолчанию.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Шовтраккер</strong></td>
<td>Недоступно. Вы можете предоставить настраиваемые элементы управления или использовать <em>проигрыватель</em>. <strong>UIMODE</strong> , чтобы выбрать конфигурацию по умолчанию.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>SourceLink</strong></td>
<td>Используйте <em>носитель</em>. <strong>саурцеурл</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Саурцепротокол</strong></td>
<td>Использовать <em>сеть</em>. <strong>саурцепротокол</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Стреамкаунт</strong></td>
<td>Недоступно. Используйте <em>элементы управления</em>. <strong>аудиолангуажекаунт</strong> для получения числа потоков звукового языка.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Субпиктуреон</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Субпиктурестреамсаваилабле</strong></td>
<td>Недоступно</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Титлесаваилабле</strong></td>
<td>Используйте следующую команду:<code>Player.Cdrom.playlist.count - 1</code><br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Тоталтитлетиме</strong></td>
<td>Используйте <em>куррентмедиа</em>. <strong>Duration</strong> или <em>куррентмедиа</em>. <strong>дуратионстринг</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Транспарентатстарт</strong></td>
<td>Используйте скрипт, чтобы задать значения высоты и ширины, чтобы сделать проигрыватель видимым или невидимым.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>UniqueID</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>VideoBorder3D</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Видеобордерколор</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Видеобордервидс</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Том</strong></td>
<td>Используйте <em>Параметры</em>. <strong>Том</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Волумесаваилабле</strong></td>
<td>Недоступно.</td>
</tr>
</tbody>
</table>



 

В следующей таблице сравниваются методы объектной модели проигрывателя Windows Media версии 6,4 с объектной моделью проигрывателя Windows Media 7 или более поздней версии.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Метод проигрывателя Windows Media 6,4</th>
<th>Проигрыватель Windows Media 7 или более поздней версии</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Player6</em>. <strong>AboutBox</strong></td>
<td>Используйте <em>проигрыватель</em>. <strong>versionInfo</strong> для получения версии проигрывателя Windows Media.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Бакквардскан</strong></td>
<td>Используйте <em>Параметры</em>. <strong>ставка</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Буттонактивате</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Буттонселектандактивате</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Отмена</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Чаптерплай</strong></td>
<td>Если вы уже воспроизводили указанный список воспроизведения заголовков, извлеките нужную главу в виде объекта мультимедиа, используя следующий синтаксис:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Затем укажите <em>Player</em>. <strong>куррентмедиа</strong> с использованием возвращенного объекта мультимедиа.<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Чаптерплайаутостоп</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Чаптерсеарч</strong></td>
<td>Если вы уже воспроизводили указанный список воспроизведения заголовков, извлеките нужную главу в виде объекта мультимедиа, используя следующий синтаксис:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Затем укажите <em>Player</em>. <strong>куррентмедиа</strong> с использованием возвращенного объекта мультимедиа.<br/></td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Фастфорвард</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>фастфорвард</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Фастреверсе</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>фастреверсе</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Форвардскан</strong></td>
<td>Используйте <em>Параметры</em>. <strong>ставка</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Жеталлгпрмс</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Жеталлспрмс</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Жетаудиолангуаже</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>куррентаудиолангуаже</strong> получить код языка текущего аудио языка.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Жеткодекдескриптион</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>ЖеткодеЦинсталлед</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Жеткодекурл</strong></td>
<td>Используйте <em>ерроритем</em>. <strong>кустомурл</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Жеткуррентентри</strong></td>
<td>Используйте скрипт для прохода по текущему списку воспроизведения. Используйте <em>носитель</em>. « <strong>идентично</strong> » для сравнения каждой записи в списке воспроизведения с <em>проигрывателем</em>. Объект <strong>куррентмедиа</strong> .</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Жетмаркернаме</strong></td>
<td>Используйте <em>носитель</em>. <strong>жетмаркернаме</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Жетмаркертиме</strong></td>
<td>Используйте <em>носитель</em>. <strong>жетмаркертиме</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Жетмедиаинфостринг</strong></td>
<td>Используйте <em>носитель</em>. <strong>getItemInfo</strong>, <em>Media</em>. <strong>жетитеминфобятом</strong>и связанные с ними методы для получения метаданных.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Жетмедиапараметер</strong></td>
<td>Использовать <em>список воспроизведения</em>. <strong>элемент</strong> , который извлекает элемент мультимедиа. Затем используйте <em>носитель</em>. <strong>getItemInfo</strong> для получения строки параметра.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Жетмедиапараметернаме</strong></td>
<td>Использовать <em>список воспроизведения</em>. <strong>элемент</strong> , который извлекает элемент мультимедиа. Затем используйте <em>носитель</em>. <strong>жетаттрибутенаме</strong> для получения строки параметра.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Жетмореинфаурл</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Жетнумберофчаптерс</strong></td>
<td>Если в данный момент заголовок воспроизводится, используйте <em>куррентплайлист</em>. <strong>количество</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Жетстреамграуп</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Жетстреамнаме</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Жетстреамселектед</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Жетсубпиктурелангуаже</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Группы</strong></td>
<td>Используйте <em>DVD-диск</em>. <strong>назад</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Иссаундкарденаблед</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Лефтбуттонселект</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Ловербуттонселект</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Менукалл</strong></td>
<td>Используйте <em>DVD-диск</em>. <strong>титлемену</strong> или <em>DVD</em>. <strong>топмену</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Далее</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>Далее</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Некстпгсеарч</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>Далее</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Открыть</strong></td>
<td>Используйте <em>проигрыватель</em>. <strong>URL-адрес</strong> или <em>проигрыватель</em>. <strong>куррентмедиа</strong>. Файлы всегда открываются асинхронно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Приостановить</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>приостановить</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Воспроизвести</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>воспроизвести</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Предыдущий</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>назад</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Превпгсеарч</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>назад</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Ресумефроммену</strong></td>
<td>Используйте <em>DVD-диск</em>. <strong>возобновить</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Ригхтбуттонселект</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Сеткуррентентри</strong></td>
<td>Получите объект мультимедиа с помощью <em>куррентплайлист</em>. <strong>Item</strong>(<em>ентринумбер</em>). Затем укажите полученный объект мультимедиа с помощью <em>элементов управления</em>. <strong>currentItem</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>ShowDialog</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Стиллофф</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>воспроизвести</strong>. Кроме того, можно использовать <em>элементы управления</em>. <strong>Далее</strong> , если сейчас находится в режиме.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Завершение</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>останавливается</strong>.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Стреамселект</strong></td>
<td>Недоступно. Используйте <em>элементы управления</em>. <strong>куррентаудиолангуаже</strong> , чтобы указать поток на звуковом языке.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Тимеплай</strong></td>
<td>В корневом списке воспроизведения используйте <em>куррентплайлист</em>. <strong>элемент</strong>(<em>индекс</em>) для получения объекта мультимедиа. Затем установите объект мультимедиа в качестве текущего объекта с помощью <em>элементов управления</em>. <strong>currentItem</strong>. Затем укажите <em>элементы управления</em>. <strong>CurrentPosition</strong> , используя значение времени в секундах.</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Тимесеарч</strong></td>
<td>Используйте <em>элементы управления</em>. <strong>CurrentPosition</strong>.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Титлеплай</strong></td>
<td>Если вы уже воспроизводили указанный список воспроизведения заголовков, извлеките нужную главу в виде объекта мультимедиа, используя следующий синтаксис:
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
Затем укажите <em>Player</em>. <strong>куррентмедиа</strong> с использованием возвращенного объекта мультимедиа.<br/> Кроме того, можно использовать <em>куррентплайлист</em>. <strong>элемент</strong> для получения объекта мультимедиа, а затем используйте возвращаемый объект мультимедиа для указания <em>элементов управления</em>. <strong>currentItem</strong>.<br/></td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Топпгсеарч</strong></td>
<td>Недоступно.</td>
</tr>
<tr class="odd">
<td><em>Player6</em>. <strong>Уопвалид</strong></td>
<td>Недоступно</td>
</tr>
<tr class="even">
<td><em>Player6</em>. <strong>Уппербуттонселект</strong></td>
<td>Недоступно.</td>
</tr>
</tbody>
</table>



 

В следующей таблице сравниваются события объектной модели проигрывателя Windows Media версии 6,4 с объектной моделью проигрывателя Windows Media 7 или более поздней версии.



| Событие проигрывателя Windows Media 6,4  | Проигрыватель Windows Media 7 или более поздней версии                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Player6*. **Буферизация**         | Используйте *проигрыватель*. **Буферизация**.                                                                                                                                                                                              |
| *Player6*. **Нажмите кнопку**             | Используйте *проигрыватель*. **Нажмите кнопку**                                                                                                                                                                                                   |
| *Player6*. **Двойное** нажатие          | Используйте *проигрыватель*. **DoubleClick**                                                                                                                                                                                             |
| *Player6*. **Отключиться**        | Недоступно.                                                                                                                                                                                                           |
| *Player6*. **Дисплаймодечанже** | Недоступно.                                                                                                                                                                                                           |
| *Player6*. **Двднотифи**         | *Проигрыватель*. **Домаинчанже** и *Player*. **Опенплайлистсвитч** — это события, связанные с DVD-дисками. Кроме того, в зависимости от приложения могут применяться и другие события, связанные с списками воспроизведения, носителями и носителями компакт-дисков.                        |
| *Player6*. **EndOfStream**       | Используйте *проигрыватель*. **Плайстате**.                                                                                                                                                                                              |
| *Player6*. **Ошибка при**             | Событие не изменено. Однако ошибки помещаются в очередь. Используйте объект **Error** с объектом **ерроритем** для получения сведений об ошибке из очереди. См. пример кода в предыдущем разделе Обработка ошибок. |
| *Player6*. **Клавиша вниз**           | Используйте *проигрыватель*. **Клавиша вниз**                                                                                                                                                                                                 |
| *Player6*. **Нажатие клавиши**          | Используйте *проигрыватель*. **Нажатие клавиши**                                                                                                                                                                                                |
| *Player6*. **Клавиша вверх**             | Используйте *проигрыватель*. **Клавиша вверх**                                                                                                                                                                                                   |
| *Player6*. **Маркерхит**         | Используйте *проигрыватель*. **Маркерхит**.                                                                                                                                                                                              |
| *Player6*. **MouseDown**         | Используйте *проигрыватель*. **MouseDown**                                                                                                                                                                                               |
| *Player6*. **Перемещение указателя**         | Используйте *проигрыватель*. **Перемещение указателя**                                                                                                                                                                                               |
| *Player6*. **MouseUp**           | Используйте *проигрыватель*. **MouseUp**                                                                                                                                                                                                 |
| *Player6*. **Невстреам**         | Используйте *проигрыватель*. **Опенстатечанже**                                                                                                                                                                                         |
| *Player6*. **Опенстатечанже**   | Используйте *проигрыватель*. **Опенстатечанже**.                                                                                                                                                                                        |
| *Player6*. **Плайстатечанже**   | Используйте *проигрыватель*. **Плайстатечанже**.                                                                                                                                                                                        |
| *Player6*. **Поситиончанже**    | Используйте *проигрыватель*. **Поситиончанже**.                                                                                                                                                                                         |
| *Player6*. **Реадистатечанже**  | Используйте *проигрыватель*. **Плайстатечанже**.                                                                                                                                                                                        |
| *Player6*. **Команду скрипта**     | Используйте *проигрыватель*. **Команду скрипта**.                                                                                                                                                                                          |
| *Player6*. **Предупреждение об ошибке**           | Недоступно.                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Руководством по миграции объектной модели**](object-model-migration-guide.md)
</dt> <dt>

[**Справочник по объектной модели для создания сценариев**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





