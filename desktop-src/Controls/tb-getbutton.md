---
title: Сообщение TB_GETBUTTON (Коммктрл. h)
description: Извлекает сведения об указанной кнопке на панели инструментов.
ms.assetid: d90d053c-0daf-4a5a-b7ca-b9b4472c65a3
keywords:
- Элементы управления Windows для TB_GETBUTTON сообщений
topic_type:
- apiref
api_name:
- TB_GETBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2080a6c984bb2384f68a1388bd46fe598f5087
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804121"
---
# <a name="tb_getbutton-message"></a>\_Сообщение о кнопке ТБ

Извлекает сведения об указанной кнопке на панели инструментов.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс кнопки, для которой требуется получить сведения.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**тббуттон**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) , которая получает сведения о кнопке.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





