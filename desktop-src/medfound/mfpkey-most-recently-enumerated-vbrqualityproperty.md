---
description: Задает уровень качества VBR последнего перечислимого типа выходных данных.
ms.assetid: 7d67e41f-060b-49a1-9e17-5db081ef4210
title: Свойство MFPKEY_MOST_RECENT_ENUMERATED_VBRQUALITY (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68e609f8dc7b95eb9cfd4bf537af47d1a11cb4ba625f0bbc65897b008ff03a31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117689798"
---
# <a name="mfpkey_most_recent_enumerated_vbrquality-property"></a>МФПКЭЙ \_ \_ Последнее \_ перечисленное \_ свойство вбркуалити

Задает уровень качества VBR последнего перечислимого типа выходных данных. Только для чтения.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

**VT \_ UI4**

## <a name="remarks"></a>Remarks

Когда кодировщик выступает в качестве Media Foundation преобразования (MFT) и перечисляет тип вывода при вызове [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype), можно запросить таблицу MFT для свойства **\_ \_ \_ \_ вбркуалити, перечисленного в мфпкэй** . Возвращаемое значение указывает качество VBR последнего возвращенного типа выходного носителя. Затем это значение можно использовать для задания свойства [**мфпкэй \_ требуемого \_ вбркуалити**](mfpkey-desired-vbrqualityproperty.md) кодировщика.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Клиент<br/> | Windows Vista или Windows 7<br/>                                                   |
| Заголовок<br/> | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**МФПКЭЙ \_ вбренаблед**](mfpkey-vbrenabledproperty.md)
</dt> <dt>

[**МФПКЭЙ \_ ограничение \_ перечисления \_ вбркуалити**](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
