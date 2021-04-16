---
description: Указывает, лиметед ли режимы, перечисленные кодировщиком, с требованиями к качеству, заданными МФПКЭЙ \_ требуемым \_ вбркуалити.
ms.assetid: b2f1d5c5-d2bb-4a8a-94ea-fd969e07bb0e
title: Свойство MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9e63ab955bbe7726ab67bdab057fe2d397942
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699229"
---
# <a name="mfpkey_constrain_enumerated_vbrquality-property"></a>МФПКЭЙ \_ ограничить \_ перечислимое \_ свойство вбркуалити

Указывает, лиметед ли режимы, перечисленные кодировщиком, с требованиями к качеству, заданными [**мфпкэй \_ требуемым \_ вбркуалити**](mfpkey-desired-vbrqualityproperty.md).

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

**Логическое значение VT \_**

## <a name="default-value"></a>Значение по умолчанию

**ВАРИАНТ \_ false**

## <a name="remarks"></a>Комментарии

Чтобы перечислить режимы VBR, соответствующие определенным требованиям к качеству, задайте следующие свойства кодировщика.

-   Задайте для [**мфпкэй \_ Вбренаблед**](mfpkey-vbrenabledproperty.md) значение **Variant \_ true**.
-   Установите для параметра **мфпкэй \_ ограничение \_ перечисления \_ вбркуалити** значение **Variant \_ true**.
-   Задайте требуемое качество для [**мфпкэй \_ \_ вбркуалити**](mfpkey-desired-vbrqualityproperty.md) . Для режимов без потерь задайте нужное качество равным 100.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Клиент<br/> | Windows Vista или Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
