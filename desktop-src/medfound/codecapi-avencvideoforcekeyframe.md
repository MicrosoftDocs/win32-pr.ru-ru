---
description: Заставляет кодировщик кодировать следующий кадр как ключевой кадр.
ms.assetid: 1E252967-6C28-4DA3-9E64-BD276E475753
title: Свойство CODECAPI_AVEncVideoForceKeyFrame (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72c555d5680e822e9a8308b3e143a754eb22b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701329"
---
# <a name="codecapi_avencvideoforcekeyframe-property"></a>КОДЕКАПИ \_ авенквидеофорцекэйфраме, свойство

Заставляет кодировщик кодировать следующий кадр как ключевой кадр.

## <a name="data-type"></a>Тип данных

**Ulong** (VT \_ UI4)

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ авенквидеофорцекэйфраме**

## <a name="property-value"></a>Значение свойства

Если значение не равно нулю, кодировщик будет кодировать следующий кадр в качестве ключевого кадра. Если значение равно нулю, кодировщик выбирает, следует ли кодировать следующий кадр как ключевой кадр.

Это свойство применяется к следующему кадру, который кодировщик получает в качестве входных данных. Для Media Foundation преобразования (MFT) это следующий кадр, который передается методу [**имфтрансформ::P роцессинпут**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) . Параметр сбрасывается в ноль после следующего кадра.

## <a name="remarks"></a>Комментарии

Это свойство также используется с [кодировщиками камер H. 264 увк 1,5](camera-encoder-h264-uvc-1-5.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Кодекапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**икодекапи**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

