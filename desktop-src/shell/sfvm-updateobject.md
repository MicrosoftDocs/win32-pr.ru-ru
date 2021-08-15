---
description: Обновляет объект, передавая указатель на массив двух указателей на списки идентификаторов элементов (PIDL). Используется \_ сообщением шшеллфолдервиев.
title: Сообщение SFVM_UPDATEOBJECT (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3bd68ace-3ccf-446c-8cf9-52f42444674e
api_name:
- SFVM_UPDATEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1e3c4ee64583710e84af0d377999c389f6fe1bfa6876bb150789a5fd118f79f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452856"
---
# <a name="sfvm_updateobject-message"></a>\_Сообщение сфвм UPDATEOBJECT

Обновляет объект, передавая указатель на массив двух указателей на списки идентификаторов элементов (PIDL). Используется [**\_ сообщением шшеллфолдервиев**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++

                SFVM_UPDATEOBJECT 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппидл* \[ окне\]
</dt> <dd>

Адрес массива из двух PIDL. Первый ПИДЛ является старым ПИДЛ. Второй — копия старого ПИДЛ с обновленной информацией. Управление временем существования копии принадлежит к представлению после успешного завершения этого вызова.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает идентификатор ListView обновленного объекта, если обновление прошло успешно. в противном случае возвращается значение-1.

## <a name="remarks"></a>Remarks

Если обновление завершилось неудачно, вызывающий объект должен освободить память.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 




