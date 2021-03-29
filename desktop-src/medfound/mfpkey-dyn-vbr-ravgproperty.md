---
description: Указывает среднюю скорость потока в битах в секунду для кодировщика, который настроен для использования среднего управляемого кодирования VBR.
ms.assetid: d689a34c-97f7-4b1c-82b6-863ce3b8403f
title: Свойство MFPKEY_DYN_VBR_RAVG (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8103d36db5a9e946449231943e076c26258eec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991607"
---
# <a name="mfpkey_dyn_vbr_ravg-property"></a>МФПКЭЙ \_ Дин \_ VBR \_ равг, свойство

Указывает среднюю скорость потока в битах в секунду для кодировщика, который настроен для использования среднего управляемого кодирования VBR.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

**VT \_ I4**

## <a name="remarks"></a>Комментарии

Если для свойств [**мфпкэй \_ Авгконстраинед**](mfpkey-avgconstrainedproperty.md) и [**мфпкэй \_ вбренаблед**](mfpkey-vbrenabledproperty.md) задано значение **Variant \_ true**, кодировщик использует среднюю управляемую кодировку VBR. В этом случае кодировщик настраивает себя в соответствии со значением этого свойства и свойством [**мфпкэй \_ Дин \_ VBR \_ бавг**](mfpkey-dyn-vbr-bavgproperty.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
