---
title: Сообщение EM_SETCARETINDEX (Коммктрл. h)
description: Задает значение индекса (с отсчетом от нуля) позиции курсора в элементе управления "поле ввода".
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- Элементы управления Windows для EM_SETCARETINDEX сообщений
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
ms.openlocfilehash: ea0c49ebad91532e82dc7e96facb62f38b2abfa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492471"
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

## <a name="remarks"></a>Комментарии

Если индекс выходит за пределы диапазона текста в элементе управления "поле ввода", индекс будет настроен таким образом, чтобы он поместился внутри диапазона текста.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, \[ только классические приложения 1809\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2019\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**EM \_ жеткаретиндекс**](em-getcaretindex.md)
</dt> </dl>

 

 





