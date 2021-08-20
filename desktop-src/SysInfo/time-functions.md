---
description: С системным временем используются следующие функции.
ms.assetid: 3733f611-c6a1-4d48-b21e-ada3490c5de1
title: Функции времени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d537224ceaf072fd5e11f0fdd839215c7317a5378de90e1be56def3f90490105
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117958047"
---
# <a name="time-functions"></a>Функции времени

С системным временем используются следующие функции.



| Функция                                                                   | Описание:                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**GetSystemTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtime)                                     | Извлекает текущую системную дату и время в формате UTC.                                              |
| [**жетсистемтимеаджустмент**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeadjustment)                 | Определяет, применяется ли к системе периодические корректировки времени для времени суток.          |
| [**жеттимеформат**](/windows/desktop/api/datetimeapi/nf-datetimeapi-gettimeformata)                                    | Форматирует системное время как строку времени для указанного языкового стандарта.                                         |
| [**нткуерисистемтиме**](/windows/desktop/api/Winternl/nf-winternl-ntquerysystemtime)                             | Возвращает системное время.                                                                               |
| [**ртллокалтиметосистемтиме**](/windows/desktop/api/Winternl/nf-winternl-rtllocaltimetosystemtime)               | Преобразует указанное местное время в системное время.                                                      |
| [**RtlTimeToSecondsSince1970**](/windows/desktop/api/Winternl/nf-winternl-rtltimetosecondssince1970)             | Преобразует указанное системное время в число секунд, начиная с первой секунды 1 января 1970. |
| [**сетсистемтиме**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtime)                                     | Задает текущее системное время и дату.                                                                 |
| [**сетсистемтимеаджустмент**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setsystemtimeadjustment)                 | Включает или отключает периодические корректировки времени для системных часов.                       |
| [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)                       | Преобразует системное время в файловый момент времени.                                                                 |
| [**системтиметотзспеЦификлокалтиме**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime) | Преобразует время в формате UTC в соответствующее местное время указанного часового пояса.                               |
| [**тзспеЦификлокалтиметосистемтиме**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime) | Преобразует местное время в время в формате UTC.                                                                   |



 

Следующие функции используются с местным временем.



| Функция                                                                                           | Описание:                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**енумдинамиктимезонеинформатион**](/windows/win32/api/timezoneapi/nf-timezoneapi-enumdynamictimezoneinformation)                           | Перечисляет динамические записи о времени перехода на летнее время, хранящиеся в реестре.                                                             |
| [**филетиметолокалфилетиме**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime)                                         | Преобразует время файла в формате UTC в местное время файла.                                                                                                  |
| [**жетдинамиктимезонеинформатион**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformation)                             | Извлекает текущие параметры часового пояса и динамического летнего времени.                                                                      |
| [**жетдинамиктимезонеинформатионеффективэйеарс**](/windows/win32/api/timezoneapi/nf-timezoneapi-getdynamictimezoneinformationeffectiveyears) | Извлекает диапазон, выраженный в годах, для которого [**\_ \_ \_ сведения о динамическом часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-dynamic_time_zone_information) имеют допустимые записи. |
| [**жетлокалтиме**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlocaltime)                                                               | Извлекает текущую локальную дату и время.                                                                                                      |
| [**жеттимезонеинформатион**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)                                           | Извлекает текущие параметры часового пояса.                                                                                                       |
| [**жеттимезонеинформатионфореар**](/windows/win32/api/timezoneapi/nf-timezoneapi-gettimezoneinformationforyear)                             | Извлекает параметры часового пояса для указанного года и часового пояса.                                                                          |
| [**ртллокалтиметосистемтиме**](/windows/desktop/api/Winternl/nf-winternl-rtllocaltimetosystemtime)                                       | Преобразует указанное местное время в системное время.                                                                                               |
| [**сетдинамиктимезонеинформатион**](/windows/win32/api/timezoneapi/nf-timezoneapi-setdynamictimezoneinformation)                             | Задает параметры текущего часового пояса и динамического летнего времени.                                                                           |
| [**сетлокалтиме**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-setlocaltime)                                                               | Задает текущее местное время и дату.                                                                                                           |
| [**сеттимезонеинформатион**](/windows/win32/api/timezoneapi/nf-timezoneapi-settimezoneinformation)                                           | Задает текущие параметры часового пояса.                                                                                                            |
| [**системтиметотзспеЦификлокалтиме**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltime)                         | Преобразует время в формате UTC в соответствующее местное время указанного часового пояса.                                                                        |
| [**системтиметотзспеЦификлокалтимикс**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetotzspecificlocaltimeex)                     | Преобразует время в формате UTC с динамическим параметром перехода на летнее время в указанное местное время часового пояса.                             |
| [**тзспеЦификлокалтиметосистемтиме**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtime)                         | Преобразует местное время в время в формате UTC.                                                                                                            |
| [**тзспеЦификлокалтиметосистемтимикс**](/windows/win32/api/timezoneapi/nf-timezoneapi-tzspecificlocaltimetosystemtimeex)                     | Преобразует местное время с динамическим параметром перехода на летнее время в время в формате UTC.                                                                   |



 

