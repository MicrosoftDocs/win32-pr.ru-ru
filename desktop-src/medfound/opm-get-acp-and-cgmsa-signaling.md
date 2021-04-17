---
description: 'Дополнительные сведения: OPM_GET_ACP_AND_CGMSA_SIGNALING'
ms.assetid: d477fe3e-4498-450b-93b7-ce74ae9ed005
title: OPM_GET_ACP_AND_CGMSA_SIGNALING (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bf6294c3f1d90ac8a2292c65b3c1b8558e69220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711437"
---
# <a name="opm_get_acp_and_cgmsa_signaling"></a>ОПМ \_ Получение \_ \_ сигнала ACP и \_ кгмса \_

Возвращает следующие сведения о выходе видео:

-   Список стандартов защиты телевизионных передач, поддерживаемых драйвером.
-   Стандартный, который активен в данный момент.
-   Текущие пропорции или другие сигнальные данные.



| Требование | Значение |
|--------------|-------------------------------------------------------------------------------------|
| GUID запроса | ОПМ \_ Получение \_ \_ сигнала ACP и \_ кгмса \_                                                |
| Входные данные   | Нет                                                                                |
| Возвращать данные  | Структура [**\_ \_ \_ \_ сигнализации ОПМ и кгмса**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling) |



 

## <a name="remarks"></a>Комментарии

Этот запрос эквивалентен \_ запросу дксва коппкуерисигналинг, используемому в сертифицированном протоколе защиты выходных данных (Копп).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                      |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                |
| Header<br/>                   | <dl> <dt>Опмапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Иопмвидеуутпут:: Коппкомпатиблежетинформатион**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**Иопмвидеуутпут:: о.**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Запросы состояния ОПМ](opm-status-requests.md)
</dt> </dl>

 

 




