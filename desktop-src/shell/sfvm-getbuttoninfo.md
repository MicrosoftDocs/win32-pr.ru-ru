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
ms.openlocfilehash: 03991e1d87ed9e607d0e55f2788921db88017499a5e81876f2e4d8622e2f52d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118048561"
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

## <a name="remarks"></a>Remarks

Кнопки можно добавлять или добавлять в начало стандартных кнопок представления объектов в системных папках или отображаться вместо стандартных кнопок. За этим сообщением следует сообщение [**сфвм \_**](sfvm-getbuttons.md) , которое извлекает сведения о характере для кнопки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



 

 
