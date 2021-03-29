---
description: Указывает число пропущенных видеокадров, так как они являлись дубликатами предыдущих кадров.
ms.assetid: ef4aa5a0-3788-493e-b541-c3a24509d939
title: Свойство MFPKEY_ZEROBYTEFRAMES (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffcf29d099b3a3fb27a307e970af7af1a5c3d58b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898201"
---
# <a name="mfpkey_zerobyteframes-property"></a>МФПКЭЙ \_ зеробитефрамес, свойство

Указывает число пропущенных видеокадров, так как они являлись дубликатами предыдущих кадров.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

g \_ всзвмвкзеробитефрамес

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="remarks"></a>Комментарии

Это значение не вычитается из общего числа переданных кадров ([мфпкэй \_ тоталфрамес](mfpkey-totalframesproperty.md)) при вычислении количества закодированных кадров ([мфпкэй \_ кодедфрамес](mfpkey-codedframesproperty.md)).

Вы можете запретить кодеку пропускать дубликаты кадров, установив для [мфпкэй \_ ПРОДУЦЕДУММИФРАМЕС](mfpkey-producedummyframesproperty.md) значение Variant \_ true.

Это значение можно получить после завершения передачи образцов.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




