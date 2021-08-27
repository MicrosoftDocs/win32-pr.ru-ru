---
description: получает состояния "автоматическое скрытие" и "всегда на начало" Windows панели задач.
title: Сообщение ABM_GETSTATE (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 18e16752-16be-492b-a4fa-c951e18dc86c
api_name:
- ABM_GETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1ced01e3f8186a82e99f408f91546ebcbb117ed9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466391"
---
# <a name="abm_getstate-message"></a>Сообщение АБМ о \_ состоянии

получает состояния "автоматическое скрытие" и "всегда на начало" Windows панели задач.


```C++
uState = (UINT) SHAppBarMessage(ABM_GETSTATE, pabd);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пабд* 
</dt> <dd>

Указатель на структуру [**аппбардата**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . При отправке этого сообщения необходимо указать элемент **кбсизе** . все остальные элементы игнорируются.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль, если панель задач не находится ни в режиме автоскрытия, ни в состоянии Always On (верхнее). В противном случае возвращаемое значение будет одним из следующих:




| Код возврата | Описание | 
|-------------|-------------|
| <dl><dt><strong>ABS_ALWAYSONTOP</strong></dt></dl> | Панель задач находится в состоянии Always On (верхнее). <br /><blockquote>[!Note]<br />начиная с Windows 7 ABS_ALWAYSONTOP больше не возвращается, так как панель задач всегда находится в этом состоянии. Старый код следует обновлять, чтобы не учитывать отсутствие этого значения, если это значение не предполагает, что возвращаемое значение означает, что панель задач не находится в состоянии Always On (верхнее).</blockquote><br /> | 
| <dl><dt><strong>ABS_AUTOHIDE</strong></dt></dl> | Панель задач находится в состоянии автоскрытия.<br /> | 




 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Шеллапи. h</dt> </dl> |



 

 




