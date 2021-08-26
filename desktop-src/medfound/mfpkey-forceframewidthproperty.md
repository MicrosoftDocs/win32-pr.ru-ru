---
description: Задает промежуточную ширину кадра для кодированного видео.
ms.assetid: 805bd587-31af-49b8-b5ab-2dcf2a3f81c5
title: Свойство MFPKEY_FORCEFRAMEWIDTH (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d04e30f5fd5d2ecc7055553e17eaf86199b62be8d3dd861b9f82246947212f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939843"
---
# <a name="mfpkey_forceframewidth-property"></a>МФПКЭЙ \_ форцефрамевидс, свойство

Задает промежуточную ширину кадра для кодированного видео.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

g \_ всзвмвкфорцефрамевидс

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="remarks"></a>Remarks

Вы можете задать это значение и свойство [мфпкэй \_ форцефрамехеигхт](mfpkey-forceframeheightproperty.md) , чтобы заставить кодировщик кодировать видеопоток размером кадра, размер которого меньше, чем размер кадра ввода или вывода. При декодировании видео будет изменено до исходного разрешения ввода.

Допустимые размеры рамки на любой из осей — от 2 до 8192 пикселей. Размеры фрейма должны быть кратны 2.

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

 

 




