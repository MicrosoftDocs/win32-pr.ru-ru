---
title: Конструктора Matrix5x4F Matrix5x4F (FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, float, float, FLOAT, float, float, float, float, float, float, float, float, float, float, float) (D2d1 \_ Helper. h)
description: Создает новый экземпляр класса Matrix5x4F, инициализируемый всеми значениями матрицы с плавающей запятой.
ms.assetid: 46C2741F-9E49-4ABD-9DA5-D4E6D3CA2B09
keywords:
- Конструктор Matrix5x4F Direct2D
- Конструктор Matrix5x4F Direct2D, интерфейс Matrix5x4F
- Интерфейс Matrix5x4F Direct2D, конструктор Matrix5x4F
topic_type:
- apiref
api_name:
- Matrix5x4F.Matrix5x4F
api_location:
- D2d1.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2582e58f535ddf4f87d54e16dd2edaec2aa37e91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682166"
---
# <a name="matrix5x4fmatrix5x4ffloat-float-float-float-float-float-float-float-float-float-float-float-float-float-float-float-float-float-float-float-constructor"></a>Конструктор Matrix5x4F:: Matrix5x4F (FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, float, float, float, float, float, float, float, float, float, float, float)

Создает новый экземпляр класса [**Matrix5x4F**](matrix5x4f.md) , инициализируемый всеми значениями матрицы с плавающей запятой.

## <a name="syntax"></a>Синтаксис


```C++
inline Matrix5x4F(
   FLOAT m11,
   FLOAT m12,
   FLOAT m13,
   FLOAT m14,
   FLOAT m21,
   FLOAT m22,
   FLOAT m23,
   FLOAT m24,
   FLOAT m31,
   FLOAT m32,
   FLOAT m33,
   FLOAT m34,
   FLOAT m41,
   FLOAT m42,
   FLOAT m43,
   FLOAT m44,
   FLOAT m51,
   FLOAT m52,
   FLOAT m53,
   FLOAT m54
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*m11* 
</dt> <dd>

Тип: **float**

Значение в первой строке и первом столбце матрицы.

</dd> <dt>

*m12* 
</dt> <dd>

Тип: **float**

Значение в первой строке и втором столбце матрицы.

</dd> <dt>

*m13* 
</dt> <dd>

Тип: **float**

Значение в первой строке и третьем столбце матрицы.

</dd> <dt>

*m14* 
</dt> <dd>

Тип: **float**

Значение в первой строке и четвертом столбце матрицы.

</dd> <dt>

*m21* 
</dt> <dd>

Тип: **float**

Значение во второй строке и первом столбце матрицы.

</dd> <dt>

*m22* 
</dt> <dd>

Тип: **float**

Значение во второй строке и втором столбце матрицы.

</dd> <dt>

*m23* 
</dt> <dd>

Тип: **float**

Значение во второй строке и третьем столбце матрицы.

</dd> <dt>

*m24* 
</dt> <dd>

Тип: **float**

Значение во второй строке и четвертом столбце матрицы.

</dd> <dt>

*m31* 
</dt> <dd>

Тип: **float**

Значение в третьей строке и первом столбце матрицы.

</dd> <dt>

*M32* 
</dt> <dd>

Тип: **float**

Значение в третьей строке и втором столбце матрицы.

</dd> <dt>

*m33* 
</dt> <dd>

Тип: **float**

Значение в третьей строке и третьем столбце матрицы.

</dd> <dt>

*m34* 
</dt> <dd>

Тип: **float**

Значение в третьей строке и четвертом столбце матрицы.

</dd> <dt>

*m41* 
</dt> <dd>

Тип: **float**

Значение в четвертой строке и первом столбце матрицы.

</dd> <dt>

*m42* 
</dt> <dd>

Тип: **float**

Значение в четвертой строке и втором столбце матрицы.

</dd> <dt>

*m43* 
</dt> <dd>

Тип: **float**

Значение в четвертой строке и третьем столбце матрицы.

</dd> <dt>

*m44* 
</dt> <dd>

Тип: **float**

Значение в четвертой строке и четвертом столбце матрицы.

</dd> <dt>

*m51* 
</dt> <dd>

Тип: **float**

Значение в пятой строке и первом столбце матрицы.

</dd> <dt>

*m52* 
</dt> <dd>

Тип: **float**

Значение в пятой строке и втором столбце матрицы.

</dd> <dt>

*m53* 
</dt> <dd>

Тип: **float**

Значение в пятой строке и третьем столбце матрицы.

</dd> <dt>

*m54* 
</dt> <dd>

Тип: **float**

Значение в пятой и четвертой столбцах матрицы.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы \[ только для настольных приложений Windows Vista\]<br/>                          |
| Минимальная версия сервера<br/> | Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 \[ только классические приложения\]<br/> |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/>                                           |
| Пространство имен<br/>                | D2D1<br/>                                                                                                                   |
| Header<br/>                   | <dl> <dt>\_Вспомогательный метод D2d1. h</dt> </dl>                                         |
| Библиотека<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                               |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Matrix5x4F**](matrix5x4f.md)
</dt> </dl>

 

 





