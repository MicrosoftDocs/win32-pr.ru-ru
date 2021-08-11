---
description: MFPKEY_COLORCONV_MODE свойство — указывает, является ли входной поток чередованием.
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: Свойство MFPKEY_COLORCONV_MODE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f86ed10873c1587aefba342392afa7f84f8c635788339d64deca18b76629255
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242893"
---
# <a name="mfpkey_colorconv_mode-property"></a>МФПКЭЙ \_ колорконв \_ mode, свойство

Указывает, является ли входной поток чередованием.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="default-value"></a>Значение по умолчанию

Вычислено DSP из исходного видео.

## <a name="applies-to"></a>Применяется к

-   [DSP цветового преобразователя](colorconverter.md)

## <a name="remarks"></a>Remarks

Используйте одно из следующих значений.



| Значение | Описание |
|-------|-------------|
| 0     | прогрессивный |
| 2     | Interlaced  |



 

Если это свойство не задано, DSP использует входной тип носителя для определения, является ли видео чередованием. Это свойство можно задать, чтобы переопределить параметр типа мультимедиа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также статью

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
