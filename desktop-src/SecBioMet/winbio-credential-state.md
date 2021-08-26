---
title: Перечисление WINBIO_CREDENTIAL_STATE (Винбио \_ types. h)
description: Определяет значения, указывающие, связаны ли учетные данные с биометрических данных конечного пользователя.
ms.assetid: c24f1771-7a1f-403e-8100-dfb3f4cd77a1
keywords:
- API биометрическая платформа Windows перечисления WINBIO_CREDENTIAL_STATE
- API биометрическая платформа Windows указателя перечисления PWINBIO_CREDENTIAL_STATE
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_STATE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce0e176479a68d39b017e852e17a73691b8349d7c6faa6be62130007a09dcef0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868064"
---
# <a name="winbio_credential_state-enumeration"></a>\_Перечисление состояния учетных данных винбио \_

Определяет значения, указывающие, связаны ли учетные данные с биометрических данных конечного пользователя. Это перечисление используется функцией [**винбиожеткредентиалстате**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) .

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _WINBIO_CREDENTIAL_STATE { 
  WINBIO_CREDENTIAL_NOT_SET  = 0x00000001,
  WINBIO_CREDENTIAL_SET      = 0x00000002
} WINBIO_CREDENTIAL_STATE, *PWINBIO_CREDENTIAL_STATE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**\_учетные данные винбио \_ не \_ заданы**
</dt> <dd>

Учетные данные были связаны с конечным пользователем.

</dd> <dt>

<span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**\_набор учетных данных винбио \_**
</dt> <dd>

Учетные данные не связаны с конечным пользователем.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                                    |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                                       |
| Заголовок<br/>                   | <dl> <dt>Винбио \_ types. h (include винбио. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Перечисления клиентских приложений](client-application-enumerations.md)
</dt> <dt>

[**винбиожеткредентиалстате**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> </dl>

 

 





