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
ms.openlocfilehash: dad068c6838f0a3a675970b7c9359b12ea8faa2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988428"
---
# <a name="winbio_identity_type-constants"></a>\_ \_ Константы типа идентификатора винбио

Для указания формата сведений об удостоверении, содержащихся в структуре [**\_ удостоверений винбио**](winbio-identity.md) , можно использовать следующие константы **\_ \_ типа идентификатора винбио** .



| Константа                                                                                                                                                                                      | Описание                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <dt>**\_тип идентификатора \_ винбио \_ null**</dt> </dl>             | Шаблон не имеет связанного идентификатора. <br/>            |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <dt>**\_ \_ шаблон типа идентификатора \_ винбио**</dt> </dl> | Структура соответствует всем удостоверениям шаблона.<br/> |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <dt>**\_ \_ GUID типа идентификатора \_ винбио**</dt> </dl>             | Идентификатор GUID идентифицирует шаблон.<br/>                |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <dt>**ИД \_ \_ безопасности типа \_ идентификатора винбио**</dt> </dl>                | Идентификатор безопасности учетной записи идентифицирует шаблон.<br/>        |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                                    |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (include винбио. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы клиентского приложения](client-application-constants.md)
</dt> <dt>

[**\_удостоверение винбио**](winbio-identity.md)
</dt> </dl>

 

 





