---
title: Сообщение CB_SETCUEBANNER (Winuser. h)
description: Задает текст баннера подсказки, отображаемый для элемента управления "поле ввода" поля со списком.
ms.assetid: 4b2b5042-ba64-4e3f-adeb-9aea66773b0e
keywords:
- элементы управления Windows сообщений CB_SETCUEBANNER
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
ms.openlocfilehash: cb546b7113247f09d8929364984d5e73c3e28b6541d2ca04bd631405040bf6fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089044"
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

## <a name="remarks"></a>Remarks

Баннер подсказки — это текст, отображаемый в элементе управления "поле со списком" при отсутствии выделения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Возможности поля со списком](combo-box-features.md)
</dt> </dl>

 

 





