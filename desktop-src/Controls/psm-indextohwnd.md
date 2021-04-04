---
title: Сообщение PSM_INDEXTOHWND (Пршт. h)
description: Принимает индекс страницы свойств и возвращает его маркер окна. Это сообщение можно отправить явным образом или использовать макрос Пропшит \_ индекстохвнд.
ms.assetid: 93b46b4c-47f9-4ce8-8797-f3d4bd5248e9
keywords:
- Элементы управления Windows для PSM_INDEXTOHWND сообщений
topic_type:
- apiref
api_name:
- PSM_INDEXTOHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 788b1dd0e7312f301051d9a57fcdec43f3f2f72a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136954"
---
# <a name="psm_indextohwnd-message"></a>\_Сообщение ПСМ индекстохвнд

Принимает индекс страницы свойств и возвращает его маркер окна. Это сообщение можно отправить явным образом или использовать макрос [**пропшит \_ индекстохвнд**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextohwnd) .

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Отсчитываемый от нуля индекс страницы.

</dd> <dt>

*lParam* 
</dt> <dd>

Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер окна страницы свойств, заданного параметром *wParam* , если выполнено успешно. В противном случае возвращается ноль.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                               |
| Header<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |



 

 





