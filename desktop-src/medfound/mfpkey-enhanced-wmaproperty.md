---
description: Указывает, использует ли основной кодировщик &\# 0034; Плюс&\# 0034;.
ms.assetid: 1ace09da-7dee-469e-a533-63b40ac747ab
title: Свойство MFPKEY_ENHANCED_WMA (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df1c7ddc0e7bfb6d62d51e535f10b257eac6f2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649106"
---
# <a name="mfpkey_enhanced_wma-property"></a>МФПКЭЙ \_ Расширенное \_ свойство WMA

Указывает, использует ли основной кодировщик функцию "плюс".

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

**VT \_ UI4**

## <a name="default-value"></a>Значение по умолчанию

0

## <a name="remarks"></a>Комментарии

Это свойство доступно только для Windows Media Audio без потерь.

Если оставить это свойство со значением по умолчанию 0 или установить его равным 1, основной кодировщик решит, следует ли использовать часть "плюс". Если задать для этого свойства значение 2, то основной кодировщик не будет использовать функцию "плюс".

Это свойство изменяет перечислимые типы носителей, поэтому, если оно задано, необходимо сделать это, прежде чем задавать тип выходных данных.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Клиент<br/> | Windows Vista или Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
