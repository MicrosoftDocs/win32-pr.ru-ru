---
title: Общие константы (Винбио \_ types. h)
description: Укажите максимальную длину SID, дескрипторы, идентификаторы, максимальную длину строки и максимальный размер буфера выборки.
ms.assetid: 62e87bd8-a708-4d00-aaa8-9cac8e3736a7
topic_type:
- apiref
api_name:
- SECURITY_MAX_SID_SIZE
- WINBIO_UNIT_ID
- WINBIO_SESSION_HANDLE
- WINBIO_FRAMEWORK_HANDLE
- WINBIO_UUID
- WINBIO_STRING
- WINBIO_MAX_STRING_LEN
- WINBIO_MAX_SAMPLE_BUFFER_SIZE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 686e94c936855d3b5466071fba7d8b629a492579de11a53a62d8b23345707c53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119740453"
---
# <a name="general-constants-winbio_typesh"></a>Общие константы (Винбио \_ types. h)

во всех биометрическая платформа Windows используются следующие константы.



| Константа/значение                                                                                                                                                                                                                                                                   | Описание                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| <span id="SECURITY_MAX_SID_SIZE"></span><span id="security_max_sid_size"></span><dl> <dt>**\_максимальный \_ размер SID \_ безопасности**</dt> </dl>                                                                                          | Максимальная длина значения идентификатора безопасности (SID). В настоящее время это 68.<br/>   |
| <span id="WINBIO_UNIT_ID"></span><span id="winbio_unit_id"></span><dl> <dt>**\_идентификатор единицы \_ винбио**</dt> </dl>                                                                                                                | ИДЕНТИФИКАЦИОНный номер биометрического блока.<br/>                                                   |
| <span id="WINBIO_SESSION_HANDLE"></span><span id="winbio_session_handle"></span><dl> <dt>**\_обработчик сеанса \_ винбио**</dt> </dl>                                                                                           | Длинное целое число без знака, содержащее маркер открытого биометрического сеанса.<br/> |
| <span id="WINBIO_FRAMEWORK_HANDLE"></span><span id="winbio_framework_handle"></span><dl> <dt>**\_обработчик винбио Framework \_**</dt> </dl>                                                                                     | Длинное целое число без знака, содержащее маркер открытого сеанса инфраструктуры.<br/> |
| <span id="WINBIO_UUID"></span><span id="winbio_uuid"></span><dl> <dt>**\_UUID винбио**</dt> </dl>                                                                                                                          | Идентификатор GUID.<br/>                                                                          |
| <span id="WINBIO_STRING"></span><span id="winbio_string"></span><dl> <dt>**\_строка винбио**</dt> </dl>                                                                                                                    | Массив байтов, содержащий строку в Юникоде, завершающуюся нулем.<br/>                     |
| <span id="WINBIO_MAX_STRING_LEN_"></span><span id="winbio_max_string_len_"></span><dl> <dt>**Винбио \_ Максимальная \_ \_ Длина строки**</dt> </dl>                                                                                       | Максимальная длина **\_ строкового значения винбио** . В настоящее время это 256.<br/>         |
| <span id="WINBIO_MAX_SAMPLE_BUFFER_SIZE"></span><span id="winbio_max_sample_buffer_size"></span><dl> <dt>**Винбио \_ МАКСИМАЛЬНЫЙ \_ \_ \_ Размер буфера выборки**</dt> ( <dt>0x7FFFFFFF</dt> ) </dl> | Максимальное число байт в одной биометрической записи данных.<br/>                  |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                                    |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                                       |
| Заголовок<br/>                   | <dl> <dt>Винбио \_ types. h (include винбио. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Константы клиентского приложения](client-application-constants.md)
</dt> </dl>

 

 





