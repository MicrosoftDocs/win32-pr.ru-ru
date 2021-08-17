---
description: Определяет различные состояния готовности расширения источника мультимедиа.
ms.assetid: 7455B92F-CC2D-4743-935D-F5EBFD834397
title: Перечисление MF_MSE_READY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_READY
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 28f476c32abbffa8faadd8a7c527f07d81632eee10f1c6cfc54eacc926b4f4e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104580"
---
# <a name="mf_mse_ready-enumeration"></a>\_ \_ Перечисление ГОТОВности MF для MSE

Определяет различные состояния готовности расширения источника мультимедиа.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _MF_MSE_READY { 
  MF_MSE_READY_CLOSED  = 1,
  MF_MSE_READY_OPEN    = 2,
  MF_MSE_READY_ENDED   = 3
} MF_MSE_READY;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MF_MSE_READY_CLOSED"></span><span id="mf_mse_ready_closed"></span>**\_ \_ Готово к закрытию с поддержкой MSE \_**
</dt> <dd>

Источник мультимедиа закрыт.

</dd> <dt>

<span id="MF_MSE_READY_OPEN"></span><span id="mf_mse_ready_open"></span>**\_ \_ ОТКРЫТа MF с поддержкой MSE \_**
</dt> <dd>

Источник мультимедиа открыт.

</dd> <dt>

<span id="MF_MSE_READY_ENDED"></span><span id="mf_mse_ready_ended"></span>**\_ \_ закончено, готово к работе с MSE \_**
</dt> <dd>

Источник мультимедиа завершен.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Мфмедиаенгине. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Media Foundation](media-foundation-enumerations.md)
</dt> </dl>

 

 




