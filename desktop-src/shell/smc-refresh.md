---
description: Отправляет уведомление о том, что меню полностью Обновлено, и вы можете сбросить состояние.
title: Сообщение SMC_REFRESH (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8c79d9d5-b7dc-4271-9edb-93b40606c9be
api_name:
- SMC_REFRESH
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 31ac0164ed3cd69dbeb71adc44c6e3a15b9092db79c7972800068dc06a378786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047005"
---
# <a name="smc_refresh-message"></a>\_Сообщение об обновлении SMC

Отправляет уведомление о том, что меню полностью Обновлено, и вы можете сбросить состояние.


```C++
SMC_REFRESH
            
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



 

 




