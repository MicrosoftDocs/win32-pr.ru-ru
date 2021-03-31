---
title: Сообщение LVM_SETTILEINFO (Коммктрл. h)
description: Задает сведения для существующей плитки элемента управления "представление списка".
ms.assetid: 345e8f16-9a6c-44e3-a262-d5d3be4d33ef
keywords:
- Элементы управления Windows для LVM_SETTILEINFO сообщений
topic_type:
- apiref
api_name:
- LVM_SETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489e163955b8f9cbf99ad25357b5be5a5d5981fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135587"
---
# <a name="lvm_settileinfo-message"></a>\_Сообщение LVM сеттилеинфо

Задает сведения для существующей плитки элемента управления "представление списка".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Указатель на структуру <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**лвтилеинфо**</a> , содержащую сведения, которые необходимо задать.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="remarks"></a>Комментарии

**LVM \_ СЕТТИЛЕИНФО** не поддерживается в стиле [**LVS \_ овнердата**](list-view-window-styles.md) .

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





