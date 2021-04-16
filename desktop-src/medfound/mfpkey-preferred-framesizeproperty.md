---
description: Указывает предпочтительное количество выборок на кадр.
ms.assetid: ad629dbd-49d8-43d0-95a8-03f2043e397e
title: Свойство MFPKEY_PREFERRED_FRAMESIZE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe04ad37c6cd684e3179cbd16328346fd6f11dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699151"
---
# <a name="mfpkey_preferred_framesize-property"></a>МФПКЭЙ \_ предпочтительное \_ свойство фрамесизе

Указывает предпочтительное количество выборок на кадр.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

**VT \_ UI4**

## <a name="remarks"></a>Комментарии

Чтобы задать предпочтительный размер кадра, задайте следующие свойства.

-   Задайте [**для \_ мфпкэй \_ запрос \_ фрамесизе**](mfpkey-requesting-a-framesizeproperty.md) к **варианту \_ true**.
-   Задайте для параметра **мфпкэй \_ предпочтительный \_ фрамесизе** число выборок в каждом кадре.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Клиент<br/> | Windows Vista или Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
