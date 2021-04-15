---
description: Непрозрачный переносимый тип для поддержки использования синтаксиса инициализатора C/C++ для загрузки целочисленных значений в экземпляр типа КСМВЕКТОР.
ms.assetid: 6564030e-b6e9-0c4f-4e2a-4132e4264c94
title: Тип данных XMVECTORI32 (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ac36caf97a62037223840e9220876f1c7a1f09a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649095"
---
# <a name="xmvectori32-data-type"></a>Тип данных XMVECTORI32

Непрозрачный переносимый тип для поддержки использования синтаксиса инициализатора C/C++ для загрузки целочисленных значений в экземпляр типа [**ксмвектор**](xmvector-data-type.md) .


```C++
typedef XMVECTORI32 vectori32;
```



## <a name="remarks"></a>Комментарии

Список дополнительных функций, таких как конструкторы и операторы, доступных `XMVECTORI32` при использовании при программировании в C++, см. в разделе [расширения XMVECTORI32](ovw-xmvectori32-extensions.md).

Структуры [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), **XMVECTORI32** и [**XMVECTORU8**](xmvectoru8-data-type.md) предоставляются в качестве механизма создания [**ксмвектор**](xmvector-data-type.md) из различных типов данных констант (с плавающей запятой, целым числом, целым числом и байтом) с помощью инициализаторов.

Это необходимо для поддержки [**ксмвектор**](xmvector-data-type.md), так как сам по себе не поддерживает инициализаторы в целях обеспечения переносимости и оптимизации.

Пример:


```
XMVECTOR data;
XMVECTORI32 intVector = { -1, 5, 33, 0 };
data = intVector;
```



**Пространство имен**. Использование DirectX

### <a name="platform-requirements"></a>Требования к платформе

Microsoft Visual Studio 2010 или Microsoft Visual Studio 2012 с Windows SDK для Windows 8. Поддерживается для классических приложений Win32, приложений для Магазина Windows и Windows Phone 8 приложений.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Директксмас. h</dt> </dl> |



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

 

 




