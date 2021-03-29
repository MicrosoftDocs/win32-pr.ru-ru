---
description: Указывает FOURCC, определяющую кодировщик, который вы хотите использовать.
ms.assetid: c03da576-cb58-4686-af6f-9575520c759c
title: Свойство MFPKEY_FOURCC (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbe852ad0d7113717428bdd832b8f327f8d0b6e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991605"
---
# <a name="mfpkey_fourcc-property"></a>МФПКЭЙ \_ FourCC, свойство

Указывает FOURCC, определяющую кодировщик, который вы хотите использовать.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

g \_ всзвмвкфауркк

## <a name="data-type"></a>Тип данных

VT \_ I4 (значение FOURCC)

## <a name="remarks"></a>Комментарии

Это значение необходимо задать перед получением значений для следующих свойств с помощью **ипропертибаг** или **ипропертисторе**:

-   [МФПКЭЙ \_ буфферфуллнессинфирстбите](mfpkey-bufferfullnessinfirstbyteproperty.md)
-   [МФПКЭЙ \_ пассесрекоммендед](mfpkey-passesrecommendedproperty.md)

Для получения значений свойств, зависящих от FOURCC, перечисленных выше, следует использовать [**ивмкодекпропс:: жеткодекпроп**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) . При использовании **жеткодекпроп** не нужно задавать **мфпкэй \_ FourCC**.

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

 

 




