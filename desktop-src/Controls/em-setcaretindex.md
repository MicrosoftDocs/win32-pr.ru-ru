---
title: Сообщение EM_SETCARETINDEX (Коммктрл. h)
description: Задает значение индекса (с отсчетом от нуля) позиции курсора в элементе управления "поле ввода".
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- элементы управления Windows сообщений EM_SETCARETINDEX
topic_type:
- apiref
api_name:
- EM_SETCARETINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 8b80202ed5294828441abcfa66a914514e31944902e52926de7fa3af92794b46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799964"
---
# <a name="em_setcaretindex-message"></a>\_Сообщение СЕТКАРЕТИНДЕКС EM

Задает значение индекса (с отсчетом от нуля) позиции курсора в элементе управления "поле ввода".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Новое значение индекса (с отсчетом от нуля) позиции курсора.

</dd> <dt>

*lParam* 
</dt> <dd>Должен равняться нулю.</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="remarks"></a>Remarks

Если индекс выходит за пределы диапазона текста в элементе управления "поле ввода", индекс будет настроен таким образом, чтобы он поместился внутри диапазона текста.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, \[ только классические приложения 1809\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2019\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**EM \_ жеткаретиндекс**](em-getcaretindex.md)
</dt> </dl>

 

 





