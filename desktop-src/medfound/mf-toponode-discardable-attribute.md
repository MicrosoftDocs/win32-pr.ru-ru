---
description: Указывает, может ли конвейер удалять образцы из узла топологии.
ms.assetid: 8be20446-4876-4d6f-b0db-2eb1ffaef9aa
title: Атрибут MF_TOPONODE_DISCARDABLE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d76e00a0f70735211cf06aca0adc00238ae5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719702"
---
# <a name="mf_toponode_discardable-attribute"></a>\_Атрибут MF топоноде \_

Указывает, может ли конвейер удалять образцы из узла топологии.

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="remarks"></a>Комментарии

Этот атрибут применяется ко всем типам узлов. Обычно этот атрибут устанавливается на узлах tee, чтобы указать, что вторичные выходные данные не являются обязательными.

Значение атрибута представляет собой массив индексов для вывода потоков на узле.

Если этот атрибут задан, конвейер может удалить образцы из указанных выходных потоков, если поток не находится позади.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Атрибуты узла топологии](topology-node-attributes.md)
</dt> </dl>

 

 




