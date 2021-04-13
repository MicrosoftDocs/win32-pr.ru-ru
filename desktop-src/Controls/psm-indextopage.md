---
title: Сообщение PSM_INDEXTOPAGE (Пршт. h)
description: Принимает индекс страницы свойств и возвращает его обработчик ХПРОПШИТПАЖЕ. Это сообщение можно отправить явным образом или использовать макрос Пропшит \_ индекстопаже.
ms.assetid: b14b35ad-bae0-4461-a90f-e2bc5e2ccfc2
keywords:
- Элементы управления Windows для PSM_INDEXTOPAGE сообщений
topic_type:
- apiref
api_name:
- PSM_INDEXTOPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38f7a5658dbd92f4208e084f1df47a4dc3582156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492132"
---
# <a name="psm_indextopage-message"></a>\_Сообщение ПСМ индекстопаже

Принимает индекс страницы свойств и возвращает его обработчик ХПРОПШИТПАЖЕ. Это сообщение можно отправить явным образом или использовать макрос [**пропшит \_ индекстопаже**](/windows/desktop/api/Prsht/nf-prsht-propsheet_indextopage) .

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

Возвращает маркер ХПРОПШИТПАЖЕ страницы свойств, указанный параметром *wParam* в случае успеха. В противном случае возвращается ноль.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                               |
| Header<br/>                   | <dl> <dt>Пршт. h</dt> </dl> |



 

 





