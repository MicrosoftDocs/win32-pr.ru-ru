---
title: Сообщение EM_SEARCHWEB (Коммктрл. h)
description: Открывает браузер и выполняет поиск в Интернете с выбранным текстом в качестве условия поиска.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- Элементы управления Windows для EM_SEARCHWEB сообщений
topic_type:
- apiref
api_name:
- EM_SEARCHWEB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e83c18db47d18648797ee3d58fe12567af941b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892394"
---
# <a name="em_searchweb-message"></a>\_Сообщение СЕАРЧВЕБ EM

Открывает браузер и выполняет поиск в Интернете с выбранным текстом в качестве условия поиска.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется; должно быть равно нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это сообщение не возвращает значение.

## <a name="remarks"></a>Комментарии

Если функция "Поиск в Интернете" отключена с помощью сообщения [**EM \_ енаблесеарчвеб**](em-enablesearchweb.md) , это сообщение не действует.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, \[ только классические приложения 1809\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2019\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EM \_ енаблесеарчвеб**](em-enablesearchweb.md)
</dt> </dl>

 

 





