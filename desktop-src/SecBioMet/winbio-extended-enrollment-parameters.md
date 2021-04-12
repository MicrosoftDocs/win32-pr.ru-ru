---
title: Структура WINBIO_EXTENDED_ENROLLMENT_PARAMETERS (Винбио \_ Adapter. h)
description: Содержит дополнительные сведения о том, что адаптеру подсистемы требуется создать шаблон регистрации.
ms.assetid: E8007316-0A9D-4F35-A266-273B2406D545
keywords:
- API структуры WINBIO_EXTENDED_ENROLLMENT_PARAMETERS биометрическая платформа Windows
- PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS API биометрическая платформа Windows указателя структуры
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f041d131bcee540a75a131b4179947fbe8e394
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489558"
---
# <a name="winbio_extended_enrollment_parameters-structure"></a>\_ \_ Структура параметров расширенной регистрации винбио \_

Структура **\_ \_ \_ параметров расширенной регистрации винбио** содержит дополнительные сведения о том, что адаптеру подсистемы требуется создать шаблон регистрации.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_PARAMETERS {
  SIZE_T                   Size;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
} WINBIO_EXTENDED_ENROLLMENT_PARAMETERS, *PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS;
```



## <a name="members"></a>Члены

<dl> <dt>

**Размер**
</dt> <dd>

Размер (в байтах) структуры **\_ \_ \_ параметров расширенной регистрации винбио** .

</dd> <dt>

**Подфакт**
</dt> <dd>

Один из [**\_ биометрического \_ подтипа Винбио**](winbio-biometric-subtype-constants.md) содержит значения констант, которые предоставляют дополнительные сведения о регистрации.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Биометрическая платформа Windows передает эту структуру методу [**енгинеадаптерсетенроллментпараметерс**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) во время операции регистрации.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                                                     |
| Header<br/>                   | <dl> <dt>Винбио \_ Adapter. h (включить винбио \_ Adapter. h)</dt> </dl> |



 

 





