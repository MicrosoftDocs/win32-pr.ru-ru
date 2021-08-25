---
description: Удаляет объект из представления оболочки. Используется \_ сообщением шшеллфолдервиев.
title: Сообщение SFVM_REMOVEOBJECT (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5b493cea-dfbd-4aee-8126-b118c058bb4c
api_name:
- SFVM_REMOVEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d5bb53da276e28d7598961cc8f68a2464f414db9a3eac2ddab769102149bf370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941954"
---
# <a name="sfvm_removeobject-message"></a>\_Сообщение сфвм ремовеобжект

Удаляет объект из представления оболочки. Используется [**\_ сообщением шшеллфолдервиев**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_REMOVEOBJECT 
    lParam = (LPARAM) pidl;
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Пидл* \[ окне\]
</dt> <dd>ПИДЛ объекта, который необходимо удалить.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс элемента, который был удален, если найден элемент, соответствующий указанному ПИДЛ. в противном случае возвращает значение-1.

## <a name="remarks"></a>Remarks

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 




