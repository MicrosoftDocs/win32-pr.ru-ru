---
description: Получает состояния автоскрытия и постоянного верхнего уровня для панели задач Windows.
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
ms.openlocfilehash: 71225cd8d93de09a07cb0049066e52be08c18a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342872"
---
# <a name="abm_getstate-message"></a>Сообщение АБМ о \_ состоянии

Получает состояния автоскрытия и постоянного верхнего уровня для панели задач Windows.


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



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Код возврата</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>ABS_ALWAYSONTOP</strong></dt> </dl></td>
<td>Панель задач находится в состоянии Always On (верхнее). <br/>
<blockquote>
[!Note]<br />
Начиная с Windows 7 ABS_ALWAYSONTOP больше не возвращается, так как панель задач всегда находится в этом состоянии. Старый код следует обновлять, чтобы не учитывать отсутствие этого значения, если это значение не предполагает, что возвращаемое значение означает, что панель задач не находится в состоянии Always On (верхнее).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>ABS_AUTOHIDE</strong></dt> </dl></td>
<td>Панель задач находится в состоянии автоскрытия.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Шеллапи. h</dt> </dl> |



 

 




