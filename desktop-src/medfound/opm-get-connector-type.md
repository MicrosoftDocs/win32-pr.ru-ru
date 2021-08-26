---
description: Возвращает тип физического соединителя для выходного видео.
ms.assetid: c5862758-0125-4dbe-af72-5ed4a85bd702
title: OPM_GET_CONNECTOR_TYPE (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3099da66193048b52011e58eb5ce3f925d451fc1ad26b193f2955f6012f0e607
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887504"
---
# <a name="opm_get_connector_type"></a>ОПМ \_ получить \_ \_ Тип соединителя

Возвращает тип физического соединителя для выходного видео.



| Требование | Значение |
|--------------|-----------------------------------------------------------------------------|
| GUID запроса | ОПМ \_ получить \_ \_ Тип соединителя                                                   |
| Входные данные   | Нет                                                                        |
| Возвращать данные  | [**\_ Стандартная \_ информационная структура ОПМ**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) |



 

## <a name="remarks"></a>Remarks

Тип соединителя возвращается в элементе **улинформатион** [**\_ \_ информационной структуры ОПМ Standard**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . Значение **улинформатион** равно одному из типов соединителей, перечисленных в списке [**флагов типа соединителя ОПМ**](opm-connector-type-flags.md).

В режиме эмуляции Копп тип соединителя может сочетаться с **\_ \_ \_ \_ \_ внутренним флагом типа соединителя ОПМ Копп Compatible** . Используйте побитовое **и** для извлечения типа соединителя:

`ulInformation & ~OPM_COPP_COMPATIBLE_CONNECTOR_TYPE_INTERNAL`

Приложения должны игнорировать **внутренний флаг \_ \_ \_ \_ типа \_ соединителя ОПМ Копп Compatible** . Дополнительные сведения см. в подразделе "Примечания" [**флагов типа соединителя ОПМ**](opm-connector-type-flags.md).

Этот запрос эквивалентен \_ запросу дксва коппкуериконнектортипе, используемому в сертифицированном протоколе защиты выходных данных (Копп).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                      |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Опмапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Иопмвидеуутпут:: Коппкомпатиблежетинформатион**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[**Иопмвидеуутпут:: о.**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[Запросы состояния ОПМ](opm-status-requests.md)
</dt> </dl>

 

 




