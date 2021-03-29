---
description: Возвращает список механизмов защиты, поддерживаемых соединителем.
ms.assetid: dd4cdd3c-6bb5-4427-827d-f3e909e752e5
title: OPM_GET_SUPPORTED_PROTECTION_TYPES (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1dc79b33673e34d00914b84165d915baa0d8f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991420"
---
# <a name="opm_get_supported_protection_types"></a>ОПМ \_ получить \_ поддерживаемые \_ \_ типы защиты

Возвращает список механизмов защиты, поддерживаемых соединителем.



| Требование | Значение |
|--------------|-----------------------------------------------------------------------------|
| GUID запроса | ОПМ \_ получить \_ поддерживаемые \_ \_ типы защиты                                      |
| Входные данные   | Нет                                                                        |
| Возвращать данные  | [**\_ Стандартная \_ информационная структура ОПМ**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Комментарии

Механизмы защиты возвращаются в элементе **улинформатион** [**\_ \_ информационной структуры ОПМ Standard**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . Значение представляет собой побитовое **или** для [флагов типа защиты ОПМ](opm-protection-type-flags.md).

Этот запрос эквивалентен \_ запросу дксва коппкуерипротектионтипе, используемому в сертифицированном протоколе защиты выходных данных (Копп).

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

 

 




