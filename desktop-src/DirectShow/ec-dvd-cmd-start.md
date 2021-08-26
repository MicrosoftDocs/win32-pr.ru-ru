---
description: Сигнализирует о начале команды DVD Navigator.
ms.assetid: 230116b4-23f1-4c37-a781-da2c5aa20a1f
title: EC_DVD_CMD_START (Двдевкоде. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_START
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 418163b55699f8ba7c38026764f3326985d7e1788369729f42067cff62a56949
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998084"
---
# <a name="ec_dvd_cmd_start"></a>\_Запуск команды DVD-диска EC \_ \_

Сигнализирует о начале команды [DVD Navigator](dvd-navigator-filter.md) .

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

Это событие возникает только в том случае, если приложение устанавливает флаг **\_ \_ \_ SendEvents** для флага DVD cmd в методе [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) , принимающем флаг [**\_ \_ флагов DVD-диска**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) .

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

 

 




