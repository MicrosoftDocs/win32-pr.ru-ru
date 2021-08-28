---
description: в следующих таблицах перечислены идентификаторы clsid для категорий фильтров DirectShow.
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: Фильтровать категории
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4e8c2b5e5f9e477633774cb24e707aa9d71060
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476330"
---
# <a name="filter-categories"></a>Фильтровать категории

в следующих таблицах перечислены идентификаторы clsid для категорий фильтров DirectShow.

-   [DirectShow Фильтровать категории](#directshow-filter-categories)
-   [Другие категории фильтров](#other-filter-categories)
-   [DirectShow Мета-Категория фильтра](#directshow-filter-meta-category)
-   [DMO Категорий](#dmo-categories)
-   [Связанные темы](#related-topics)

## <a name="directshow-filter-categories"></a>DirectShow Фильтровать категории

Перечисленные здесь категории перечисляются с помощью модуля [сопоставления фильтров](filter-mapper.md). Однако по умолчанию средство сопоставления фильтров не учитывает категории с \_ \_ недоступностью и не использует их \_ . Дополнительные сведения см. в разделе [**IFilterMapper2:: енумматчингфилтерс**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters). Все перечисленные здесь категории также можно перечислить с помощью [перечислителя системных устройств](system-device-enumerator.md).

Следующие категории объявляются в UUID. h. Включите заголовочный файл DShow. h.




| Понятное имя | CLSID | Заслуживают | 
|---------------|-------|-------|
| Источники записи звука | <strong>CLSID_AudioInputDeviceCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Звуковые компрессоры | <strong>CLSID_AudioCompressorCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Модули подготовки звука | <strong>CLSID_AudioRendererCategory</strong> | <strong>MERIT_NORMAL</strong> | 
| Фильтры управления устройствами | <strong>CLSID_DeviceControlCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| DirectShow Фильтрующ | <strong>CLSID_LegacyAmFilterCategory</strong> | <strong>MERIT_NORMAL</strong> | 
| Внешние модули подготовки отчетов | <strong>CLSID_TransmitCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Модули подготовки MIDI | <strong>CLSID_MidiRendererCategory</strong> | <strong>MERIT_NORMAL</strong> | 
| Источники видеозаписи | <strong>CLSID_VideoInputDeviceCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Видео программы сжатия | <strong>CLSID_VideoCompressorCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Устройства распаковки WDM Stream | <strong>CLSID_DVDHWDecodersCategory</strong><blockquote>[!Note]<br />В этой категории содержатся аппаратные декодеры DVD.</blockquote><br /> | <strong>MERIT_DO_NOT_USE</strong> | 
| Устройства захвата WDM Streaming | <strong>AM_KSCATEGORY_CAPTURE</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Устройства микширования WDM Streaming | <strong>AM_KSCATEGORY_CROSSBAR</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Устройства отрисовки WDM Streaming | <strong>AM_KSCATEGORY_RENDER</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Устройства tee/разделитель WDM Streaming | <strong>AM_KSCATEGORY_SPLITTER</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Аудиоустройства потоковой передачи WDM Streaming | <strong>AM_KSCATEGORY_TVAUDIO</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Устройства ТВ-тюнера WDM Streaming | <strong>AM_KSCATEGORY_TVTUNER</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| ВБИ кодеки WDM Streaming | <strong>AM_KSCATEGORY_VBICODEC</strong> | <strong>MERIT_DO_NOT_USE</strong> | 




 

Следующие категории объявляются в файле заголовка KS. h.



| Понятное имя                          | CLSID                                   | Заслуживают                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| Преобразования связи WDM Streaming | **КСКАТЕГОРИ \_ коммуникатионстрансформ** | **\_ \_ не \_ использовать** |
| Преобразования данных потоковой передачи WDM          | **\_Преобразование кскатегори**           | **\_ \_ не \_ использовать** |
| Преобразования интерфейса потоковой передачи WDM     | **КСКАТЕГОРИ \_ интерфацетрансформ**      | **\_ \_ не \_ использовать** |
| потоковая передача WDM stream Mixer устройств            | **\_микшер кскатегори**                   | **\_ \_ не \_ использовать** |



 

Следующие категории объявляются в файле заголовка Бдамедиа. h. Включите следующие файлы заголовков: KS. h, ксмедиа. h и бдамедиа. h.



| Понятное имя                       | CLSID                                       | Заслуживают                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| BDA сетевые поставщики               | **\_ \_ поставщик сети BDA \_ кскатегори**      | **неуспешный \_ режим**       |
| Компоненты приемника BDA             | **\_ \_ компонент приемника BDA кскатегори \_**    | **\_ \_ не \_ использовать** |
| Фильтры визуализации BDA               | **\_приемник IP-адресов кскатегори \_**                    | **\_ \_ не \_ использовать** |
| BDA фильтры источников                  | **КСКАТЕГОРИ \_ BDA \_ Network \_ тюнер**         | **\_ \_ не \_ использовать** |
| Средства подготовки отчетов для передачи данных BDA | **\_ \_ сведения о транспорте кскатегори BDA \_** | **неуспешный \_ режим**       |



 

> [!Note]  
> декодеры регистрируются в категории "фильтры DirectShow" (CLSID \_ легациамфилтеркатегори).

 

## <a name="other-filter-categories"></a>Другие категории фильтров

перечисленные здесь категории можно перечислить с помощью перечислителя системных устройств, но они не видны для модуля сопоставления фильтров и не используются [интеллектуальными Подключение](intelligent-connect.md).

Следующие категории объявляются в файле заголовка Кедит. h.



| Понятное имя            | клид                             | Заслуживают                   |
|--------------------------|----------------------------------|-------------------------|
| Видеоэффекты (1 вход)  | **\_VIDEOEFFECTS1CATEGORY CLSID** | **\_ \_ не \_ использовать** |
| Видеоэффекты (2 входа) | **\_VIDEOEFFECTS2CATEGORY CLSID** | **\_ \_ не \_ использовать** |



 

эти категории содержат видеоэффекты и переходы для [DirectShow редактирования служб](directshow-editing-services.md):

-   "Видеоролики (1 Ввод)" содержит видеоэффекты.
-   "Видеоэффекты (2 входные данные)" содержат видеопереходы.

Дополнительные сведения см. в разделе [перечисление эффектов и переходов](enumerating-effects-and-transitions.md).

Следующие категории объявляются в файле заголовков UUID. h. Включите заголовочный файл DShow. h.



| Понятное имя       | клид                                | Заслуживают                   |
|---------------------|-------------------------------------|-------------------------|
| Кодировщики Енкапи     | **\_МЕДИАЕНКОДЕРКАТЕГОРИ CLSID**     | **\_ \_ не \_ использовать** |
| Мультиплексоры Енкапи | **\_МЕДИАМУЛТИПЛЕКСЕРКАТЕГОРИ CLSID** | **\_ \_ не \_ использовать** |



 

## <a name="directshow-filter-meta-category"></a>DirectShow Meta-Category фильтра



| Понятное имя                 | CLSID                            | Заслуживают          |
|-------------------------------|----------------------------------|----------------|
| Категории фильтра ActiveMovie | **\_АКТИВЕМОВИЕКАТЕГОРИЕС CLSID** | Неприменимо |



 

Эта мета-категория содержит список категорий фильтров. если категория фильтра не отображается в этом списке, то средство [сопоставления фильтров](filter-mapper.md) игнорирует категорию, что означает, что фильтр недоступен для [интеллектуальных Подключение](intelligent-connect.md).

Чтобы перечислить список категорий фильтров, вызовите [**икреатедевенум:: креатеклассенумератор**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) со значением CLSID \_ активемовиекатегориес. Моникеры, возвращаемые этим методом, поддерживают следующие свойства.



| Имя свойства  | Описание                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| FriendlyName | Имя категории (VT \_ BSTR).                                                              |
| Заслуживают        | Категория заслуживает (VT \_ i4). Если это свойство отсутствует, **\_ \_ \_ обработайте его как недоступное**. |
| ЭТОМУ        | CLSID категории (VT \_ BSTR).                                                             |



 

Чтобы добавить новую категорию фильтра в этот список, вызовите метод [**IFilterMapper2:: креатекатегори**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).

## <a name="dmo-categories"></a>DMO Категорий

объекты мультимедиа DirectX (дмос) используют другой механизм перечисления DirectShow фильтров. Дополнительные сведения см. [в разделе регистрация DMO](registering-a-dmo.md). однако можно использовать перечислитель системных устройств для перечисления DMO категорий. моникеры привязываются к [фильтру оболочки DMO](dmo-wrapper-filter.md) и автоматически инициализируют фильтр с DMO.

кроме того, некоторые категории DMO сопоставляются с DirectShow категориями фильтров в целях интеллектуального подключения:



| DMO Категори                    | DirectShow Друг              |
|---------------------------------|------------------------------------|
| **\_КОДИРОВЩИК дмокатегори Audio \_** | **\_АУДИОКОМПРЕССОРКАТЕГОРИ CLSID** |
| **\_декодер дмокатегори Audio \_** | **\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID**  |
| **\_кодировщик видео \_ дмокатегори** | **\_ВИДЕОКОМПРЕССОРКАТЕГОРИ CLSID** |
| **\_декодер видео \_ дмокатегори** | **\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID**  |



 

обратите внимание, что категории эффектов видео и звуковых эффектов не сопоставлены ни с одной из категорий DirectShow.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Константы и идентификаторы GUID](constants-and-guids.md)
</dt> <dt>

[Перечисление устройств и фильтров](enumerating-devices-and-filters.md)
</dt> <dt>

[интеллектуальные Подключение](intelligent-connect.md)
</dt> <dt>

[Структура разделов реестра](layout-of-the-registry-keys.md)
</dt> <dt>

[Использование средства сопоставления фильтров](using-the-filter-mapper.md)
</dt> <dt>

[Использование перечислителя системных устройств](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




