---
description: 'Вызывается выходным центром доверия (OTA), когда метод Имфаутпуттрустаусорити:: Сетполици завершается асинхронно.'
ms.assetid: c5d8a88e-2864-45a0-97b7-051341116a4c
title: Событие Меполицисет (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 238af6cbd740e62825ae0b661769c1cf1bf880ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711570"
---
# <a name="mepolicyset-event"></a>Событие Меполицисет

Вызывается выходным центром доверия (OTA), когда метод [**имфаутпуттрустаусорити:: сетполици**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) завершается асинхронно.

## <a name="event-values"></a>Значения событий

Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.



| VARTYPE              | Описание                           |
|----------------------|---------------------------------------|
| VT \_ пуст<br/> | Нет данных события.<br/> <br/> |
| VT \_ UI4<br/> | Идентификатор, который можно задать для [имфаутпутполици](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) с помощью атрибута [MF_POLICY_ID](mf-policy-id.md) .<br/> <br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[События Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




