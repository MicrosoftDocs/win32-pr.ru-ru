---
description: В следующей таблице приведены коды ошибок, относящиеся к объектам мультимедиа Microsoft DirectX (дмос). Эти коды ошибок определены в файле заголовка Медиаерр. h.
ms.assetid: 1ded5656-084d-4315-a414-aebf4a1820dc
title: Коды ошибок DMO (Медиаерр. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76c8cd5e7001751cd2cf9eb7da4d88b2dc100bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652215"
---
# <a name="dmo-error-codes"></a>Коды ошибок DMO

В следующей таблице приведены коды ошибок, относящиеся к объектам мультимедиа Microsoft DirectX (дмос). Эти коды ошибок определены в файле заголовка Медиаерр. h.



| Константа/значение                                                                                                                                                                                                                                                  | Описание                                                                                                                                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMO_E_INVALIDSTREAMINDEX"></span><span id="dmo_e_invalidstreamindex"></span><dl> <dt>**DMO \_ E \_ инвалидстреаминдекс**</dt> <dt>0x80040201</dt> </dl> | Недопустимый индекс потока.<br/>                                                                                                                                    |
| <span id="DMO_E_INVALIDTYPE"></span><span id="dmo_e_invalidtype"></span><dl> <dt>**DMO \_ E \_ инвалидтипе**</dt> <dt>0x80040202</dt> </dl>                      | Недопустимый тип носителя.<br/>                                                                                                                                      |
| <span id="DMO_E_TYPE_NOT_SET"></span><span id="dmo_e_type_not_set"></span><dl> <dt>**DMO \_ \_Тип E \_ не \_ задан**</dt> <dt>0x80040203</dt> </dl>                 | Тип носителя не задан. Перед выполнением этой операции для одного или нескольких потоков требуется тип мультимедиа.<br/>                                                 |
| <span id="DMO_E_NOTACCEPTING"></span><span id="dmo_e_notaccepting"></span><dl> <dt>**DMO \_ E \_ нотакцептинг**</dt> <dt>0x80040204</dt> </dl>                   | Данные не могут быть приняты в этом потоке. Может потребоваться обработка дополнительных выходных данных. см. раздел [**имедиаобжект::P роцессинпут**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput).<br/> |
| <span id="DMO_E_TYPE_NOT_ACCEPTED"></span><span id="dmo_e_type_not_accepted"></span><dl> <dt>**DMO \_ \_Тип E \_ не \_ принят**</dt> <dt>0x80040205</dt> </dl>  | Тип носителя не принят.<br/>                                                                                                                             |
| <span id="DMO_E_NO_MORE_ITEMS"></span><span id="dmo_e_no_more_items"></span><dl> <dt>**DMO \_ Е 0x80040206 больше \_ \_ \_ элементов**</dt> <dt></dt> </dl>              | Индекс типа носителя выходит за пределы допустимого диапазона.<br/>                                                                                                                        |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Медиаерр. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы DMO](dmo-constants.md)
</dt> </dl>

 

 




