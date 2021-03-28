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
ms.openlocfilehash: 4367551cdf2d48a06c633329ad850c3f7c2e0976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272845"
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

## <a name="remarks"></a>Примечания

Если обновление завершилось неудачно, вызывающий объект должен освободить память.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 




