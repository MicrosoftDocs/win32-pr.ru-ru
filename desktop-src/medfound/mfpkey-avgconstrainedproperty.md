---
description: Указывает, использует ли кодировщик среднее-управляемое кодирование VBR.
ms.assetid: 2c150eb1-4ffe-4f77-8ef8-e3bf29b17b10
title: Свойство MFPKEY_AVGCONSTRAINED (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e7231cb3807be8f4467592ac0138a75ea277bdf8a13dfb3564d3572036e7ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874096"
---
# <a name="mfpkey_avgconstrained-property"></a>МФПКЭЙ \_ авгконстраинед, свойство

Указывает, использует ли кодировщик среднее-управляемое кодирование VBR.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

**Логическое значение VT \_**

## <a name="default-value"></a>Значение по умолчанию

**ВАРИАНТ \_ false**

## <a name="remarks"></a>Remarks

Если для этого свойства и [**свойства \_ вбренаблед мфпкэй**](mfpkey-vbrenabledproperty.md) задано значение **Variant \_ true**, кодировщик использует среднее-управляемое кодирование VBR. В этом случае кодировщик настраивает себя в соответствии со значениями [**мфпкэй \_ Дин \_ VBR \_ бавг**](mfpkey-dyn-vbr-bavgproperty.md) и [**мфпкэй \_ Дин \_ VBR \_ равг**](mfpkey-dyn-vbr-ravgproperty.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
