---
description: Корректирует насыщенность.
ms.assetid: bd71f542-36d9-4dfc-b402-35ee8e574731
title: Свойство MFPKEY_COLOR_SATURATION (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b357521327bc913a0ace6b630cb9f2a27b553c3dfc8303e1a6bd9af218c5b743
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954404"
---
# <a name="mfpkey_color_saturation-property"></a>\_ \_ Свойство насыщенности цвета мфпкэй

Корректирует насыщенность.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="default-value"></a>Значение по умолчанию

0

## <a name="applies-to"></a>Применяется к

-   [Преобразование элемента управления цветом DSP](colorcontroltransform.md)

## <a name="remarks"></a>Remarks

Корректировка насыщенности выполняется путем умножения значений CB и CR на константу.

Это свойство имеет диапазон от-127 до 127. Ноль означает отсутствие изменений в насыщенности.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
