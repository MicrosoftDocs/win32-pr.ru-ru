---
title: Сообщение TB_INSERTMARKHITTEST (Коммктрл. h)
description: Извлекает данные метки вставки для точки на панели инструментов.
ms.assetid: 65c64fd0-f089-4b1a-84e5-1a3e10aa7f5e
keywords:
- Элементы управления Windows для TB_INSERTMARKHITTEST сообщений
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
ms.openlocfilehash: 5237d5a13250c3eb95bfe741415a9da245585c78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071448"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

