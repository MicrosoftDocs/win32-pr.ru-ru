---
description: Указывает число кадров видео, закодированных кодеком.
ms.assetid: 4a812609-137f-4f7f-aa55-89e26d7f1972
title: Свойство MFPKEY_CODEDFRAMES (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708bb6c200701cdf48fa8407108be2161fdb4f61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663619"
---
# <a name="mfpkey_codedframes-property"></a>МФПКЭЙ \_ кодедфрамес, свойство

Указывает число кадров видео, закодированных кодеком.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

g \_ всзвмвккодедфрамес

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="remarks"></a>Комментарии

Это значение равно [мфпкэй \_ тоталфрамес](mfpkey-totalframesproperty.md) минус все кадры, которые были удалены из-за ограничений скорости. Это значение можно получить после завершения передачи образцов.

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

 

 




