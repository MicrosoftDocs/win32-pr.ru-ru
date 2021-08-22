---
title: Сообщение EM_SEARCHWEB (Коммктрл. h)
description: Открывает браузер и выполняет поиск в Интернете с выбранным текстом в качестве условия поиска.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- элементы управления Windows сообщений EM_SEARCHWEB
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
ms.openlocfilehash: 21523df67acf91b8a44f59ea40b012f1af7c287185b7ac64b5dc1288005dfb17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118673180"
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

## <a name="remarks"></a>Remarks

Если функция "Поиск в Интернете" отключена с помощью сообщения [**EM \_ енаблесеарчвеб**](em-enablesearchweb.md) , это сообщение не действует.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, \[ только классические приложения 1809\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2019\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**EM \_ енаблесеарчвеб**](em-enablesearchweb.md)
</dt> </dl>

 

 





