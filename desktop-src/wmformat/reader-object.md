---
title: Объект модуля чтения
description: Объект модуля чтения
ms.assetid: b5edbf8b-820f-4e09-a482-8efc2283360e
keywords:
- Windows Media Format SDK, объекты Reader
- Расширенный системный формат (ASF), объекты Reader
- ASF (Расширенный системный формат), объекты Reader
- объекты, объекты Reader
- объекты Reader, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7958689fa7744286c92c294219fb2c963e55c860
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "104412742"
---
# <a name="reader-object"></a>Объект модуля чтения

Объект DataReader считывает образцы данных из файлов мультимедиа. Объект модуля чтения в настоящее время поддерживает файлы, использующие структуру файлов ASF, а также файлы в формате MP3. Данные, доставляемые объектом Reader, не сжимаются и готовы к подготовке к просмотру по умолчанию, хотя образцы можно доставлять без распаковки при необходимости. Примеры доставляются асинхронно из объекта Reader; чтобы получить их, необходимо настроить функцию обратного вызова. Для синхронного воспроизведения файлов ASF используйте синхронный объект Reader. Ни модуль чтения, ни синхронный читатель не отображают данные. Необходимо предоставить собственные подпрограммы подготовки отчетов для отображения мультимедиа, извлеченного из файла.

Если файл содержит закодированный носитель, который можно декодировать с помощью кодека, поддерживаемого объектом Reader, можно управлять форматом несжатого вывода. Чтобы изменить формат выходных данных распаковки для потока, необходимо получить объект свойств выходного носителя по умолчанию для этого потока, внести в него изменения и переназначить его потоку в модуле чтения. Объекты свойств выходных данных мультимедиа являются подчиненными для объекта Reader и должны создаваться только с помощью метода [**ивмреадер:: жетаутпутпропс**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) .

Объект модуля чтения создается функцией [**вмкреатереадер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader), которая устанавливает указатель на интерфейс **ивмреадер** . Другие интерфейсы объекта Reader можно получить, вызвав метод **QueryInterface** .

Объект модуля чтения поддерживает следующие интерфейсы.



| Интерфейс                                                    | Описание                                                                                                                                                                     |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**иреференцеклокк**](ireferenceclock.md)                   | Предоставляет доступ к системным часам, используемым модулем чтения.                                                                                                                         |
| [**ивмдрмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)                         | Управляет получением лицензий, свойствами [*DRM*](wmformat-glossary.md) и индивидуальной разстановкой клиентов.                                  |
| [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)                       | Предоставляет доступ к лицензиям, использующим уровни защиты выходных данных (ОПЛ) для указания прав.                                                                                          |
| [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)                       | Задает и получает сведения о заголовке, включая метаданные, [*маркеры*](wmformat-glossary.md)и данные скрипта.                                                 |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)                     | Извлекает сведения о кодеках, которые использовались для кодирования содержимого в файле. Наследует все методы **ивмхеадеринфо**.                                      |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)                     | Поддерживает крупные размеры атрибутов, дублирующиеся имена атрибутов и поддержку нескольких языков. Наследует все методы **ивмхеадеринфо** и **IWMHeaderInfo2**.              |
| [**ивмпаккетсизе**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)                       | Возвращает размер самого крупного пакета в файле, загруженном в модуль чтения.                                                                                                      |
| [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)                     | Возвращает размер наименьшего пакета в файле, загруженном в модуль чтения.                                                                                                     |
| [**ивмпрофиле**](iwmprofile.md)                             | Предоставляет доступ к сведениям о профиле файла, загруженного в средство чтения.                                                                                                    |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)                           | Возвращает глобальный уникальный идентификатор (GUID), если таковой имеется, связанный с профилем. Наследует все методы **ивмпрофиле**.                                            |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)                           | Поддерживает совместное использование пропускной способности и сведения о приоритизации потоков в профиле. Наследует все методы **ивмпрофиле** и **IWMProfile2**.                             |
| [**ивмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)                               | Предоставляет базовые возможности чтения файлов, включая операции открытия, закрытия, запуска, приостановки, возобновления, остановки и получения и задания выходных свойств.                  |
| [**ивмреадеракцелератор**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderaccelerator)         | Взаимодействует с ускорением видео DirectX.                                                                                                                                   |
| [**ивмреадерадванцед**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)               | Предоставляет дополнительные возможности средства чтения, такие как предоставляемые пользователем часы, выделение буфера, возврат статистики и уведомления о выборе потоков.                              |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)             | Предоставляет дополнительный диапазон расширенных методов для существующего объекта Reader. Наследует все методы **ивмреадерадванцед**.                                           |
| [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)             | Обеспечивает расширенный поиск и потоковый контроль. Наследует все методы **ивмреадерадванцед** и **IWMReaderAdvanced2**.                                               |
| [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)             | Предоставляет расширенные возможности чтения, включая поддержку нескольких языков. Наследует все методы **ивмреадерадванцед**, **IWMReaderAdvanced2** и **IWMReaderAdvanced3**. |
| [**ивмреадернетворкконфиг**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)     | Управляет параметрами конфигурации сети.                                                                                                                                        |
| [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2)   | Предоставляет доступ к дополнительным параметрам конфигурации сети. Наследует все методы **ивмреадернетворкконфиг**.                                                          |
| [**ивмреадерстреамклокк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderstreamclock)         | Устанавливает и отменяет таймеры для потоковых часов и получает текущее значение указанного потока часов.                                                                          |
| [**ивмреадертимекоде**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode)               | Содержит сведения о диапазонах кода времени SMPTE в файле, загруженном в средство чтения.                                                                                             |
| [**ивмреадертипенеготиатион**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation) | Проверяет, правильно ли работают изменения выходных свойств потока.                                                                                                |



 

В приложении можно реализовать следующие интерфейсы обратного вызова для отслеживания хода выполнения объекта Reader.



| Интерфейс                                                      | Описание                                                                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**ивмкредентиалкаллбакк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)         | Получает учетные данные пользователей и проверяет наличие у них разрешения на доступ к удаленному сайту.                                               |
| [**ивмреадераллокаторекс**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderallocatorex)           | Предоставляет расширенные альтернативы методам **аллокатефораутпут** и **аллокатефорстреам** интерфейса **ивмреадеркаллбаккадванцед** . |
| [**ивмреадеркаллбакк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)                 | Предоставляет методы обратного вызова для методов **Start** и **Open** для **ивмреадер**.                                                            |
| [**ивмреадеркаллбаккадванцед**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced) | Предоставляет методы обратного вызова для методов интерфейса [**ивмреадерадванцед**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) .                                    |
| [**ивмстатускаллбакк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)                 | Требуется, если информация о состоянии должна быть передана ведущему приложению.                                                                |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Объекты**](objects.md)
</dt> <dt>

[**Чтение файлов ASF**](reading-asf-files.md)
</dt> <dt>

[**Объект модуля синхронного чтения**](synchronous-reader-object.md)
</dt> </dl>

 

 




