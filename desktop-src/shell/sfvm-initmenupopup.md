---
description: 'позволяет объекту обратного вызова изменять всплывающее меню Windows Explorer перед отображением. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_INITMENUPOPUP (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9d7e96e9-c52e-43bd-945b-05db33c8dfd0
api_name:
- SFVM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: fd69d19f753c1c72c1e0c143a0aface2cdb234cb2ace8c87d559834b97bbf0f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592324"
---
# <a name="sfvm_initmenupopup-message"></a>\_Сообщение сфвм инитменупопуп

позволяет объекту обратного вызова изменять всплывающее меню Windows Explorer перед отображением. Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_INITMENUPOPUP 

    wParam = (WPARAM)(int) idCmd,nIndex;

    lParam = (LPARAM)(HMENU) hmenu;

            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*идкмд \_ ниндекс* \[ в\]
</dt> <dd>

Младшее слово этого параметра содержит значение первого идентификатора команды, зарезервированного для клиентских команд. Слово в высоком порядке содержит индекс меню.

</dd> <dt>

*HMENU* \[ в, out\]
</dt> <dd>

Маркер меню.

</dd> </dl>

## <a name="remarks"></a>Remarks

Объект представления системных папок отправляет это сообщение, если выбрано меню, но перед его отображением. Обработайте это сообщение, если, например, необходимо включить или отключить команды меню. Всплывающее меню может быть следующим:

-   Меню файл, Правка или вид.
-   Меню верхнего уровня, определенное клиентом.
-   Определяемое клиентом подменю.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Шлобж. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**СФВМ \_ мержемену**](sfvm-mergemenu.md)
</dt> </dl>

 

 
