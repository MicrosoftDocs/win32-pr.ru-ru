---
title: Сообщение CB_SETCUEBANNER (Winuser. h)
description: Задает текст баннера подсказки, отображаемый для элемента управления "поле ввода" поля со списком.
ms.assetid: 4b2b5042-ba64-4e3f-adeb-9aea66773b0e
keywords:
- Элементы управления Windows для CB_SETCUEBANNER сообщений
topic_type:
- apiref
api_name:
- CB_SETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5799b1b1be5e938ce1e234948a1f7d878122f30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071610"
---
# <a name="cb_setcuebanner-message"></a>\_Сообщение СЕТКУЕБАННЕР CB

Задает текст баннера подсказки, отображаемый для элемента управления "поле ввода" поля со списком.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Должен равняться нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на завершающийся нулем буфер строки в Юникоде, содержащий текст.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает 1 в случае успеха или значение ошибки в противном случае.

## <a name="remarks"></a>Комментарии

Баннер подсказки — это текст, отображаемый в элементе управления "поле со списком" при отсутствии выделения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Возможности поля со списком](combo-box-features.md)
</dt> </dl>

 

 





