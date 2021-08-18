---
description: Задает требуемый уровень качества (1-проходная) для кодирования звуковых потоков с учетом скорости.
ms.assetid: 0bbb4f51-78c3-4455-bd96-9a6d80110220
title: Свойство MFPKEY_DESIRED_VBRQUALITY (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f52ab8cc791a5309b5df6537d133bce68e49d66a15ab79c12beeb7411cece8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939951"
---
# <a name="mfpkey_desired_vbrquality-property"></a>МФПКЭЙ \_ нужное \_ вбркуалити свойство

Задает требуемый уровень качества (1-проходная) для кодирования звуковых потоков с учетом скорости.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

**VT \_ UI4**

## <a name="default-value"></a>Значение по умолчанию

0

## <a name="remarks"></a>Remarks

Это значение может быть от 0 до 100, где 100 — максимальное качество. Значение 0 указывает, что метод кодирования VBR с учетом качества не должен использоваться.

Чтобы перечислить режимы VBR, соответствующие определенным требованиям к качеству, задайте следующие свойства кодировщика.

-   Задайте для [**мфпкэй \_ Вбренаблед**](mfpkey-vbrenabledproperty.md) значение **Variant \_ true**.
-   Установите для параметра [**мфпкэй \_ ограничение \_ перечисления \_ вбркуалити**](mfpkey-constrain-enumerated-vbrqualityproperty.md) значение **Variant \_ true**.
-   Задайте требуемое качество для **мфпкэй \_ \_ вбркуалити** . Для режимов без потерь задайте нужное качество равным 100.

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

 

 
