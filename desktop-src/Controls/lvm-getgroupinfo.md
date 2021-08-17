---
title: Сообщение LVM_GETGROUPINFO (Коммктрл. h)
description: Возвращает сведения о группе.
ms.assetid: 72d84e0b-121e-473b-a34d-874234c598b6
keywords:
- элементы управления Windows сообщений LVM_GETGROUPINFO
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
ms.openlocfilehash: f5c48a21a1bba0c6dd1af3fd567ea853dc922591c553ea11a935fb705ad65bf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411398"
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

## <a name="remarks"></a>Remarks

Прежде чем пытаться получить заголовок для группы, сначала убедитесь, что у группы нет \_ стиля лбгс.

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





