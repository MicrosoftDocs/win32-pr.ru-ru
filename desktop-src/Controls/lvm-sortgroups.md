---
title: Сообщение LVM_SORTGROUPS (Коммктрл. h)
description: Использует определяемую приложением функцию сравнения для сортировки групп по ИДЕНТИФИКАТОРу в элементе управления "представление списка".
ms.assetid: 553e96d6-a982-4482-8fba-ef11a74fb82e
keywords:
- элементы управления Windows сообщений LVM_SORTGROUPS
topic_type:
- apiref
api_name:
- LVM_SORTGROUPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ec17d46205746495cfe95a2af83690644dd8bfced26041906bdea4f809fb36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670788"
---
# <a name="lvm_sortgroups-message"></a>\_Сообщение LVM сортграупс

Использует определяемую приложением функцию сравнения для сортировки групп по ИДЕНТИФИКАТОРу в элементе управления "представление списка".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Указатель на определяемую приложением функцию сравнения <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">лвграупкомпаре</a>.</dd> <dt>

*lParam* 
</dt> <dd>Указатель void на сведения, определяемые приложением.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает 1, если успешно, или 0 в противном случае.

## <a name="remarks"></a>Remarks

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**лвграупкомпаре**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> </dl>

