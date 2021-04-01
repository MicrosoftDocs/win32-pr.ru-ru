---
title: Сообщение PSM_INDEXTOID (Пршт. h)
description: Принимает индекс страницы свойств и возвращает идентификатор ресурса. Это сообщение можно отправить явным образом или использовать макрос Пропшит \_ индекстоид.
ms.assetid: c153675a-360f-4916-aa0b-500636dd9022
keywords:
- Элементы управления Windows для PSM_INDEXTOID сообщений
topic_type:
- apiref
api_name:
- PSM_INDEXTOID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643861ecb6dc11d949483defc282d6d65648bdca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071777"
---
# <a name="psm_indextoid-message"></a>\_Сообщение ПСМ индекстоид

Принимает индекс страницы свойств и возвращает идентификатор ресурса. Это сообщение можно отправить явным образом или использовать макрос [**пропшит \_ индекстоид**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextoid) .

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

Возвращает идентификатор ресурса страницы свойств, указанной параметром *wParam* в случае успеха. В противном случае возвращается ноль.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                               |
| Header<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |



 

 





