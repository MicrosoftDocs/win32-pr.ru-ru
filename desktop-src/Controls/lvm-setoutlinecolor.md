---
title: Сообщение LVM_SETOUTLINECOLOR (Коммктрл. h)
description: Задает цвет границы элемента управления "представление списка", если \_ \_ установлен расширенный стиль окна LVS ex бордерселект.
ms.assetid: c2b606fa-8d47-4192-94b7-d01c3cfdc514
keywords:
- Элементы управления Windows для LVM_SETOUTLINECOLOR сообщений
topic_type:
- apiref
api_name:
- LVM_SETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 776cb13479e4d091d394941844691c117a4ebbef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891442"
---
# <a name="lvm_setoutlinecolor-message"></a>\_Сообщение LVM сетаутлинеколор

Задает цвет границы элемента управления "представление списка", если установлен расширенный стиль окна [**LVS \_ ex \_ бордерселект**](extended-list-view-styles.md) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>Структура **COLORREF** , указывающая цвет для задания границы.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает структуру **COLORREF** , содержащую цвет контура.

## <a name="remarks"></a>Комментарии

> [!Note]  
> Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0. Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





