---
title: Сообщение LVM_GETGROUPINFO (Коммктрл. h)
description: Возвращает сведения о группе.
ms.assetid: 72d84e0b-121e-473b-a34d-874234c598b6
keywords:
- Элементы управления Windows для LVM_GETGROUPINFO сообщений
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b55d5b1d781e7749df97bd0c9f7782f56545dbee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071457"
---
# <a name="lvm_getgroupinfo-message"></a>\_Сообщение LVM жетграупинфо

Возвращает сведения о группе.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Идентификатор, указывающий группу, сведения о которой извлекаются.</dd> <dt>

*lParam* 
</dt> <dd>Указатель на структуру <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**лвграуп**</a> , которая получает извлеченные сведения. Задайте для элемента **кбсизе** этой структуры значение sizeof (лвграуп). </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает идентификатор группы в случае успеха или значение-1 в противном случае.

## <a name="remarks"></a>Комментарии

Прежде чем пытаться получить заголовок для группы, сначала убедитесь, что у группы нет \_ стиля лбгс.

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





