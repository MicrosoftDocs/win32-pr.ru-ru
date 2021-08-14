---
title: Константы WINBIO_SETTING_SOURCE (Винбио \_ types. h)
description: определите, включена ли в данный момент биометрическая платформа Windows.
ms.assetid: d95aa6cc-ddff-40fb-ab82-eac78dc0cb6b
topic_type:
- apiref
api_name:
- WINBIO_SETTING_SOURCE_INVALID
- WINBIO_SETTING_SOURCE_DEFAULT
- WINBIO_SETTING_SOURCE_POLICY
- WINBIO_SETTING_SOURCE_LOCAL
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f02a5edc80d00d098a592626ad4d9f0e1030f9f6eee119bf615375680d11842
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909322"
---
# <a name="winbio_setting_source-constants"></a>\_ \_ Константы источника параметра винбио

функция [**винбиожетенабледсеттинг**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting) использует следующие константы для определения того, включена ли в данный момент биометрическая платформа Windows. Константы указывают, где был создан параметр.



| Константа                                                                                                                                                                                                        | Описание                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| <span id="WINBIO_SETTING_SOURCE_INVALID"></span><span id="winbio_setting_source_invalid"></span><dl> <dt>**\_ \_ Недопустимый источник параметра винбио \_**</dt> </dl> | Недопустимый параметр.<br/>                              |
| <span id="WINBIO_SETTING_SOURCE_DEFAULT"></span><span id="winbio_setting_source_default"></span><dl> <dt>**\_Источник параметра \_ винбио \_ по умолчанию**</dt> </dl> | Этот параметр создан из встроенной политики.<br/>           |
| <span id="WINBIO_SETTING_SOURCE_POLICY"></span><span id="winbio_setting_source_policy"></span><dl> <dt>**\_ \_ Политика источника параметра \_ винбио**</dt> </dl>    | Этот параметр создан в реестре локального компьютера.<br/> |
| <span id="WINBIO_SETTING_SOURCE_LOCAL"></span><span id="winbio_setting_source_local"></span><dl> <dt>**\_ \_ Локальная настройка источника винбио \_**</dt> </dl>       | Этот параметр был создан групповая политика<br/>                |



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

 

 





