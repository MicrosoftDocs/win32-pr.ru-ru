---
title: Сообщение IPM_GETADDRESS (Коммктрл. h)
description: Возвращает значения адреса для всех четырех полей в элементе управления IP-адреса.
ms.assetid: 4fe68d45-7d7f-46da-a110-65f899b3c393
keywords:
- Элементы управления Windows для IPM_GETADDRESS сообщений
topic_type:
- apiref
api_name:
- IPM_GETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 426e9c76712701b2f4e108679133be23eb700687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988911"
---
# <a name="ipm_getaddress-message"></a>Сообщение IPM. \_ Address

Возвращает значения адреса для всех четырех полей в элементе управления IP-адреса.

## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>Должен равняться нулю.</dd> <dt>

*lParam* 
</dt> <dd>

Указатель на значение **DWORD** , получающее адрес. Значение поля 3 будет содержаться в битах от 0 до 7. Значение поля 2 будет содержаться в битах 8 – 15. Значение поля 1 будет содержаться в битах от 16 до 23. Значение поля 0 будет содержаться в битах с 24 по 31. Для извлечения сведений об адресе также можно использовать [**первый \_ IP**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)-адрес, [**второй \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress), [**третий \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)и [**четвертый \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) . Ноль будет возвращен в качестве адреса для любых пустых полей.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает количество непустых полей.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





