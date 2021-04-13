---
description: Корректирует насыщенность.
ms.assetid: bd71f542-36d9-4dfc-b402-35ee8e574731
title: Свойство MFPKEY_COLOR_SATURATION (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496b1f017ceff6ab4bd01ce01ccfd5da0759befc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544938"
---
# <a name="mfpkey_color_saturation-property"></a>\_ \_ Свойство насыщенности цвета мфпкэй

Корректирует насыщенность.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="default-value"></a>Значение по умолчанию

0

## <a name="applies-to"></a>Применение

-   [Преобразование элемента управления цветом DSP](colorcontroltransform.md)

## <a name="remarks"></a>Комментарии

Корректировка насыщенности выполняется путем умножения значений CB и CR на константу.

Это свойство имеет диапазон от-127 до 127. Ноль означает отсутствие изменений в насыщенности.

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

 

 
