---
description: 'Позволяет объекту обратного вызова добавлять кнопки на панель инструментов. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_GETBUTTONINFO (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 983652ed-7309-46aa-a6c9-7516411ba5ac
api_name:
- SFVM_GETBUTTONINFO
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d0db40f7c1f54cd13d54765ba34a8eab31246809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985773"
---
# <a name="sfvm_getbuttoninfo-message"></a>\_Сообщение сфвм жетбуттонинфо

Позволяет объекту обратного вызова добавлять кнопки на панель инструментов. Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETBUTTONINFO 

    lParam = (LPARAM)(LPTBINFO) ptbinfo;

            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птбинфо* \[ заполняет\]
</dt> <dd>

Адрес структуры [**тбинфо**](/windows/desktop/api/Shlobj/ns-shlobj-tbinfo) , указывающей количество кнопок и способ их добавления на панель инструментов.

</dd> </dl>

## <a name="remarks"></a>Примечания

Кнопки можно добавлять или добавлять в начало стандартных кнопок представления объектов в системных папках или отображаться вместо стандартных кнопок. За этим сообщением следует сообщение [**сфвм \_**](sfvm-getbuttons.md) , которое извлекает сведения о характере для кнопки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
