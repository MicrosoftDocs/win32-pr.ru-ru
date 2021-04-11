---
title: Сообщение TVM_MAPHTREEITEMTOACCID (Коммктрл. h)
description: Сопоставляет ХТРИИТЕМ с ИДЕНТИФИКАТОРом специальных возможностей.
ms.assetid: 87ef0785-88c1-49f4-8a05-872577e16fe4
keywords:
- Элементы управления Windows для TVM_MAPHTREEITEMTOACCID сообщений
topic_type:
- apiref
api_name:
- TVM_MAPHTREEITEMTOACCID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6267c2040583917283fc444db74ddacbdabd69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135926"
---
# <a name="tvm_maphtreeitemtoaccid-message"></a>\_Сообщение TVM мафтриитемтоакЦид

Сопоставляет **хтриитем** с идентификатором специальных возможностей.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>**Хтриитем** , сопоставленный с идентификатором специальных возможностей.</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает идентификатор специальных возможностей.

## <a name="remarks"></a>Комментарии

При добавлении элемента в элемент управления "дерево" возвращается маркер **хтриитем** , который однозначно определяет элемент.

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

[**\_МафтриитемтоакЦид TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_maphtreeitemtoaccid)
</dt> </dl>

 

 





