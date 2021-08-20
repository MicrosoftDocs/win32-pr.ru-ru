---
description: Управляет сигнализацией Мфсампликстенсион \_ меанабсолутедифференце через имфаттрибуте для каждого выходного образца.
ms.assetid: 61C0F431-FBF5-4B17-8F3A-0F6AD2BA33B7
title: Свойство CODECAPI_AVEncVideoMeanAbsoluteDifference (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eb0d2e515187961b020ef4896f4e6669d378dbed2ca4ddb487cf271db684591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118064755"
---
# <a name="codecapi_avencvideomeanabsolutedifference-property"></a>КОДЕКАПИ \_ авенквидеомеанабсолутедифференце, свойство

Управляет сигнализацией [мфсампликстенсион \_ Меанабсолутедифференце](mfsampleextension-meanabsolutedifference.md) через [**имфаттрибуте**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) для каждого выходного образца.

## <a name="data-type"></a>Тип данных

**Ulong** (VT \_ UI4)

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ авенквидеомеанабсолутедифференце**

## <a name="remarks"></a>Remarks

Если приложение устанавливает ненулевое значение, кодировщику следует добавить к каждому выходному примеру атрибут [мфсампликстенсион \_ меанабсолутедифференце](mfsampleextension-meanabsolutedifference.md) Sample. Атрибут Мфсампликстенсион \_ меанабсолутедифференце показывает среднее абсолютное различие между исходными примерами и прогнозируемыми примерами на плоскости Y.

Если кодировщик возвращает 0 для **жетпараметерранже**, кодировщик не поддерживает выходные данные [мфсампликстенсион \_ меанабсолутедифференце](mfsampleextension-meanabsolutedifference.md) в выходных образцах.

Значение по умолчанию должно быть равно 0.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Кодекапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




