---
title: Константы WINBIO_IDENTITY_TYPE (Винбио \_ types. h)
description: Укажите формат сведений об удостоверении, содержащихся в \_ структуре удостоверений винбио.
ms.assetid: 27A01538-9B26-4A29-8ADB-ED9C5D5808B3
topic_type:
- apiref
api_name:
- WINBIO_ID_TYPE_NULL
- WINBIO_ID_TYPE_WILDCARD
- WINBIO_ID_TYPE_GUID
- WINBIO_ID_TYPE_SID
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2f0e51d30e45b16dd7683d746cdef7ab5f75aaf62611102dd4dcd3e7bd07c8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910196"
---
# <a name="winbio_identity_type-constants"></a>\_ \_ Константы типа идентификатора винбио

Для указания формата сведений об удостоверении, содержащихся в структуре [**\_ удостоверений винбио**](winbio-identity.md) , можно использовать следующие константы **\_ \_ типа идентификатора винбио** .



| Константа                                                                                                                                                                                      | Описание                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <dt>**\_тип идентификатора \_ винбио \_ null**</dt> </dl>             | Шаблон не имеет связанного идентификатора. <br/>            |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <dt>**\_ \_ шаблон типа идентификатора \_ винбио**</dt> </dl> | Структура соответствует всем удостоверениям шаблона.<br/> |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <dt>**\_ \_ GUID типа идентификатора \_ винбио**</dt> </dl>             | Идентификатор GUID идентифицирует шаблон.<br/>                |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <dt>**ИД \_ \_ безопасности типа \_ идентификатора винбио**</dt> </dl>                | Идентификатор безопасности учетной записи идентифицирует шаблон.<br/>        |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                                    |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (include винбио. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы клиентского приложения](client-application-constants.md)
</dt> <dt>

[**\_удостоверение винбио**](winbio-identity.md)
</dt> </dl>

 

 





