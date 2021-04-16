---
description: Указывает, должен ли кодировщик использовать предпочтительный размер кадра, заданный в числе выборок на кадр.
ms.assetid: c9baeff7-53fb-425f-b07b-4066a705ca54
title: Свойство MFPKEY_REQUESTING_A_FRAMESIZE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3355e84318ba4ad7995ac5ad0f002f4d70767b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699262"
---
# <a name="mfpkey_requesting_a_framesize-property"></a>МФПКЭЙ \_ запрашивает \_ \_ свойство фрамесизе

Указывает, должен ли кодировщик использовать предпочтительный размер кадра, заданный в числе выборок на кадр.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

**Логическое значение VT \_**

## <a name="remarks"></a>Комментарии

Чтобы задать предпочтительный размер кадра, задайте следующие свойства.

-   Задайте **для \_ мфпкэй \_ запрос \_ фрамесизе** к варианту \_ true.
-   Задайте для параметра [**мфпкэй \_ предпочтительный \_ фрамесизе**](mfpkey-preferred-framesizeproperty.md) число выборок в каждом кадре.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Клиент<br/> | Windows Vista или Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
