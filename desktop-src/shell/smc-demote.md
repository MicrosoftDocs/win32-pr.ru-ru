---
description: Понизить элемент, указанный в сопровождающей структуре СМДАТА.
title: Сообщение SMC_DEMOTE (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4809fbd1-da66-4453-b4f2-e75cb5b3457c
api_name:
- SMC_DEMOTE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 46e5505571402feec24d81a9184b713e1c61ae0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997795"
---
# <a name="smc_demote-message"></a>SMC \_ понизить сообщение

Понизить элемент, указанный в сопровождающей структуре [**смдата**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .


```C++
SMC_DEMOTE
            
```



## <a name="parameters"></a>Параметры

Это сообщение не содержит параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвратите \_ ОК.

## <a name="remarks"></a>Примечания

Это уведомление получает метод [**ишеллменукаллбакк:: каллбакксм**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 




