---
title: Коды результатов IMAPIv1 (Имапиеррор. h)
description: Методы интерфейсов IMAPI возвращают S \_ ОК, если метод был успешным. В противном случае они возвращают один из следующих кодов результатов.
ms.assetid: 0143ad10-9b65-4621-9bed-71dadd38c3fc
topic_type:
- apiref
api_name:
- IMAPI_S_PROPERTIESIGNORED
- IMAPI_S_BUFFER_TO_SMALL
- IMAPI_E_NOTOPENED
- IMAPI_E_NOTINITIALIZED
- IMAPI_E_USERABORT
- IMAPI_E_GENERIC
- IMAPI_E_MEDIUM_NOTPRESENT
- IMAPI_E_MEDIUM_INVALIDTYPE
- IMAPI_E_DEVICE_NOPROPERTIES
- IMAPI_E_DEVICE_NOTACCESSIBLE
- IMAPI_E_DEVICE_NOTPRESENT
- IMAPI_E_DEVICE_INVALIDTYPE
- IMAPI_E_INITIALIZE_WRITE
- IMAPI_E_INITIALIZE_ENDWRITE
- IMAPI_E_FILESYSTEM
- IMAPI_E_FILEACCESS
- IMAPI_E_DISCINFO
- IMAPI_E_TRACKNOTOPEN
- IMAPI_E_TRACKOPEN
- IMAPI_E_DISCFULL
- IMAPI_E_BADJOLIETNAME
- IMAPI_E_INVALIDIMAGE
- IMAPI_E_NOACTIVEFORMAT
- IMAPI_E_NOACTIVERECORDER
- IMAPI_E_WRONGFORMAT
- IMAPI_E_ALREADYOPEN
- IMAPI_E_WRONGDISC
- IMAPI_E_FILEEXISTS
- IMAPI_E_STASHINUSE
- IMAPI_E_DEVICE_STILL_IN_USE
- IMAPI_E_LOSS_OF_STREAMING
- IMAPI_E_COMPRESSEDSTASH
- IMAPI_E_ENCRYPTEDSTASH
- IMAPI_E_NOTENOUGHDISKFORSTASH
- IMAPI_E_REMOVABLESTASH
- IMAPI_E_CANNOT_WRITE_TO_MEDIA
- IMAPI_E_TRACK_NOT_BIG_ENOUGH
api_location:
- Imapierror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80e8aba2a2d3d12628a45c6716c6f94a405d752f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801138"
---
# <a name="imapiv1-result-codes"></a>Коды результатов IMAPIv1

Методы интерфейсов IMAPI возвращают S \_ ОК, если метод был успешным. В противном случае они возвращают один из следующих кодов результатов.



