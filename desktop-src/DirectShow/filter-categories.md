---
description: В следующих таблицах перечислены идентификаторы CLSID для категорий фильтров DirectShow.
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: Фильтровать категории
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4ccb9443c405abcbd0b9afbd406d6faf2558a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416444"
---
# <a name="filter-categories"></a>Фильтровать категории

В следующих таблицах перечислены идентификаторы CLSID для категорий фильтров DirectShow.

-   [Категории фильтров DirectShow](#directshow-filter-categories)
-   [Другие категории фильтров](#other-filter-categories)
-   [Meta-Категория фильтра DirectShow](#directshow-filter-meta-category)
-   [Категории DMO](#dmo-categories)
-   [См. также](#related-topics)

## <a name="directshow-filter-categories"></a>Категории фильтров DirectShow

Перечисленные здесь категории перечисляются с помощью модуля [сопоставления фильтров](filter-mapper.md). Однако по умолчанию средство сопоставления фильтров не учитывает категории с \_ \_ недоступностью и не использует их \_ . Дополнительные сведения см. в разделе [**IFilterMapper2:: енумматчингфилтерс**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters). Все перечисленные здесь категории также можно перечислить с помощью [перечислителя системных устройств](system-device-enumerator.md).

Следующие категории объявляются в UUID. h. Включите заголовочный файл DShow. h.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Понятное имя</th>
<th>CLSID</th>
<th>Заслуживают</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Источники записи звука</td>
<td><strong>CLSID_AudioInputDeviceCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Звуковые компрессоры</td>
<td><strong>CLSID_AudioCompressorCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Модули подготовки звука</td>
<td><strong>CLSID_AudioRendererCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>Фильтры управления устройствами</td>
<td><strong>CLSID_DeviceControlCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Фильтры DirectShow</td>
<td><strong>CLSID_LegacyAmFilterCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>Внешние модули подготовки отчетов</td>
<td><strong>CLSID_TransmitCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Модули подготовки MIDI</td>
<td><strong>CLSID_MidiRendererCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>Источники видеозаписи</td>
<td><strong>CLSID_VideoInputDeviceCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Видео программы сжатия</td>
<td><strong>CLSID_VideoCompressorCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Устройства распаковки WDM Stream</td>
<td><strong>CLSID_DVDHWDecodersCategory</strong>
<blockquote>
[!Note]<br />
В этой категории содержатся аппаратные декодеры DVD.
</blockquote>
<br/></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Устройства захвата WDM Streaming</td>
<td><strong>AM_KSCATEGORY_CAPTURE</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Устройства микширования WDM Streaming</td>
<td><strong>AM_KSCATEGORY_CROSSBAR</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Устройства отрисовки WDM Streaming</td>
<td><strong>AM_KSCATEGORY_RENDER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Устройства tee/разделитель WDM Streaming</td>
<td><strong>AM_KSCATEGORY_SPLITTER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Аудиоустройства потоковой передачи WDM Streaming</td>
<td><strong>AM_KSCATEGORY_TVAUDIO</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>Устройства ТВ-тюнера WDM Streaming</td>
<td><strong>AM_KSCATEGORY_TVTUNER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>ВБИ кодеки WDM Streaming</td>
<td><strong>AM_KSCATEGORY_VBICODEC</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
</tbody>
</table>



 

Следующие категории объявляются в файле заголовка KS. h.



| Понятное имя                          | CLSID                                   | Заслуживают                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| Преобразования связи WDM Streaming | **КСКАТЕГОРИ \_ коммуникатионстрансформ** | **\_ \_ не \_ использовать** |
| Преобразования данных потоковой передачи WDM          | **\_Преобразование кскатегори**           | **\_ \_ не \_ использовать** |
| Преобразования интерфейса потоковой передачи WDM     | **КСКАТЕГОРИ \_ интерфацетрансформ**      | **\_ \_ не \_ использовать** |
| Устройства микшера потоковой передачи WDM            | **\_микшер кскатегори**                   | **\_ \_ не \_ использовать** |



 

Следующие категории объявляются в файле заголовка Бдамедиа. h. Включите следующие файлы заголовков: KS. h, ксмедиа. h и бдамедиа. h.



| Понятное имя                       | CLSID                                       | Заслуживают                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| BDA сетевые поставщики               | **\_ \_ поставщик сети BDA \_ кскатегори**      | **неуспешный \_ режим**       |
| Компоненты приемника BDA             | **\_ \_ компонент приемника BDA кскатегори \_**    | **\_ \_ не \_ использовать** |
| Фильтры визуализации BDA               | **\_приемник IP-адресов кскатегори \_**                    | **\_ \_ не \_ использовать** |
| BDA фильтры источников                  | **КСКАТЕГОРИ \_ BDA \_ Network \_ тюнер**         | **\_ \_ не \_ использовать** |
| Средства подготовки отчетов для передачи данных BDA | **\_ \_ сведения о транспорте кскатегори BDA \_** | **неуспешный \_ режим**       |



 

> [!Note]  
> Декодеры регистрируются в категории "фильтры DirectShow" (CLSID \_ легациамфилтеркатегори).

 

## <a name="other-filter-categories"></a>Другие категории фильтров

Перечисленные здесь категории можно перечислить с помощью перечислителя системных устройств, но они не видны для модуля сопоставления фильтров и не используются [интеллектуальным соединением](intelligent-connect.md).

Следующие категории объявляются в файле заголовка Кедит. h.



| Понятное имя            | клид                             | Заслуживают                   |
|--------------------------|----------------------------------|-------------------------|
| Видеоэффекты (1 вход)  | **\_VIDEOEFFECTS1CATEGORY CLSID** | **\_ \_ не \_ использовать** |
| Видеоэффекты (2 входа) | **\_VIDEOEFFECTS2CATEGORY CLSID** | **\_ \_ не \_ использовать** |



 

Эти категории содержат видеоэффекты и переходы для [служб редактирования DirectShow](directshow-editing-services.md).

-   "Видеоролики (1 Ввод)" содержит видеоэффекты.
-   "Видеоэффекты (2 входные данные)" содержат видеопереходы.

Дополнительные сведения см. в разделе [перечисление эффектов и переходов](enumerating-effects-and-transitions.md).

Следующие категории объявляются в файле заголовков UUID. h. Включите заголовочный файл DShow. h.



| Понятное имя       | клид                                | Заслуживают                   |
|---------------------|-------------------------------------|-------------------------|
| Кодировщики Енкапи     | **\_МЕДИАЕНКОДЕРКАТЕГОРИ CLSID**     | **\_ \_ не \_ использовать** |
| Мультиплексоры Енкапи | **\_МЕДИАМУЛТИПЛЕКСЕРКАТЕГОРИ CLSID** | **\_ \_ не \_ использовать** |



 

## <a name="directshow-filter-meta-category"></a>Meta-Category фильтров DirectShow



| Понятное имя                 | CLSID                            | Заслуживают          |
|-------------------------------|----------------------------------|----------------|
| Категории фильтра ActiveMovie | **\_АКТИВЕМОВИЕКАТЕГОРИЕС CLSID** | Неприменимо |



 

Эта мета-категория содержит список категорий фильтров. Если Категория фильтра не отображается в этом списке, то средство [сопоставления фильтров](filter-mapper.md) игнорирует категорию, что означает, что фильтр недоступен для [интеллектуального соединения](intelligent-connect.md).

Чтобы перечислить список категорий фильтров, вызовите [**икреатедевенум:: креатеклассенумератор**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) со значением CLSID \_ активемовиекатегориес. Моникеры, возвращаемые этим методом, поддерживают следующие свойства.



| Имя свойства  | Описание                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| FriendlyName | Имя категории (VT \_ BSTR).                                                              |
| Заслуживают        | Категория заслуживает (VT \_ i4). Если это свойство отсутствует, **\_ \_ \_ обработайте его как недоступное**. |
| ЭТОМУ        | CLSID категории (VT \_ BSTR).                                                             |



 

Чтобы добавить новую категорию фильтра в этот список, вызовите метод [**IFilterMapper2:: креатекатегори**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).

## <a name="dmo-categories"></a>Категории DMO

Объекты мультимедиа DirectX (дмос) используют другой механизм перечисления из фильтров DirectShow. Дополнительные сведения см. [в разделе Регистрация DMO](registering-a-dmo.md). Однако можно использовать перечислитель системных устройств для перечисления категорий DMO. Моникеры привязываются к [фильтру оболочки DMO](dmo-wrapper-filter.md) и автоматически инициализируют фильтр с помощью DMO.

Кроме того, некоторые категории DMO сопоставляются с категориями фильтров DirectShow в целях интеллектуального подключения:



| Категория DMO                    | Эквивалент DirectShow              |
|---------------------------------|------------------------------------|
| **\_КОДИРОВЩИК дмокатегори Audio \_** | **\_АУДИОКОМПРЕССОРКАТЕГОРИ CLSID** |
| **\_декодер дмокатегори Audio \_** | **\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID**  |
| **\_кодировщик видео \_ дмокатегори** | **\_ВИДЕОКОМПРЕССОРКАТЕГОРИ CLSID** |
| **\_декодер видео \_ дмокатегори** | **\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID**  |



 

Обратите внимание, что категории эффектов видео и звуковых эффектов не сопоставлены ни с одной из категорий DirectShow.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Константы и идентификаторы GUID](constants-and-guids.md)
</dt> <dt>

[Перечисление устройств и фильтров](enumerating-devices-and-filters.md)
</dt> <dt>

[Интеллектуальное подключение](intelligent-connect.md)
</dt> <dt>

[Структура разделов реестра](layout-of-the-registry-keys.md)
</dt> <dt>

[Использование средства сопоставления фильтров](using-the-filter-mapper.md)
</dt> <dt>

[Использование перечислителя системных устройств](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




