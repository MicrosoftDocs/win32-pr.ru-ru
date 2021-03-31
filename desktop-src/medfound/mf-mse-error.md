---
description: Определяет различные состояния ошибок расширения источника мультимедиа.
ms.assetid: 8FD54833-F60B-49E8-A673-6130F3B06160
title: Перечисление MF_MSE_ERROR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_ERROR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 6b6aaea772376b0e57c006a56a5a1bb30bc497c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155563"
---
# <a name="mf_mse_error-enumeration"></a>\_ \_ Перечисление ошибок MF MSE

Определяет различные состояния ошибок расширения источника мультимедиа.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _MF_MSE_ERROR { 
  MF_MSE_ERROR_NOERROR        =  0,
  MF_MSE_ERROR_NETWORK        = 1,
  MF_MSE_ERROR_DECODE         = 2,
  MF_MSE_ERROR_UNKNOWN_ERROR  =  3
} MF_MSE_ERROR;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MF_MSE_ERROR_NOERROR"></span><span id="mf_mse_error_noerror"></span>**MF \_ MSE \_ ошибка ошибки \_**
</dt> <dd>

Не указывает на ошибку.

</dd> <dt>

<span id="MF_MSE_ERROR_NETWORK"></span><span id="mf_mse_error_network"></span>**\_ \_ Сетевая ошибка MF MSE \_**
</dt> <dd>

Указывает ошибку в сети.

</dd> <dt>

<span id="MF_MSE_ERROR_DECODE"></span><span id="mf_mse_error_decode"></span>**\_ \_ расшифровка ошибок MF в MSE \_**
</dt> <dd>

Указывает ошибку при декодировании.

</dd> <dt>

<span id="MF_MSE_ERROR_UNKNOWN_ERROR"></span><span id="mf_mse_error_unknown_error"></span>**MF \_ MSE \_ Ошибка \_ неизвестная \_ Ошибка**
</dt> <dd>

Указывает неизвестную ошибку.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Мфмедиаенгине. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Media Foundation](media-foundation-enumerations.md)
</dt> </dl>

 

 




