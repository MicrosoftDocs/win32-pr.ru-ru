---
title: Сообщение PBM_SETPOS (Коммктрл. h)
description: Задает текущую точку для индикатора выполнения и перерисовывает линию для отражения новой должности.
ms.assetid: 9ebeaa19-0f42-4af7-85d8-aae22498fd6f
keywords:
- Элементы управления Windows для PBM_SETPOS сообщений
topic_type:
- apiref
api_name:
- PBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a157f6a220f4932d39d13f08df79afa99d7348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654579"
---
# <a name="pbm_setpos-message"></a>\_Сообщение СЕТПОС PBM

Задает текущую точку для индикатора выполнения и перерисовывает линию для отражения новой должности.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Целое число со знаком, которое станет новой позицией.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает предыдущее расположение.

## <a name="remarks"></a>Комментарии

Если параметр *wParam* находится за пределами диапазона элемента управления, то в качестве расположения устанавливается Ближайшая граница.

Не отправляйте это сообщение элементу управления с стилем [**\_ области PBS**](progress-bar-control-styles.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





