---
description: Непрозрачный переносимый тип для поддержки использования синтаксиса инициализатора C/C++ для загрузки значений с плавающей запятой в экземпляр типа КСМВЕКТОР.
ms.assetid: bafaa59f-fd1b-e252-cbbd-903df796fde0
title: Тип данных XMVECTORF32 (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1a39de246e3e0e4ab9a96197dbe4a286cb6ecabe327d60e5c506795af79dd11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739784"
---
# <a name="xmvectorf32-data-type"></a>Тип данных XMVECTORF32

Непрозрачный переносимый тип для поддержки использования синтаксиса инициализатора C/C++ для загрузки значений с плавающей запятой в экземпляр типа [**ксмвектор**](xmvector-data-type.md) .


```C++
typedef XMVECTORF32 vectorf32;
```



## <a name="remarks"></a>Remarks

Список дополнительных функций, таких как конструкторы и операторы, доступных `XMVECTORF32` при использовании при программировании в C++, см. в разделе [расширения XMVECTORF32](ovw-xmvectorf32-extensions.md).

Структуры **XMVECTORF32**, [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md)и [**XMVECTORU8**](xmvectoru8-data-type.md) предоставляются в качестве механизма создания [**ксмвектор**](xmvector-data-type.md) из различных типов данных констант (с плавающей запятой, целым числом, целым числом и байтом) с помощью инициализаторов.

Это необходимо для поддержки [**ксмвектор**](xmvector-data-type.md), так как сам по себе не поддерживает инициализаторы в целях обеспечения переносимости и оптимизации.

Например:


```
XMVECTOR data;
XMVECTORF32 floatingVector = { 0.f, 0.f, 0.1f, 1.f };
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

[**Тип данных XMVECTORI32**](xmvectori32-data-type.md)
</dt> <dt>

[**Тип данных КСМВЕКТОР**](xmvector-data-type.md)
</dt> <dt>

[**Тип данных XMVECTORU32**](xmvectoru32-data-type.md)
</dt> <dt>

[**Тип данных XMVECTORU8**](xmvectoru8-data-type.md)
</dt> <dt>

[**Тип данных XMVECTORF32**](xmvectorf32-data-type.md)
</dt> </dl>

 

 




