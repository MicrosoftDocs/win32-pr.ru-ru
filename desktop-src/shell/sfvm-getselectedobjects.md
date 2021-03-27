---
description: Извлекает массив указателей на списки идентификаторов элементов (PIDL) для всех выбранных объектов. Используется \_ сообщением шшеллфолдервиев.
title: Сообщение SFVM_GETSELECTEDOBJECTS (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9639fbb6-d0ef-49b1-b3c5-e6a1dee0b7ad
api_name:
- SFVM_GETSELECTEDOBJECTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 056a9bd6bea78ef5093f6654b9935eb90e3759ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913315"
---
# <a name="sfvm_getselectedobjects-message"></a>\_Сообщение сфвм жетселектедобжектс

Извлекает массив указателей на списки идентификаторов элементов (PIDL) для всех выбранных объектов. Используется [**\_ сообщением шшеллфолдервиев**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_GETSELECTEDOBJECTS 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппидл* \[ заполняет\]
</dt> <dd>Адрес массива PIDL объектов, выбранных в данный момент.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает число элементов в массиве.

## <a name="remarks"></a>Примечания

По завершении необходимо вызвать [**илфри**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) для каждого члена массива, чтобы освободить память.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 




