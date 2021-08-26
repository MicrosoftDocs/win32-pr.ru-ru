---
title: Интерфейсы DirectWrite
description: Выводит список интерфейсов, определенных DirectWrite.
ms.assetid: 7075e771-ce34-4426-8c07-13e85ff4d453
keywords:
- DirectWrite, интерфейсы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1abd75d83fedf29da1bb5f67073dd74ca10816fdeb6ca43a61f40ad8ae26c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048614"
---
# <a name="directwrite-interfaces"></a>Интерфейсы DirectWrite

DirectWrite определяет следующие интерфейсы.

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|-|-|
| [**идвритеасинкресулт**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) | Представляет результат асинхронной операции. Клиент может использовать интерфейс для ожидания завершения операции, а также для получения результата.  |
| [**идвритебитмапрендертаржет**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) | 32 инкапсулирует независимое от устройства битовое изображение и контекст устройства, которые можно использовать для отрисовки глифов. |
| [**IDWriteBitmapRenderTarget1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1) | 32 инкапсулирует независимое от устройства битовое изображение и контекст устройства, которые можно использовать для отрисовки глифов. |
| [**IDWriteBitmapRenderTarget2**](/windows/windows-app-sdk/api/win32/dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2) | 32 инкапсулирует независимое от устройства битовое изображение и контекст устройства, которые можно использовать для отрисовки глифов. |
| [**идвритеколорглифруненумератор**](idwritecolorglyphrunenumerator.md) | Этот интерфейс позволяет приложению выполнять перечисление по цвету глифа цвета. |
| [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) | Перечислитель упорядоченной коллекции глифов цвета. |
| [**идвритефактори**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) | используется для создания всех последующих объектов DirectWrite. этот интерфейс является корневым интерфейсом фабрики для всех DirectWriteных объектов. |
| [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1) | интерфейс корневой фабрики для всех объектов [DirectWrite](direct-write-portal.md) . |
| [**IDWriteFactory2**](idwritefactory2.md) | интерфейс корневой фабрики для всех объектов [DirectWrite](direct-write-portal.md) . |
| [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) | интерфейс корневой фабрики для всех объектов [DirectWrite](direct-write-portal.md) . |
| [**IDWriteFactory4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory4) | интерфейс корневой фабрики для всех объектов DirectWrite. |
| [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) | интерфейс корневой фабрики для всех объектов DirectWrite. |
| [**IDWriteFactory6**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory6) | представляет объект фабрики, из которого создаются все объекты DirectWrite. **IDWriteFactory6** добавляет новые средства для работы со шрифтами и ресурсами шрифтов. |
| [**IDWriteFactory7**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory7) | этот интерфейс представляет объект фабрики, из которого создаются все объекты DirectWrite. **IDWriteFactory7** добавляет новые средства для работы с системными шрифтами. |
| [**идвритефонт**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | Представляет физический шрифт в коллекции шрифтов. Этот интерфейс используется для создания гарнитуры шрифта из физических шрифтов или для получения таких сведений, как метрики шрифта или имена лиц, от существующих лиц. |
| [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) | Представляет физический шрифт в коллекции шрифтов. |
| [**IDWriteFont2**](idwritefont2.md) | Представляет физический шрифт в коллекции шрифтов. |
| [**IDWriteFont3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefont3) | Представляет шрифт в коллекции шрифтов. |
| [**идвритефонтколлектион**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) | Объект, инкапсулирующий набор шрифтов, например набор шрифтов, установленных в системе, или набор шрифтов в определенном каталоге. API коллекции шрифтов можно использовать для обнаружения доступных семейств шрифтов и шрифтов, а также для получения метаданных о шрифтах. |
| [**IDWriteFontCollection1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1) | Объект, инкапсулирующий набор шрифтов, например набор шрифтов, установленных в системе, или набор шрифтов в определенном каталоге. API коллекции шрифтов можно использовать для обнаружения доступных семейств шрифтов и шрифтов, а также для получения метаданных о шрифтах. |
| [**IDWriteFontCollection2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection2) | Этот интерфейс инкапсулирует набор шрифтов, например набор шрифтов, установленных в системе, или набор шрифтов в определенном каталоге. |
| [**IDWriteFontCollection3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection3) | Этот интерфейс инкапсулирует набор шрифтов, например набор шрифтов, установленных в системе, или набор шрифтов в определенном каталоге. |
| [**идвритефонтколлектионлоадер**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) | Используется для создания коллекции шрифтов, имеющих определенный тип ключа.  |
| [**идвритефонтдовнлоадлистенер**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) | Определяемый приложением интерфейс обратного вызова, который получает уведомления из очереди скачивания шрифтов (интерфейс [**идвритефонтдовнлоадкуеуе**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) ). Обратные вызовы будут выполняться в потоке загрузки, и объекты должны быть подготовлены для обработки вызовов их методов из других потоков в любое время. |
| [**идвритефонтдовнлоадкуеуе**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) | Интерфейс, помещает в очередь запросы на скачивание для удаленных шрифтов, символов, глифов и фрагментов шрифта.  |
| [**идвритефонтфаце**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) | Этот интерфейс предоставляет различные данные шрифта, такие как метрики, имена и контуры глифов. Он содержит тип начертания шрифта, соответствующие ссылки на файлы и идентификационные данные лица. |
| [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) | Содержит тип начертания шрифта, соответствующие ссылки на файлы и идентификационные данные лица.  |
| [**IDWriteFontFace2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontface2) | Этот интерфейс содержит тип начертания шрифта, соответствующие ссылки на файлы и идентификационные данные лица. Он добавляет возможность проверки того, является ли путь визуализации цвета потенциально необходимым.  |
| [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) | Содержит тип начертания шрифта, соответствующие ссылки на файлы и идентификационные данные лица. |
| [**IDWriteFontFace4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4) | Содержит тип начертания шрифта, соответствующие ссылки на файлы и идентификационные данные лица. |
| [**IDWriteFontFace5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface5) | Этот интерфейс содержит тип начертания шрифта, соответствующие ссылки на файлы и идентификационные данные лица. Он добавляет новые средства, такие как сравнение двух сторон шрифта, получение значений оси шрифта и получение ресурса базового шрифта. |
| [**идвритефонтфацереференце**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) | Представляет ссылку на начертание шрифта. Уникально идентифицирующая ссылка на шрифт, с помощью которого можно создать начертание шрифта для запроса метрик шрифта и использования при подготовке к просмотру. Ссылка на начертание шрифта состоит из файла шрифта, индекса начертания шрифта и модели начертания шрифта. Файловые данные могут быть физически отсутствуют на локальном компьютере.  |
| [**IDWriteFontFaceReference1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference1) | Представляет ссылку на начертание шрифта. Уникально идентифицирующая ссылка на шрифт, с помощью которого можно создать начертание шрифта для запроса метрик шрифта и использования при подготовке к просмотру. |
| [**идвритефонтфаллбакк**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback) | Позволяет получать доступ к резервным шрифтам из списка шрифтов. |
| [**идвритефонтфаллбаккбуилдер**](idwritefontfallbackbuilder.md) | Позволяет создавать сопоставления отката шрифта в Юникоде и создавать объекты возврата шрифта из этих сопоставлений. |
| [**идвритефонтфамили**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) | Представляет семейство связанных шрифтов. |
| [**IDWriteFontFamily1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily1) | Представляет семейство связанных шрифтов. |
| [**IDWriteFontFamily2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily2) | Представляет семейство связанных шрифтов. **IDWriteFontFamily2** добавляет новые средства, включая получение шрифтов по значениям оси шрифта. |
| [**идвритефонтфиле**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) | Представляет файл шрифта. Такие приложения, как диспетчеры шрифтов или средства просмотра шрифтов, могут вызывать метод [**идвритефонтфиле:: Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) , чтобы определить, является ли конкретный файл файлом шрифта, а также тип шрифта, поддерживаемый системой шрифтов. |
| [**идвритефонтфилинумератор**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) | Инкапсулирует коллекцию файлов шрифтов. Система шрифтов использует этот интерфейс для перечисления файлов шрифтов при построении коллекции шрифтов. |
| [**идвритефонтфилелоадер**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) | Обрабатывает загрузку файловых ресурсов определенного типа из ключа ссылки на файл шрифта в объект потока файла шрифта.  |
| [**идвритефонтфилестреам**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) | Загружает данные файла шрифта из пользовательского загрузчика файлов шрифтов.  |
| [**идвритефонтлист**](/windows/win32/api/dwrite/nn-dwrite-idwritefontlist) | Представляет список шрифтов. |
| [**IDWriteFontList1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist1) | Представляет список шрифтов. |
| [**IDWriteFontList2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist2) | Представляет список шрифтов. **IDWriteFontList2** добавляет новые средства, включая получение базового набора шрифтов, используемого в списке. |
| [**идвритефонтресаурце**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontresource) | NN-dwrite_3-идвритефонтресаурце |
| [**идвритефонтсет**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) | Представляет набор шрифтов. |
| [**IDWriteFontSet1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1) | Представляет набор шрифтов. |
| [**IDWriteFontSet2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset2) | Представляет набор шрифтов. |
| [**IDWriteFontSet3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset3) | Представляет набор шрифтов. |
| [**идвритефонтсетбуилдер**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) | Содержит методы для создания набора шрифтов. |
| [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) | Содержит методы для создания набора шрифтов. |
| [**IDWriteFontSetBuilder2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder2) | Содержит методы для создания набора шрифтов. |
| [**идвритегдиинтероп**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) | Обеспечивает взаимодействие с GDI, например методы для преобразования начертания шрифта в структуру LOGFONT или преобразования описания шрифта GDI в начертание шрифта. Он также используется для создания целевых объектов прорисовки растрового изображения. |
| [**IDWriteGdiInterop1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritegdiinterop1) | Обеспечивает взаимодействие с GDI, например методы для преобразования начертания шрифта в структуру LOGFONT или преобразования описания шрифта GDI в начертание шрифта. Он также используется для создания целевых объектов прорисовки растрового изображения. |
| [**идвритежеометрисинк**](idwritegeometrysink.md) | [**Идвритежеометрисинк**](idwritegeometrysink.md) является **typedef** интерфейса [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) . Дополнительные сведения см. на странице справочника по [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) . |
| [**идвритеглифрунаналисис**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) | Содержит сведения низкого уровня, используемые для визуализации выполнения глифа. |
| [**идвритеинлинеобжект**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) | Заключает в оболочку определяемую приложением встроенную графику, позволяя Дврите запрашивать метрики, как если бы рисунок был встроен в текст. |
| [**идвритеинмеморифонтфилелоадер**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) | Представляет загрузчик файлов шрифтов, который может обращаться к шрифтам в памяти. |
| [**идврителокалфонтфилелоадер**](idwritelocalfontfileloader.md) | Встроенная реализация интерфейса [**идвритефонтфилелоадер**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) , которая работает с локальными файлами шрифтов и предоставляет сведения о файле локального шрифта из ключа ссылки на файл шрифта. Ссылки на файлы шрифтов, созданные с помощью [**креатефонтфилереференце**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) , используют этот загрузчик файлов шрифтов. |
| [**идврителокализедстрингс**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) | Представляет коллекцию строк, индексированных по имени локали. |
| [**идвритенумберсубститутион**](./idwritenumbersubstitution.md) | Содержит подходящие цифры и цифры пунктуации для указанного языкового стандарта. |
| [**идвритепикселснаппинг**](/windows/win32/api/dwrite/nn-dwrite-idwritepixelsnapping) | Определяет свойства привязки пикселя, такие как пикселы на DIP (аппаратно-независимые пиксели) и текущую матрицу преобразования текстового модуля визуализации. |
| [**идвритеремотефонтфилелоадер**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) | Представляет загрузчик файлов шрифтов, который может обращаться к удаленным (т. е. загружаемым) шрифтам.  |
| [**идвритеремотефонтфилестреам**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream) | Представляет поток файла шрифта, части которого могут быть не локальными.  |
| [**идвритерендерингпарамс**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) | Представляет параметры отрисовки текста, такие как уровень ClearType, улучшенная контрастность и гамма-коррекция для растрирования и фильтрации глифов. Приложение обычно получает объект параметров отрисовки путем вызова метода [**идвритефактори:: креатемониторрендерингпарамс**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) . |
| [**IDWriteRenderingParams1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwriterenderingparams1) | Представляет параметры отрисовки текста для растрирования и фильтрации глифов. |
| [**IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2) | Представляет параметры отрисовки текста для растрирования и фильтрации глифов. |
| [**IDWriteRenderingParams3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriterenderingparams3) | Представляет параметры отрисовки текста для растрирования и фильтрации глифов. |
| [**идвритестринглист**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritestringlist) | Представляет коллекцию строк, индексированных по числу. |
| [**идвритетекстаналисиссинк**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissink) | Этот интерфейс реализуется клиентом анализатора текста для получения выходных данных данного анализа текста.  |
| [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) | Интерфейс, реализуемый для получения выходных данных анализаторов текста. |
| [**идвритетекстаналисиссаурце**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) | Реализуется клиентом анализатора текста для предоставления текста анализатору. Он позволяет разделить логическое представление текста на непрерывный поток символов, идентифицируемых уникальными положениями текста, и фактический макет памяти потенциально дискретных блоков текста в резервном хранилище клиента.  |
| [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) | Интерфейс, реализуемый для предоставления необходимой информации анализатору текста, например тексту и связанным свойствам текста. |
| [**идвритетекстанализер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer) | Анализирует различные свойства текста для сложной обработки скриптов, например двунаправленной (двунаправленной) поддержки для таких языков, как арабский, определение возможностей разрыва строк, размещение глифов и подстановка чисел. |
| [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) | Анализирует различные свойства текста для обработки сложных скриптов. |
| [**IDWriteTextAnalyzer2**](idwritetextanalyzer2.md) | Анализирует различные свойства текста для обработки сложных скриптов. |
| [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) | Интерфейс [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) описывает свойства шрифта и абзаца, используемые для форматирования текста, и описывает сведения о языковых стандартах.  |
| [**IDWriteTextFormat1**](idwritetextformat1.md) | Описывает свойства шрифта и абзаца, используемые для форматирования текста, а также сведения о языковых стандартах.  |
| [**IDWriteTextFormat2**](idwritetextformat2.md) | Описывает свойства шрифта и абзаца, используемые для форматирования текста, а также сведения о языковых стандартах.  |
| [**IDWriteTextFormat3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextformat3) | Описывает свойства шрифта и абзаца, используемые для форматирования текста, а также сведения о языковых стандартах. |
| [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) | Интерфейс [**идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) представляет блок текста после полного анализа и форматирования. |
| [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) | Представляет блок текста после полного анализа и форматирования. |
| [**IDWriteTextLayout2**](idwritetextlayout2.md) | Представляет блок текста после полного анализа и форматирования. |
| [**IDWriteTextLayout3**](idwritetextlayout3.md) | Представляет блок текста после полного анализа и форматирования.  |
| [**идвритетекстрендерер**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) | Представляет набор определяемых приложением обратных вызовов, выполняющих отрисовку текста, встроенных объектов и украшений, таких как подчеркивания. |
| [**IDWriteTextRenderer1**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritetextrenderer1) | Представляет набор определяемых приложением обратных вызовов, выполняющих отрисовку текста, встроенных объектов и украшений, таких как подчеркивания.  |
| [**идвритетипографи**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) | Представляет параметр оформления шрифта. |