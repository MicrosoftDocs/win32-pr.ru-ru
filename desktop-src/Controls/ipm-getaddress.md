---
title: Сообщение IPM_GETADDRESS (Коммктрл. h)
description: Возвращает значения адреса для всех четырех полей в элементе управления IP-адреса.
ms.assetid: 4fe68d45-7d7f-46da-a110-65f899b3c393
keywords:
- элементы управления Windows сообщений IPM_GETADDRESS
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
ms.openlocfilehash: e9bcb35ed71532e815b33b45e1c15e9b82b75b5c87fac406b52de80670e3d72a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434516"
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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Коммктрл. h</dt> </dl> |



 

 