| Константа/значение                                                                                                                                                                                                                                                                    | Описание                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMAPI_S_PROPERTIESIGNORED"></span><span id="imapi_s_propertiesignored"></span><dl> <dt>**IMAPI \_ \_Пропертиесигноред**</dt> <dt>0x40200</dt> </dl>                   | В наборе свойств было передано неизвестное свойство, которое было пропущено.<br/>                                                                                                                                                                              |
| <span id="IMAPI_S_BUFFER_TO_SMALL"></span><span id="imapi_s_buffer_to_small"></span><dl> <dt>**IMAPI \_ С \_ буферизацией \_ до \_ мелких**</dt> <dt>0x40201</dt> </dl>                       | Выходной буфер слишком мал.<br/>                                                                                                                                                                                                                   |
| <span id="IMAPI_E_NOTOPENED"></span><span id="imapi_e_notopened"></span><dl> <dt>**IMAPI \_ E \_ нотопенед**</dt> <dt>0x8004020b</dt> </dl>                                        | Вызов [**идискмастер:: Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open) не выполнен.<br/>                                                                                                                                                                        |
| <span id="IMAPI_E_NOTINITIALIZED"></span><span id="imapi_e_notinitialized"></span><dl> <dt>**IMAPI \_ E \_ нотинитиализед**</dt> <dt>0x8004020c</dt> </dl>                         | Объект средства записи не инициализирован.<br/>                                                                                                                                                                                                       |
| <span id="IMAPI_E_USERABORT"></span><span id="imapi_e_userabort"></span><dl> <dt>**IMAPI \_ E \_ усераборт**</dt> <dt>0x8004020d</dt> </dl>                                        | Пользователь отменил операцию.<br/>                                                                                                                                                                                                                  |
| <span id="IMAPI_E_GENERIC"></span><span id="imapi_e_generic"></span><dl> <dt>**IMAPI \_ E \_ Generic**</dt> <dt>0x8004020e</dt> </dl>                                              | Произошла общая ошибка.<br/>                                                                                                                                                                                                                         |
| <span id="IMAPI_E_MEDIUM_NOTPRESENT"></span><span id="imapi_e_medium_notpresent"></span><dl> <dt>**IMAPI \_ E \_ Medium \_ нотпресент**</dt> <dt>0x8004020f</dt> </dl>               | На устройстве нет диска.<br/>                                                                                                                                                                                                                   |
| <span id="IMAPI_E_MEDIUM_INVALIDTYPE"></span><span id="imapi_e_medium_invalidtype"></span><dl> <dt>**IMAPI \_ E \_ Medium \_ инвалидтипе**</dt> <dt>0x80040210</dt> </dl>            | Носитель не является типом, который можно использовать.<br/>                                                                                                                                                                                                         |
| <span id="IMAPI_E_DEVICE_NOPROPERTIES"></span><span id="imapi_e_device_noproperties"></span><dl> <dt>**IMAPI \_ 0x80040211 \_ устройства \_ E**</dt> <dt></dt> </dl>         | Средство записи не поддерживает никакие свойства.<br/>                                                                                                                                                                                                     |
| <span id="IMAPI_E_DEVICE_NOTACCESSIBLE"></span><span id="imapi_e_device_notaccessible"></span><dl> <dt>**IMAPI \_ \_ \_ Нотакцессибле устройство E**</dt> <dt>0x80040212</dt> </dl>      | Устройство не может использоваться или уже используется.<br/>                                                                                                                                                                                                   |
| <span id="IMAPI_E_DEVICE_NOTPRESENT"></span><span id="imapi_e_device_notpresent"></span><dl> <dt>**IMAPI \_ \_ \_ Нотпресент устройство E**</dt> <dt>0x80040213</dt> </dl>               | Устройство отсутствует или удалено.<br/>                                                                                                                                                                                                    |
| <span id="IMAPI_E_DEVICE_INVALIDTYPE"></span><span id="imapi_e_device_invalidtype"></span><dl> <dt>**IMAPI \_ \_ \_ Инвалидтипе устройство E**</dt> <dt>0x80040214</dt> </dl>            | Средство записи не поддерживает операцию.<br/>                                                                                                                                                                                                       |
| <span id="IMAPI_E_INITIALIZE_WRITE"></span><span id="imapi_e_initialize_write"></span><dl> <dt>**IMAPI \_ E \_ инициализация \_ записи**</dt> <dt>ошибки: 0x80040215</dt> </dl>                  | Не удалось инициализировать интерфейс диска для записи.<br/>                                                                                                                                                                                         |
| <span id="IMAPI_E_INITIALIZE_ENDWRITE"></span><span id="imapi_e_initialize_endwrite"></span><dl> <dt>**IMAPI \_ E \_ инициализация \_ ENDWRITE**</dt> <dt>0x80040216</dt> </dl>         | Не удалось инициализировать интерфейс диска для закрытия.<br/>                                                                                                                                                                                         |
| <span id="IMAPI_E_FILESYSTEM"></span><span id="imapi_e_filesystem"></span><dl> <dt>**IMAPI \_ 0x80040217 \_ Файловая система**</dt> <dt></dt> </dl>                                     | Произошла ошибка при включении или отключении доступа к файловой системе или во время обнаружения автоматической вставки.<br/>                                                                                                                                                 |
| <span id="IMAPI_E_FILEACCESS"></span><span id="imapi_e_fileaccess"></span><dl> <dt>**IMAPI \_ E \_ FILEACCESS**</dt> <dt>0x80040218</dt> </dl>                                     | Произошла ошибка при записи файла изображения.<br/>                                                                                                                                                                                                   |
| <span id="IMAPI_E_DISCINFO"></span><span id="imapi_e_discinfo"></span><dl> <dt>**IMAPI \_ E \_ дисЦинфо**</dt> <dt>0x80040219</dt> </dl>                                           | Произошла ошибка при попытке чтения данных диска с устройства.<br/>                                                                                                                                                                                 |
| <span id="IMAPI_E_TRACKNOTOPEN"></span><span id="imapi_e_tracknotopen"></span><dl> <dt>**IMAPI \_ E \_ траккнотопен**</dt> <dt>0x8004021a</dt> </dl>                               | Звуковая дорожка не открыта для записи.<br/>                                                                                                                                                                                                           |
| <span id="IMAPI_E_TRACKOPEN"></span><span id="imapi_e_trackopen"></span><dl> <dt>**IMAPI \_ E \_ траккопен**</dt> <dt>0x8004021b</dt> </dl>                                        | Открытая звуковая дорожка уже размещена.<br/>                                                                                                                                                                                                      |
| <span id="IMAPI_E_DISCFULL"></span><span id="imapi_e_discfull"></span><dl> <dt>**IMAPI \_ E \_ дискфулл**</dt> <dt>0x8004021c</dt> </dl>                                           | Диск не может содержать больше данных.<br/>                                                                                                                                                                                                               |
| <span id="IMAPI_E_BADJOLIETNAME"></span><span id="imapi_e_badjolietname"></span><dl> <dt>**IMAPI \_ E \_ баджолиетнаме**</dt> <dt>0x8004021d</dt> </dl>                            | Приложение попыталось добавить на диск неверно именованный элемент.<br/>                                                                                                                                                                                     |
| <span id="IMAPI_E_INVALIDIMAGE"></span><span id="imapi_e_invalidimage"></span><dl> <dt>**IMAPI \_ E \_ инвалидимаже**</dt> <dt>0x8004021e</dt> </dl>                               | Промежуточное изображение не подходит для записи. Она повреждена или удалена и не содержит пригодного для использования содержимого.<br/>                                                                                                                                          |
| <span id="IMAPI_E_NOACTIVEFORMAT"></span><span id="imapi_e_noactiveformat"></span><dl> <dt>**IMAPI \_ E \_ ноактивеформат**</dt> <dt>0x8004021f</dt> </dl>                         | Активный образец формата не был выбран с помощью [**идискмастер:: сетактиведискмастерформат**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscmasterformat).<br/>                                                                                                      |
| <span id="IMAPI_E_NOACTIVERECORDER"></span><span id="imapi_e_noactiverecorder"></span><dl> <dt>**IMAPI \_ E \_ ноактиверекордер**</dt> <dt>0x80040220</dt> </dl>                   | Активный записывающий диск не выбран с помощью [**идискмастер:: сетактиведискрекордер**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder).<br/>                                                                                                              |
| <span id="IMAPI_E_WRONGFORMAT"></span><span id="imapi_e_wrongformat"></span><dl> <dt>**IMAPI \_ E \_ вронгформат**</dt> <dt>0x80040221</dt> </dl>                                  | Вызов [**ижолиетдискмастер**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) был выполнен, когда [**иредбукдискмастер**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster) является активным форматом, или наоборот. Чтобы использовать другой формат, измените формат и очистите содержимое файла изображения.<br/> |
| <span id="IMAPI_E_ALREADYOPEN"></span><span id="imapi_e_alreadyopen"></span><dl> <dt>**IMAPI \_ E \_ алреадйопен**</dt> <dt>0x80040222</dt> </dl>                                  | Вызов [**идискмастер:: Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open) для этого объекта в приложении уже выполнен.<br/>                                                                                                                            |
| <span id="IMAPI_E_WRONGDISC"></span><span id="imapi_e_wrongdisc"></span><dl> <dt>**IMAPI \_ E \_ вронгдиск**</dt> <dt>0x80040223</dt> </dl>                                        | Диск с несколькими сеансами IMAPI был удален из активного устройства записи.<br/>                                                                                                                                                                           |
| <span id="IMAPI_E_FILEEXISTS"></span><span id="imapi_e_fileexists"></span><dl> <dt>**IMAPI \_ E \_ FILEEXISTS**</dt> <dt>0x80040224</dt> </dl>                                     | Добавляемый файл уже находится в файле образа, а флаг перезаписи не установлен.<br/>                                                                                                                                                                  |
| <span id="IMAPI_E_STASHINUSE"></span><span id="imapi_e_stashinuse"></span><dl> <dt>**IMAPI \_ E \_ сташинусе**</dt> <dt>0x80040225</dt> </dl>                                     | Другое приложение уже использует файл образа IMAPI, необходимый для размещения образа диска. Повторите попытку позже.<br/>                                                                                                                                        |
| <span id="IMAPI_E_DEVICE_STILL_IN_USE"></span><span id="imapi_e_device_still_in_use"></span><dl> <dt>**IMAPI \_ \_Устройство E \_ по-прежнему \_ \_ используется**</dt> <dt>0x80040226</dt> </dl>       | Это устройство уже используется другим приложением, поэтому IMAPI не может получить доступ к устройству.<br/>                                                                                                                                                              |
| <span id="IMAPI_E_LOSS_OF_STREAMING"></span><span id="imapi_e_loss_of_streaming"></span><dl> <dt>**IMAPI \_ \_Потери \_ \_ потоковой передачи**</dt> <dt>0x80040227</dt> </dl>              | Потоковая передача содержимого потеряна; возможно, произошло переполнение буфера.<br/>                                                                                                                                                                                 |
| <span id="IMAPI_E_COMPRESSEDSTASH"></span><span id="imapi_e_compressedstash"></span><dl> <dt>**IMAPI \_ E \_ компресседсташ**</dt> <dt>0x80040228</dt> </dl>                      | Скрытый том находится на сжатом томе и не может быть прочитан.<br/>                                                                                                                                                                                   |
| <span id="IMAPI_E_ENCRYPTEDSTASH"></span><span id="imapi_e_encryptedstash"></span><dl> <dt>**IMAPI \_ E \_ енкриптедсташ**</dt> <dt>0x80040229</dt> </dl>                         | Скрытый объект находится на зашифрованном томе и не может быть прочитан.<br/>                                                                                                                                                                                   |
| <span id="IMAPI_E_NOTENOUGHDISKFORSTASH"></span><span id="imapi_e_notenoughdiskforstash"></span><dl> <dt>**IMAPI \_ E \_ нотенаугхдискфорсташ**</dt> <dt>0x8004022a</dt> </dl>    | Недостаточно свободного места для создания файла образа на указанном томе.<br/>                                                                                                                                                                  |
| <span id="IMAPI_E_REMOVABLESTASH"></span><span id="imapi_e_removablestash"></span><dl> <dt>**IMAPI \_ E \_ ремоваблесташ**</dt> <dt>0x8004022b</dt> </dl>                         | Выбранное расположение образа находится на съемном носителе.<br/>                                                                                                                                                                                              |
| <span id="IMAPI_E_CANNOT_WRITE_TO_MEDIA"></span><span id="imapi_e_cannot_write_to_media"></span><dl> <dt>**IMAPI \_ E \_ не удается выполнить \_ запись \_ на \_ носитель**</dt> <dt>0x8004022c</dt> </dl> | Не удается записать на носитель.<br/>                                                                                                                                                                                                                   |
| <span id="IMAPI_E_TRACK_NOT_BIG_ENOUGH"></span><span id="imapi_e_track_not_big_enough"></span><dl> <dt>**IMAPI \_ E \_ имеет \_ \_ \_ недостаточный размер**</dt> <dt>0x8004022d</dt> </dl>    | Эта запись недостаточно велика.<br/>                                                                                                                                                                                                                      |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Имапиеррор. h</dt> </dl> |



 

 





