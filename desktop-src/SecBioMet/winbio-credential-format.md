---
title: Перечисление WINBIO_CREDENTIAL_FORMAT (Винбио \_ types. h)
description: Определяет флаги, которые можно использовать для указания формата учетных данных конечного пользователя.
ms.assetid: f107e000-98a2-44f0-aa5e-d13b5d9c8d43
keywords:
- API биометрическая платформа Windows перечисления WINBIO_CREDENTIAL_FORMAT
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa28ea56c7af9f78947e64587740300a70f763ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135910"
---
# <a name="winbio_credential_format-enumeration"></a>\_Перечисление форматов учетных данных винбио \_

Определяет флаги, которые можно использовать для указания формата учетных данных конечного пользователя. Это перечисление используется функцией [**винбиосеткредентиал**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) .

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _WINBIO_CREDENTIAL_FORMAT { 
  WINBIO_PASSWORD_GENERIC    = 0x00000001,
  WINBIO_PASSWORD_PACKED     = 0x00000002,
  WINBIO_PASSWORD_PROTECTED  = 0x00000003
} WINBIO_CREDENTIAL_FORMAT;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**\_универсальный пароль \_ винбио**
</dt> <dd>

Пароль имеет общий формат.

</dd> <dt>

<span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**ВИНБИО \_ пароль \_**
</dt> <dd>

Пароль имеет сжатый формат.

</dd> <dt>

<span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**\_защищен паролем винбио \_**
</dt> <dd>

Учетные данные пароля были заключены в оболочку с помощью [**кредпротект**](/windows/desktop/api/wincred/nf-wincred-credprotecta).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                                                  |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (include винбио. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления клиентских приложений](client-application-enumerations.md)
</dt> <dt>

[**винбиосеткредентиал**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

