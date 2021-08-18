---
description: Непрозрачный переносимый тип для поддержки использования синтаксиса инициализатора C/C++ для загрузки целочисленных значений в экземпляр типа КСМВЕКТОР.
ms.assetid: 6564030e-b6e9-0c4f-4e2a-4132e4264c94
title: Тип данных XMVECTORI32 (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b4bb03dffb4c77575aab8c2a2680ecd821fea627f49325c6748ede607ef81f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739763"
---
# <a name="xmvectori32-data-type"></a>Тип данных XMVECTORI32

Непрозрачный переносимый тип для поддержки использования синтаксиса инициализатора C/C++ для загрузки целочисленных значений в экземпляр типа [**ксмвектор**](xmvector-data-type.md) .


```C++
typedef XMVECTORI32 vectori32;
```



## <a name="remarks"></a>Remarks

Список дополнительных функций, таких как конструкторы и операторы, доступных `XMVECTORI32` при использовании при программировании в C++, см. в разделе [расширения XMVECTORI32](ovw-xmvectori32-extensions.md).

Структуры [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), **XMVECTORI32** и [**XMVECTORU8**](xmvectoru8-data-type.md) предоставляются в качестве механизма создания [**ксмвектор**](xmvector-data-type.md) из различных типов данных констант (с плавающей запятой, целым числом, целым числом и байтом) с помощью инициализаторов.

Это необходимо для поддержки [**ксмвектор**](xmvector-data-type.md), так как сам по себе не поддерживает инициализаторы в целях обеспечения переносимости и оптимизации.

Например:


```
XMVECTOR data;
XMVECTORI32 intVector = { -1, 5, 33, 0 };
data = intVector;
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

[**Тип данных XMVECTORU32**](xmvectoru32-data-type.md)
</dt> <dt>

[**Тип данных XMVECTORU8**](xmvectoru8-data-type.md)
</dt> <dt>

[**Тип данных XMVECTORI32**](xmvectori32-data-type.md)
</dt> </dl>

 

 




