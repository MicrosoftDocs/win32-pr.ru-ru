---
description: Извлекает маркер панель приложенийа автоскрытия, связанный с границей экрана. Это сообщение расширяет АБМ \_ жетаутохидебар, позволяя указать определенный монитор, который будет использоваться в ситуациях с несколькими мониторами.
title: Сообщение ABM_GETAUTOHIDEBAREX (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 538EA230-06DF-4441-A6AA-9DD613521BE1
api_name:
- ABM_GETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9aecbc81e313c3d971b310cc35bd399b93cc18f2ef2a4f02a00d51a16745eb61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225243"
---
# <a name="abm_getautohidebarex-message"></a>\_Сообщение АБМ жетаутохидебарекс

Извлекает маркер панель приложенийа автоскрытия, связанный с границей экрана. Это сообщение расширяет [**АБМ \_ жетаутохидебар**](abm-getautohidebar.md) , позволяя указать определенный монитор, который будет использоваться в ситуациях с несколькими мониторами.


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пабд* 
</dt> <dd>

Указатель на структуру [**аппбардата**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) , которая указывает границы экрана и монитор. При отправке этого сообщения необходимо указать члены **кбсизе**, **уедже** и **RC** . все остальные элементы игнорируются.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер для панель приложенийа автоскрытия. Возвращаемое значение равно **null** , если возникает ошибка или если панель приложений не связан с данным ребром данного монитора.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Шеллапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**АБМ \_ жетаутохидебар**](abm-getautohidebar.md)
</dt> <dt>

[**АБМ \_ сетаутохидебар**](abm-setautohidebar.md)
</dt> <dt>

[**АБМ \_ сетаутохидебарекс**](abm-setautohidebarex.md)
</dt> </dl>

 

 




