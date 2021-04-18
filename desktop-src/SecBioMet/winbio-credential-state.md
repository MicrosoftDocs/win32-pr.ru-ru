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
ms.openlocfilehash: 3f8b8292cbbaefeeda0f6bf349f55e8f825f1756
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340425"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                                    |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (include винбио. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления клиентских приложений](client-application-enumerations.md)
</dt> <dt>

[**винбиожеткредентиалстате**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> </dl>

 

 





