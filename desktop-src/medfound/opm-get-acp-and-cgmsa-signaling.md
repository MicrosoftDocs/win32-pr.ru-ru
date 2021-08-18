---
description: 'Дополнительные сведения: OPM_GET_ACP_AND_CGMSA_SIGNALING'
ms.assetid: d477fe3e-4498-450b-93b7-ce74ae9ed005
title: OPM_GET_ACP_AND_CGMSA_SIGNALING (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6c06da78ea9ae1a4f0ea58f0fb8770dffadff6a34d577fd2328816ffc100e4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102068"
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



 

## <a name="remarks"></a>Remarks

Этот запрос эквивалентен \_ запросу дксва коппкуерисигналинг, используемому в сертифицированном протоколе защиты выходных данных (Копп).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                |
| Header<br/>                   | <dl> <dt>Опмапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Иопмвидеуутпут:: Коппкомпатиблежетинформатион**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**Иопмвидеуутпут:: о.**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Запросы состояния ОПМ](opm-status-requests.md)
</dt> </dl>

 

 




