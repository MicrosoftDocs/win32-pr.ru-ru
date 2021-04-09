---
title: Сообщение RB_GETBARINFO (Коммктрл. h)
description: Извлекает сведения об элементе управления "Главная панель" и используемом в нем списке изображений.
ms.assetid: d3d56b95-7540-4e45-bb2e-b9d41cfcca0d
keywords:
- Элементы управления Windows для RB_GETBARINFO сообщений
topic_type:
- apiref
api_name:
- RB_GETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d224c7c826bad0d5d6ae76ce5a4c2266632fa8a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071809"
---
# <a name="rb_getbarinfo-message"></a>\_Сообщение ЖЕТБАРИНФО RB

Извлекает сведения об элементе управления "Главная панель" и используемом в нем списке изображений.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**ребаринфо**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) , которая будет принимать сведения об элементе управления главной панели. Перед отправкой этого сообщения необходимо задать для элемента **кбсизе** этой структуры значение **sizeof**(ребаринфо).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение в случае успеха или ноль в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





