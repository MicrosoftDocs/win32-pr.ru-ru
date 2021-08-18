---
description: Пользователь щелкнул Шеврон, чтобы развернуть элемент, указанный в соответствующей структуре СМДАТА.
title: Сообщение SMC_CHEVRONEXPAND (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cb0b3cf1-1a12-4236-96e9-cc04360d269f
api_name:
- SMC_CHEVRONEXPAND
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 036c45c6bd0e156a17cbcf2f89d3f64b2f619d4b4a6eb7e0a19b70eb3295292c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968253"
---
# <a name="smc_chevronexpand-message"></a>\_Сообщение SMC чевронекспанд

Пользователь щелкнул Шеврон, чтобы развернуть элемент, указанный в соответствующей структуре [**смдата**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .


```C++
SMC_CHEVRONEXPAND
            
```



## <a name="parameters"></a>Параметры

Это сообщение не содержит параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвратите \_ ОК.

## <a name="remarks"></a>Remarks

Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 




