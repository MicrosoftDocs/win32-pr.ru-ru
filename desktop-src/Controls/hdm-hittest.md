---
title: Сообщение HDM_HITTEST (Коммктрл. h)
description: Проверяет точку, чтобы определить, какой элемент заголовка, если таковой имеется, находится в указанной точке.
ms.assetid: ff866bd1-9f2a-457c-921d-549610ab9088
keywords:
- элементы управления Windows сообщений HDM_HITTEST
topic_type:
- apiref
api_name:
- HDM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cc219640d9dd9d5d9a4c9537169401f681e37660554266b3edd653365cf8cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544774"
---
# <a name="hdm_hittest-message"></a>\_Сообщение HITTEST HDM

Проверяет точку, чтобы определить, какой элемент заголовка, если таковой имеется, находится в указанной точке.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**хдхиттестинфо**](/windows/win32/api/commctrl/ns-commctrl-hdhittestinfo) , которая содержит позиции для проверки и получает сведения о результатах теста.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает индекс элемента в указанной позиции, если таковой имеется, или значение 1 в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





