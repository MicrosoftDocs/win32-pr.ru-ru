---
description: Регулирует оттенок.
ms.assetid: 8dc3c888-5ab8-40a1-8768-bec58b62eaf0
title: Свойство MFPKEY_COLOR_HUE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 646d9e3ae0e72e11ae8952d28df9e4e3afc4147eaa7983bd1f0e9c82266ca5c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954444"
---
# <a name="mfpkey_color_hue-property"></a>\_Свойство цветового \_ тона мфпкэй

Регулирует оттенок.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="default-value"></a>Значение по умолчанию

0

## <a name="applies-to"></a>Применяется к

-   [Преобразование элемента управления цветом DSP](colorcontroltransform.md)

## <a name="remarks"></a>Remarks

Корректировка оттенков выполняется путем смешения значений CB и CR. (Если CB и CR отображаются в двухмерном пространстве, Настройка оттенков выполняется путем поворота вокруг источника.)

Это свойство имеет диапазон от-127 до 127. Ноль означает отсутствие изменений в оттенках.

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

 

 
