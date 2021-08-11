---
description: Указывает среднюю скорость потока в битах в секунду для кодировщика, который настроен для использования среднего управляемого кодирования VBR.
ms.assetid: d689a34c-97f7-4b1c-82b6-863ce3b8403f
title: Свойство MFPKEY_DYN_VBR_RAVG (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48ee3d3a9b9a60b664041b9c6f84c38b8da9ceef87f73177f2ace792cf043992
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242616"
---
# <a name="mfpkey_dyn_vbr_ravg-property"></a>МФПКЭЙ \_ Дин \_ VBR \_ равг, свойство

Указывает среднюю скорость потока в битах в секунду для кодировщика, который настроен для использования среднего управляемого кодирования VBR.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

**VT \_ I4**

## <a name="remarks"></a>Remarks

Если для свойств [**мфпкэй \_ Авгконстраинед**](mfpkey-avgconstrainedproperty.md) и [**мфпкэй \_ вбренаблед**](mfpkey-vbrenabledproperty.md) задано значение **Variant \_ true**, кодировщик использует среднюю управляемую кодировку VBR. В этом случае кодировщик настраивает себя в соответствии со значением этого свойства и свойством [**мфпкэй \_ Дин \_ VBR \_ бавг**](mfpkey-dyn-vbr-bavgproperty.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также статью

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
