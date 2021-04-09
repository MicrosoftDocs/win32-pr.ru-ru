---
title: Сообщение TVM_SELECTITEM (Коммктрл. h)
description: Выбирает указанный элемент представления дерева, прокручивает элемент в представлении или перерисовывает элемент в стиле, который используется для указания цели операции перетаскивания.
ms.assetid: 8b943958-7b93-4e54-99de-200121cf0752
keywords:
- Элементы управления Windows для TVM_SELECTITEM сообщений
topic_type:
- apiref
api_name:
- TVM_SELECTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94862b64a02cd8972e3da38a75282d99bbc1cbc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891597"
---
# <a name="tvm_selectitem-message"></a>\_Сообщение TVM селектитем

Выбирает указанный элемент представления дерева, прокручивает элемент в представлении или перерисовывает элемент в стиле, который используется для указания цели операции перетаскивания. Это сообщение можно отправить явным образом или с помощью макроса [**\_ SELECT TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select), [**TreeView \_ селектитем**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)или [**TreeView \_ селектдроптаржет**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Флаг действия. Этот параметр может принимать одно из следующих значений:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Значение</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="TVGN_CARET"></span><span id="tvgn_caret"></span><dl> <dt><strong>TVGN_CARET</strong></dt> </dl></td>
<td>Задает выборку для указанного элемента. Родительское окно элемента управления представлением дерева получает <a href="tvn-selchanging.md">TVN_SELCHANGING</a> и <a href="tvn-selchanged.md">TVN_SELCHANGED</a> коды уведомления. <br/></td>
</tr>
<tr class="even">
<td><span id="TVGN_DROPHILITE"></span><span id="tvgn_drophilite"></span><dl> <dt><strong>TVGN_DROPHILITE</strong></dt> </dl></td>
<td>Перерисовывает указанный элемент в стиле, который используется для указания цели операции перетаскивания.<br/></td>
</tr>
<tr class="odd">
<td><span id="TVGN_FIRSTVISIBLE"></span><span id="tvgn_firstvisible"></span><dl> <dt><strong>TVGN_FIRSTVISIBLE</strong></dt> </dl></td>
<td>Гарантирует, что указанный элемент является видимым, и, если это возможно, отображает его в верхней части окна элемента управления. Элементы управления "дерево-представление" отображают столько элементов, сколько будет помещаться в окне. Если указанный элемент находится ближе к нижней части иерархии элементов управления, он может не стать первым видимым элементом в зависимости от того, сколько элементов умещается в окне.<br/></td>
</tr>
<tr class="even">
<td><span id="TVSI_NOSINGLEEXPAND"></span><span id="tvsi_nosingleexpand"></span><dl> <dt><strong>TVSI_NOSINGLEEXPAND</strong></dt> </dl></td>
<td>Если выбран один элемент, гарантирует, что TreeView не расширяет его дочерние элементы. Это допустимо, только если используется с флагом TVGN_CARET. <br/>
<blockquote>
[!Note]<br />
Чтобы использовать этот флаг, необходимо указать манифест, задающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе <a href="cookbook-overview.md">Включение визуальных стилей</a>.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*lParam* 
</dt> <dd>

Обработчик элемента. Если параметр *lParam* имеет **значение NULL**, элементу управления задается значение, не имеющее выбранного элемента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Комментарии

Если указанный элемент является дочерним по отношению к свернутому родительскому элементу, то родительский список дочерних элементов разворачивается для отображения указанного элемента. В этом случае родительское окно элемента управления получает коды уведомлений [ТВН \_ Итемекспандинг](tvn-itemexpanding.md) и [ТВН \_ итемекспандед](tvn-itemexpanded.md) .

Использование макроса [**\_ Селектитем в TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem) эквивалентно отправке **сообщения \_ Селектитем TVM** с параметром *wParam* , равным \_ значению курсора твгн. Использование макроса [**\_ Селектдроптаржет в TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget) эквивалентно отправке сообщения **TVM \_ селектитем** с параметром *wParam* , равным \_ значению твгн дрофилите. Использование [**TreeView \_ селектсетфирствисибле**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible) эквивалентно отправке сообщения **TVM \_ селектитем** с параметром *wParam* , установленным в \_ значение твгн фирствисибле.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





