---
description: Указывает максимальное число проходов, поддерживаемое кодировщиком.
ms.assetid: 7e21cd0f-f13f-4321-b246-f1adaa5c6094
title: Свойство MFPKEY_PASSESRECOMMENDED (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af869c6acca584547083b3de245913a35680306b47feabaf2a602a3c1c15e87e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826364"
---
# <a name="mfpkey_passesrecommended-property"></a>МФПКЭЙ \_ пассесрекоммендед, свойство

Указывает максимальное число проходов, поддерживаемое кодировщиком. Только для чтения.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

g \_ всзвмвкпассесрекоммендед, g \_ всзвмкпмакспассес

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="remarks"></a>Remarks

Можно получить значение этого свойства, вызвав [ивмкодекпропс:: жеткодекпроп](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop). При использовании **ипропертибаг** необходимо сначала задать значение FOURCC нужного сжатого формата с помощью свойства [мфпкэй \_ FourCC](mfpkey-fourccproperty.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




