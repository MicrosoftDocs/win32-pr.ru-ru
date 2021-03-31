---
title: Сообщение TCM_GETITEMRECT (Коммктрл. h)
description: Извлекает ограничивающий прямоугольник для вкладки в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл жетитемрект.
ms.assetid: 6abd8cdf-5f19-4b7e-800e-970097bc891b
keywords:
- Элементы управления Windows для TCM_GETITEMRECT сообщений
topic_type:
- apiref
api_name:
- TCM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa6c214efbeeaf58d1ff3def9f50f10011b41dfc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892533"
---
# <a name="tcm_getitemrect-message"></a>\_Сообщение ЖЕТИТЕМРЕКТ TCM

Извлекает ограничивающий прямоугольник для вкладки в элементе управления "Вкладка". Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ жетитемрект**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemrect) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс вкладки.

</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая получает ограничивающий прямоугольник вкладки в координатах окна просмотра.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

