---
description: Возвращает список механизмов защиты, поддерживаемых соединителем.
ms.assetid: dd4cdd3c-6bb5-4427-827d-f3e909e752e5
title: OPM_GET_SUPPORTED_PROTECTION_TYPES (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eddc6f4006f9692ec6152875cda412191b87d247e907d33b615aa6d4fb89748e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012544"
---
# <a name="opm_get_supported_protection_types"></a>ОПМ \_ получить \_ поддерживаемые \_ \_ типы защиты

Возвращает список механизмов защиты, поддерживаемых соединителем.



| Требование | Значение |
|--------------|-----------------------------------------------------------------------------|
| GUID запроса | ОПМ \_ получить \_ поддерживаемые \_ \_ типы защиты                                      |
| Входные данные   | Нет                                                                        |
| Возвращать данные  | [**\_ Стандартная \_ информационная структура ОПМ**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Remarks

Механизмы защиты возвращаются в элементе **улинформатион** [**\_ \_ информационной структуры ОПМ Standard**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . Значение представляет собой побитовое **или** для [флагов типа защиты ОПМ](opm-protection-type-flags.md).

Этот запрос эквивалентен \_ запросу дксва коппкуерипротектионтипе, используемому в сертифицированном протоколе защиты выходных данных (Копп).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Опмапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Иопмвидеуутпут:: Коппкомпатиблежетинформатион**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**Иопмвидеуутпут:: о.**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Запросы состояния ОПМ](opm-status-requests.md)
</dt> </dl>

 

 




