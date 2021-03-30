---
title: Перечисление WINBIO_CREDENTIAL_TYPE (Винбио \_ types. h)
description: Определяет флаги, которые можно использовать для фильтрации по типу учетных данных.
ms.assetid: 7ef2d4b3-e1f9-46a0-8fc2-0e8660805ac3
keywords:
- API биометрическая платформа Windows перечисления WINBIO_CREDENTIAL_TYPE
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_TYPE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae41693db264308d33bc30191bdb73007b6b2dba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892673"
---
# <a name="winbio_credential_type-enumeration"></a>\_Перечисление типов учетных данных винбио \_

Определяет флаги, которые можно использовать для фильтрации по типу учетных данных. Это перечисление используется функциями [**винбиосеткредентиал**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential), [**винбиоремовекредентиал**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)и [**винбиожеткредентиалстате**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) .

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _WINBIO_CREDENTIAL_TYPE { 
  WINBIO_CREDENTIAL_PASSWORD  = 0x00000001,
  WINBIO_CREDENTIAL_ALL       = 0xffffffff
} WINBIO_CREDENTIAL_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WINBIO_CREDENTIAL_PASSWORD"></span><span id="winbio_credential_password"></span>**\_пароль учетных данных винбио \_**
</dt> <dd>

Фильтрует учетные данные пароля.

</dd> <dt>

<span id="WINBIO_CREDENTIAL_ALL"></span><span id="winbio_credential_all"></span>**ВИНБИО \_ учетные данные \_**
</dt> <dd>

Фильтрует все учетные данные.

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
</dt> <dt>

[**винбиоремовекредентиал**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
</dt> <dt>

[**винбиосеткредентиал**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

 





