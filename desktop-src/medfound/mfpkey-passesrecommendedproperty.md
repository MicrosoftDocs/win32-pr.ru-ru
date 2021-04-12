---
description: Указывает максимальное число проходов, поддерживаемое кодировщиком.
ms.assetid: 7e21cd0f-f13f-4321-b246-f1adaa5c6094
title: Свойство MFPKEY_PASSESRECOMMENDED (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433e0a0d254c09965976e5659bacfacf3be06643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263984"
---
# <a name="mfpkey_passesrecommended-property"></a>МФПКЭЙ \_ пассесрекоммендед, свойство

Указывает максимальное число проходов, поддерживаемое кодировщиком. Только для чтения.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

g \_ всзвмвкпассесрекоммендед, g \_ всзвмкпмакспассес

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="remarks"></a>Комментарии

Можно получить значение этого свойства, вызвав [ивмкодекпропс:: жеткодекпроп](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop). При использовании **ипропертибаг** необходимо сначала задать значение FOURCC нужного сжатого формата с помощью свойства [мфпкэй \_ FourCC](mfpkey-fourccproperty.md) .

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

 

 




