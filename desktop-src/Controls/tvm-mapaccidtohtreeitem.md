---
title: Сообщение TVM_MAPACCIDTOHTREEITEM (Коммктрл. h)
description: Сопоставляет идентификатор доступа с ХТРИИТЕМ.
ms.assetid: f4feb7cb-2138-4930-b8ee-b9e2d4b19001
keywords:
- Элементы управления Windows для TVM_MAPACCIDTOHTREEITEM сообщений
topic_type:
- apiref
api_name:
- TVM_MAPACCIDTOHTREEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b827b18387723fe4792321f7932e1abb3673466e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071362"
---
# <a name="tvm_mapaccidtohtreeitem-message"></a>\_Сообщение TVM мапакЦидтохтриитем

Сопоставляет идентификатор доступа с **хтриитем**.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>**Uint** , содержащий идентификатор доступа, сопоставляемый с **хтриитем**. </dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **хтриитем** , с которым СОПОСТАВЛЕН указанный идентификатор доступа.

## <a name="remarks"></a>Комментарии

При добавлении элемента в элемент управления представлением в виде дерева возвращается **хтриитем** , который однозначно определяет элемент.

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_МапакЦидтохтриитем TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_mapaccidtohtreeitem)
</dt> </dl>

 

 





