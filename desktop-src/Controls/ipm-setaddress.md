---
title: Сообщение IPM_SETADDRESS (Коммктрл. h)
description: Задает значения адреса для всех четырех полей в элементе управления "IP-адрес".
ms.assetid: 52e72437-3558-4789-844f-5ab5b0b7967c
keywords:
- элементы управления Windows сообщений IPM_SETADDRESS
topic_type:
- apiref
api_name:
- IPM_SETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54817d2206295432e9b477532268a000fc43047ae928ab02224d668912474519
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434494"
---
# <a name="ipm_setaddress-message"></a>\_Сообщение IPM сетаддресс

Задает значения адреса для всех четырех полей в элементе управления "IP-адрес".

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Значение **типа DWORD** , содержащее новый адрес. Значение поля 3 содержится в битах от 0 до 7. Значение поля 2 содержится в битах от 8 до 15. Значение поля 1 содержится в битах от 16 до 23. Значение поля 0 содержится в битах с 24 по 31. Для создания сведений об адресе также можно использовать макрос [**макеипаддресс**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение не используется.

## <a name="remarks"></a>Remarks

Это сообщение не создает уведомление [**ИПН \_ фиелдчанжед**](ipn-fieldchanged.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





