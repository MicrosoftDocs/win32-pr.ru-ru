---
description: Указывает, должен ли кодировщик использовать предпочтительный размер кадра, заданный в числе выборок на кадр.
ms.assetid: c9baeff7-53fb-425f-b07b-4066a705ca54
title: Свойство MFPKEY_REQUESTING_A_FRAMESIZE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c39d1d9ecdba27e46a1e49949f1607fc60d53501d321e49c4899f9b8928ccf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555434"
---
# <a name="mfpkey_requesting_a_framesize-property"></a>МФПКЭЙ \_ запрашивает \_ \_ свойство фрамесизе

Указывает, должен ли кодировщик использовать предпочтительный размер кадра, заданный в числе выборок на кадр.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

**Логическое значение VT \_**

## <a name="remarks"></a>Remarks

Чтобы задать предпочтительный размер кадра, задайте следующие свойства.

-   Задайте **для \_ мфпкэй \_ запрос \_ фрамесизе** к варианту \_ true.
-   Задайте для параметра [**мфпкэй \_ предпочтительный \_ фрамесизе**](mfpkey-preferred-framesizeproperty.md) число выборок в каждом кадре.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Клиент<br/> | Windows Vista или Windows 7<br/>                                                   |
| Заголовок<br/> | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
