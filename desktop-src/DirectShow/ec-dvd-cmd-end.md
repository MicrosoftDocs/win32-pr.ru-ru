---
description: Сигнализирует о завершении определенной команды DVD-навигатора.
ms.assetid: f460db8e-b966-41fa-bfa1-4ad3fa65c3e3
title: EC_DVD_CMD_END (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_END
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 869da360f3321059df81a609d5ce953ad64f60485126fe7ae8f5e5a7df21753a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965884"
---
# <a name="ec_dvd_cmd_end"></a>\_Завершение команды DVD-диска EC \_ \_

Сигнализирует о завершении определенной команды [DVD-навигатора](dvd-navigator-filter.md) .

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Идентификатор команды. Передайте этот параметр в метод [**IDvdInfo2:: жеткмдфромевент**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) , чтобы получить указатель интерфейса [**идвдкмд**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) .

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Значение **HRESULT** , указывающее состояние команды.

</dd> </dl>

## <a name="remarks"></a>Remarks

Это событие возникает только в том случае, если приложение устанавливает флаг SendEvents для флага DVD \_ cmd \_ \_ в методе [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) , принимающем флаг [**\_ \_ флагов DVD-диска**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) .

Это событие возникает в домене Title.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Двдевкоде. h (включение DShow. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[DVD-приложения](dvd-applications.md)
</dt> <dt>

[Коды уведомлений о событиях DVD](dvd-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Синхронизация команд DVD](synchronizing-dvd-commands.md)
</dt> </dl>

 

 




