---
title: Константы WINBIO_POOL (Винбио \_ types. h)
description: Укажите тип пула биометрических единиц, который будет использоваться в сеансе.
ms.assetid: e6e49b95-981a-477d-9889-ea132db5b387
topic_type:
- apiref
api_name:
- WINBIO_POOL_UNKNOWN
- WINBIO_POOL_SYSTEM
- WINBIO_POOL_PRIVATE
- WINBIO_POOL_UNASSIGNED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fefc43bb9dc4cefbde1ce5622853a3ba2cfae498ff2f8f81e97417e306641db9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909801"
---
# <a name="winbio_pool-constants"></a>\_Константы пула винбио

Следующие константы можно использовать в функции [**винбиупенсессион**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) для указания типа пула биометрических единиц, который будет использоваться в сеансе.



| Константа                                                                                                                                                                                  | Описание                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <dt>**\_неизвестный пул винбио \_**</dt> </dl>          | Неизвестный тип пула.<br/>                                                         |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <dt>**\_система пула \_ винбио**</dt> </dl>             | Указывает общую коллекцию биометрических модулей, управляемых поставщиком услуг.<br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <dt>**\_частный пул \_ винбио**</dt> </dl>          | Указывает коллекцию биометрических единиц, управляемых вызывающим объектом.<br/>         |
| <span id="WINBIO_POOL_UNASSIGNED"></span><span id="winbio_pool_unassigned"></span><dl> <dt>**пул ВИНБИО не \_ \_ назначен**</dt> </dl> | Зарезервировано.<br/>                                                                         |



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                                    |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (include винбио. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы клиентского приложения](client-application-constants.md)
</dt> </dl>

 

 





