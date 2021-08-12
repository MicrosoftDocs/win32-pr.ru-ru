---
description: Непрозрачный переносимый тип для поддержки использования синтаксиса инициализатора C/C++ для загрузки \_ значений Uint8 t в экземпляр типа ксмвектор.
ms.assetid: ab73ac2c-f178-1bb9-910d-9eef5fc6f5df
title: Тип данных XMVECTORU8 (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff3c335df3e74bc58776883b15d724c65d558bad30fc37e0e28547102260301a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118276200"
---
# <a name="xmvectoru8-data-type"></a>Тип данных XMVECTORU8

Непрозрачный переносимый тип для поддержки использования синтаксиса инициализатора C/C++ для загрузки \_ значений Uint8 t в экземпляр типа [**ксмвектор**](xmvector-data-type.md) .


```C++
typedef XMVECTORU8 vectoru8;
```



## <a name="remarks"></a>Remarks

Список дополнительных функций, таких как конструкторы и операторы, доступных при использовании XMVECTORU8 при программировании в C++, см. в разделе [расширения XMVECTORU8](ovw-xmvectoru8-extensions.md).

Структуры [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md)и **XMVECTORU8** предоставляются в качестве механизма создания [**ксмвектор**](xmvector-data-type.md) из различных типов данных констант (с плавающей запятой, целым числом, целым числом и байтом) с помощью инициализаторов.

Это необходимо для поддержки [**ксмвектор**](xmvector-data-type.md), так как сам по себе не поддерживает инициализаторы в целях обеспечения переносимости и оптимизации.

Пример:

``` syntax
XMVECTOR data;
XMVECTORU8  byteVector = { (uint8_t)  1,(uint8_t) 16,(uint8_t)101,(uint8_t) 62,
                           (uint8_t)  4,(uint8_t)  0,(uint8_t)  2,(uint8_t) 99,
                           (uint8_t)  9,(uint8_t) 18,(uint8_t)  0,(uint8_t)  0,
                           (uint8_t)100,(uint8_t) 51,(uint8_t) 23,(uint8_t)117};

data = floatingVector;
```

**Пространство имен**. Использование DirectX

### <a name="platform-requirements"></a>Требования к платформе

Microsoft Visual Studio 2010 или Microsoft Visual Studio 2012 с Windows SDK для Windows 8. поддерживается для классических приложений Win32, приложений для магазина Windows и Windows Phone 8 приложений.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Директксмас. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Типы библиотек Директксмас](ovw-xnamath-reference-types.md)
</dt> <dt>

[**Тип данных КСМВЕКТОР**](xmvector-data-type.md)
</dt> <dt>

[**Тип данных XMVECTORF32**](xmvectorf32-data-type.md)
</dt> <dt>

[**Тип данных XMVECTORI32**](xmvectori32-data-type.md)
</dt> <dt>

[**Тип данных XMVECTORU32**](xmvectoru32-data-type.md)
</dt> <dt>

[Расширения XMVECTORU8](ovw-xmvectoru8-extensions.md)
</dt> </dl>

 

 




