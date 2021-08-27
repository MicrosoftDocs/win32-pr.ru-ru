---
title: Сообщение TB_INSERTMARKHITTEST (Коммктрл. h)
description: Извлекает данные метки вставки для точки на панели инструментов.
ms.assetid: 65c64fd0-f089-4b1a-84e5-1a3e10aa7f5e
keywords:
- элементы управления Windows сообщений TB_INSERTMARKHITTEST
topic_type:
- apiref
api_name:
- TB_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbc231b915d6d71cc22ee3cd98b1c6dd602451cc3c70d2153ba1bee8a0d55657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061364"
---
# <a name="tb_insertmarkhittest-message"></a>\_Сообщение ИНСЕРТМАРКХИТТЕСТ ТБ

Извлекает данные метки вставки для точки на панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указатель на структуру [**точек**](/previous-versions//dd162805(v=vs.85)) , содержащую координаты проверки попадания относительно клиентской области панели инструментов.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**тбинсертмарк**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) , которая получает сведения о метке вставки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое значение, если точка является отметкой вставки, или ноль в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

