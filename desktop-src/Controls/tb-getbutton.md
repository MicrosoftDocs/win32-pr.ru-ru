---
title: Сообщение TB_GETBUTTON (Коммктрл. h)
description: Извлекает сведения об указанной кнопке на панели инструментов.
ms.assetid: d90d053c-0daf-4a5a-b7ca-b9b4472c65a3
keywords:
- элементы управления Windows сообщений TB_GETBUTTON
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
ms.openlocfilehash: 9e36d8cd4e382570884b0cb30f7c95615e2342544cab0970e9864e9fde7882f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919034"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





