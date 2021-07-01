---
title: Фильтр чтения WM ASF (пакет SDK для формата Windows Media 11)
description: Узнайте о фильтре модуля чтения WM ASF для пакета SDK Windows Media Format 11. Просмотрите сведения о фильтре и см. связанные разделы.
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Пакет SDK для Windows Media Format, средство чтения WM ASF
- DirectShow, средство чтения WM ASF
- Фильтры КАСФ, средство чтения WM ASF
- Средство чтения WM ASF
- Расширенный формат систем (ASF), читатель WM ASF
- ASF (Расширенный системный формат), читатель WM ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26bde36b1b2cfa7644d6e75d8d1ff96260b2e457
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119649"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a>Фильтр чтения WM ASF (пакет SDK для формата Windows Media 11)

При наличии имени файла ASF или URL-адреса средство чтения WM ASF считывает сжатое содержимое, анализирует потоки и предоставляет закрепление вывода для каждого из них. Этот фильтр подключается к Windows Media Audio или Windows Media Video дмос, который выполняет распаковку. Поиск поддерживается, если ASF-файл доступен для поиска. Модуль чтения WM ASF применяет штампы времени к примерам мультимедиа на основе метки времени в файле ASF, но не изменяет метки времени каким бы то ни было образом. На внутреннем уровне фильтр использует объект чтения формата Windows Media для чтения содержимого на основе Windows Media.

> [!Note]  
> В пакете SDK для DirectX этот фильтр не является фильтром источника по умолчанию для файлов ASF, поэтому с этим пакетом SDK этот фильтр нельзя использовать с методом **RenderFile** . необходимо явно добавить его в граф фильтра с помощью идентификатора класса (CLSID). Это поведение отличается от пакета SDK Windows Media Format. При установке библиотек среды выполнения пакета SDK для Windows Media Format средство чтения WM ASF регистрируется в качестве фильтра по умолчанию для файлов ASF.

 

В следующей таблице содержатся сведения о фильтре чтения WM ASF, например интерфейсах и типах носителей, которые он поддерживает.



|  Сведения о фильтре                      |  Типы                                                                                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Интерфейсы фильтра      | **Ибасефилтер**, **ифилесаурцефилтер**, **IServiceProvider**, **ивмхеадеринфо**, **ивмреадерадванцед** (частично реализовано). См. примечания.), **IWMReaderAdvanced2** (частично реализован), **Ивмдрмреадер** (через **IServiceProvider**) |
| Типы носителей входных закрепления  | Неприменимо                                                                                                                                                                                                                                |
| Интерфейсы входных закрепления   | Неприменимо                                                                                                                                                                                                                                |
| Типы носителей для выходного ПИН-кода | МУЛЬТИМЕДИЙное \_ видео, MediaType \_ Audio, MediaType \_ команду скрипта, MediaType \_ филетрансфер                                                                                                                                                         |
| Тип формата            | **VIDEOINFOHEADER2** , если содержимое [*чередуются*](wmformat-glossary.md), в противном случае **видеоинфохеадер**                                                                                                                    |
| Интерфейсы выходного ПИН-кода  | **Имедиасикинг**, **иамвмбуфферпасс**, **IServiceProvider**, **IWMStreamConfig2** (через **IServiceProvider**)                                                                                                                             |
| Фильтровать CLSID           | \_ВМАСФРЕАДЕР CLSID                                                                                                                                                                                                                            |
| CLSID страницы свойств    | Нет страницы свойств                                                                                                                                                                                                                              |
| Исполняемый объект             | Qasf.dll                                                                                                                                                                                                                                      |
| Заслуживают                  | \_маловероятно                                                                                                                                                                                                                               |
| Категория фильтра        | \_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Remarks

Читатель WM ASF частично реализует интерфейсы **ивмреадерадванцед** и **IWMReaderAdvanced2** , чтобы предоставить приложениям доступ к информационным методам объекта Reader. Реализация фильтра просто передает вызовы в интерфейс объекта Reader. Методы потоковой передачи не реализованы, поскольку фильтр должен иметь полный контроль над процессом потоковой передачи. Реализуются следующие методы **ивмреадерадванцед** и **IWMReaderAdvanced2** :

-   [**Ивмреадерадванцед:: Statistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [**Ивмреадерадванцед:: SetClientInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [**IWMReaderAdvanced2:: Жетбуфферпрогресс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [**IWMReaderAdvanced2:: Жетдовнлоадпрогресс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [**IWMReaderAdvanced2:: Жетплаймоде**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [**IWMReaderAdvanced2:: Жетпротоколнаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [**IWMReaderAdvanced2:: Сетлогклиентид**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [**IWMReaderAdvanced2:: Сетплаймоде**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Справочник по КАСФ DirectShow**](directshow-qasf-reference.md)
</dt> <dt>

[**Чтение файлов ASF в DirectShow**](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




