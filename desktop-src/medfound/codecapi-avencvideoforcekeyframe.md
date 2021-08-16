---
description: Заставляет кодировщик кодировать следующий кадр как ключевой кадр.
ms.assetid: 1E252967-6C28-4DA3-9E64-BD276E475753
title: Свойство CODECAPI_AVEncVideoForceKeyFrame (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2e28738dcd7398ce04abe7f71778e94d7d5d4f49393365e92c43bbb347d98c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880710"
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

## <a name="remarks"></a>Remarks

Это свойство также используется с [кодировщиками камер H. 264 увк 1,5](camera-encoder-h264-uvc-1-5.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Кодекапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**икодекапи**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