Следующие функции используются со временем файла.



| Функция                                                   | Описание:                                                                                                     |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**компарефилетиме**](/windows/desktop/api/FileAPI/nf-fileapi-comparefiletime)                 | Сравнивает два раза файлов.                                                                                        |
| [**филетиметолокалфилетиме**](/windows/desktop/api/FileAPI/nf-fileapi-filetimetolocalfiletime) | Преобразует время файла в формате UTC в местное время файла.                                                                  |
| [**филетиметосистемтиме**](/windows/win32/api/timezoneapi/nf-timezoneapi-filetimetosystemtime)       | Преобразует время файла в формат системного времени.                                                                     |
| [**Функции getFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime)                         | Извлекает дату и время создания указанного файла или каталога, последнего доступа и последнего изменения. |
| [**GetSystemTimeAsFileTime**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimeasfiletime) | Извлекает текущую системную дату и время в формате UTC.                                                       |
| [**локалфилетиметофилетиме**](/windows/desktop/api/FileAPI/nf-fileapi-localfiletimetofiletime) | Преобразует время локального файла в файловый момент времени, основанный на формате UTC.                                                         |
| [**сетфилетиме**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime)                         | Задает дату и время создания указанного файла или каталога, последнего доступа или последнего изменения.       |
| [**SystemTimeToFileTime**](/windows/win32/api/timezoneapi/nf-timezoneapi-systemtimetofiletime)       | Преобразует системное время в файловый момент времени.                                                                          |



 

Следующие функции используются с датой и временем MS-DOS.



| Функция                                               | Описание:                                          |
|--------------------------------------------------------|------------------------------------------------------|
| [**досдатетиметофилетиме**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) | Преобразует значения даты и времени MS-DOS в файловый момент времени. |
| [**филетиметодосдатетиме**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) | Преобразует время файла в значения даты и времени MS-DOS. |



 

при Windows времени используются следующие функции.



| Функция                                 | Описание:                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**жетсистемтимес**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes) | Возвращает сведения о времени системы.                                                                  |
| [**жеттикккаунт**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount)     | Возвращает число миллисекунд, прошедших с момента запуска системы, до 49,7 дней. |
| [**GetTickCount64**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount64) | Возвращает число миллисекунд, прошедших с момента запуска системы.                  |



 

Для счетчиков производительности с высоким разрешением используются следующие функции.



| Функция                                                              | Описание:                                                             |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)     | Извлекает текущее значение счетчика производительности с высоким разрешением. |
| [**куериперформанцефрекуенци**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) | Возвращает частоту счетчика производительности с высоким разрешением.     |



 

С дополнительным счетчиком производительности используются следующие функции.



| Функция                                                                                           | Описание:                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**куеряуксилиарикаунтерфрекуенци**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryauxiliarycounterfrequency)                           | Запрашивает частоту вспомогательных счетчиков.                                                                                                                                                                      |
| [**конвертауксилиарикаунтертоперформанцекаунтер**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-convertauxiliarycountertoperformancecounter) | Преобразует указанное значение дополнительного счетчика в соответствующее значение счетчика производительности; При необходимости предоставляет оценочную ошибку преобразования в наносекундах из-за задержек и максимального возможного смещения. |
| [**конвертперформанцекаунтертоауксилиарикаунтер**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-convertperformancecountertoauxiliarycounter) | Преобразует указанное значение счетчика производительности в соответствующее значение вспомогательного счетчика; При необходимости предоставляет оценочную ошибку преобразования в наносекундах из-за задержек и максимального возможного смещения. |



 

Следующая функция используется со временем прерываний.



| Функция                                                                       | Описание:                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**куеринтеррупттиме**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime)                               | Возвращает текущее количество времени прерываний.                                                                                                                                                                                                                |
| [**куеринтеррупттимепреЦисе**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttimeprecise)                 | Возвращает текущее число времени прерываний в более точной форме, чем [**куеринтеррупттиме**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryinterrupttime) .                                                                                                                             |
| [**куерюнбиасединтеррупттиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime)               | Возвращает текущее значение несмещенного счетчика времени прерываний. Несмещенное значение счетчика времени прерываний не включает время, затрачиваемое системой на ожидание в спящем режиме или в спящий режим.                                                                                                    |
| [**куерюнбиасединтеррупттимепреЦисе**](/windows/desktop/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttimeprecise) | Возвращает текущее значение несмещенного счетчика времени прерываний в более точной форме, чем [**куерюнбиасединтеррупттиме**](/windows/win32/api/realtimeapiset/nf-realtimeapiset-queryunbiasedinterrupttime) . Несмещенное значение счетчика времени прерываний не включает время, затрачиваемое системой на ожидание в спящем режиме или в спящий режим. |



 

 

 
