---
title: Сообщение LVM_SORTGROUPS (Коммктрл. h)
description: Использует определяемую приложением функцию сравнения для сортировки групп по ИДЕНТИФИКАТОРу в элементе управления "представление списка".
ms.assetid: 553e96d6-a982-4482-8fba-ef11a74fb82e
keywords:
- Элементы управления Windows для LVM_SORTGROUPS сообщений
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
ms.openlocfilehash: 2c70fd0f343c9efe0215c87f430e5ed1c89a3aed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137086"
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

## <a name="remarks"></a>Комментарии

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

[**лвграупкомпаре**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> </dl>

