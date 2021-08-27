---
description: Описывает типы и структуры библиотеки Директксмас.
ms.assetid: 58acb05d-e79b-8f42-4cf4-76ae57929739
title: Структуры библиотеки Директксмас
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce40aeb51c04f0b5ab76f20b83e2825c33e261862ab3205490aaab855ddb4ec1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117514"
---
# <a name="directxmath-library-structures"></a>Структуры библиотеки Директксмас

Описывает типы и структуры библиотеки Директксмас.

Библиотека Директксмас предоставляет ряд структур и определенных типов для инкапсуляции данных для поддержки простоты использования, оптимизации и переносимости. В следующем списке перечислены структуры, которые в настоящее время входят в библиотеку Директксмас. Они доступны через Директксмас. h.

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|-|-|
| [**XMBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyte2) | 2D-вектор, где каждый компонент является целым числом со знаком, 8 бит (1 байт) в длину. |
| [**XMBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyte4) | Вектор 4D, где каждый компонент имеет целое число со знаком, 8 бит (1 байт) в длину.  |
| [**XMBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyten2) | Двумерный вектор для хранения подписанных нормализованных значений как 8-разрядных (1 байтовых) целых чисел. |
| [**XMBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4) | Трехмерный вектор для хранения подписанных нормализованных значений как 8-разрядных (1 байтовых) целых чисел.  |
| [**ксмколор**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor) | Цветовой вектор 32-разрядного красного зеленого цвета (ARGB), где каждый цветовой канал указан как 8-разрядное целое число без знака. |
| [**XMDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdec4) | Вектор 4D с компонентами x, y и z, представленными в виде 10-разрядных целочисленных значений со знаком, а компонент w-Component — как целое число со знаком, равное 2 битам.  |
| [**XMDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdecn4) | Вектор 4D для хранения подписанных нормализованных значений в виде 10-разрядных компонентов x-, y и z, а также 2-разрядного, подписанного w.  |
| [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2) | 2D-вектор, состоящий из двух значений с плавающей запятой одиночной точности. |
| [**XMFLOAT2A**](/previous-versions/windows/desktop/legacy/ee419469(v=vs.85)) | Описывает структуру [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2) , выравниваемая по 16-байтовой границе. |
| [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) | Описывает трехмерный вектор, состоящий из трех значений с плавающей запятой одиночной точности. |
| [**XMFLOAT3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3a) | Описывает структуру [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) , выравниваемая по 16-байтовой границе. |
| [**XMFLOAT3PK**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk) | Описывает трехмерный вектор с компонентами X и Y, хранящимся в виде 11-разрядного числа с плавающей запятой, и компонент Z, сохраненный в виде 10-разрядного значения с плавающей точкой.  |
| [**XMFLOAT3SE**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se) | Описывает трехмерный вектор трех компонентов с плавающей запятой с 9-битовыми мантиссами, каждый из которых имеет один и тот же показатель «5 бит».  |
| [**XMFLOAT3X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x3) | Матрица с плавающей точкой 3X3. |
| [**XMFLOAT3X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x4) | 3X4 столбец — основная матрица, содержащая 32-разрядные компоненты с плавающей запятой. |
| [**XMFLOAT3X4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x4a) | 3X4 столбец — основная матрица, содержащая 32-разрядные компоненты с плавающей запятой, выравниваемая по 16-байтовой границе. |
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) | Описывает вектор 4D, состоящий из четырех значений с плавающей запятой одиночной точности.  |
| [**XMFLOAT4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4a) | Описывает структуру [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) , выравниваемая по 16-байтовой границе. |
| [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) | Матрица с плавающей точкой 4x3. |
| [**XMFLOAT4X3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3a) | Описывает структуру [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) , выравниваемая по 16-байтовой границе. |
| [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) | Матрица с плавающей точкой 4x4. |
| [**XMFLOAT4X4A**](/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)) | Описывает структуру [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) , выравниваемая по 16-байтовой границе. |
| [**XMHALF2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2) | 2D-вектор, состоящий из двух значений с плавающей запятой половинной точности (16-разрядный).  |
| [**XMHALF4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4) | Описывает вектор 4D, состоящий из четырех значений с плавающей запятой половинной точности (16 бит).  |
| [**XMINT2**](/windows/win32/api/directxmath/ns-directxmath-xmint2) | 2D-вектор, где каждый компонент является целым числом со знаком. |
| [**XMINT3**](/windows/win32/api/directxmath/ns-directxmath-xmint3) | Трехмерный вектор, где каждый компонент является целым числом со знаком. |
| [**XMINT4**](/windows/win32/api/directxmath/ns-directxmath-xmint4) | Вектор 4D, где каждый компонент является целым числом со знаком. |
| [**ксмматрикс**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) | Описывает матрицу 4x4, выравниваемая по 16-байтовой границе, которая сопоставляется с четырьмя аппаратными регистрами вектора. |
| [**XMSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort2) | Описывает двумерный вектор, состоящий из 16-разрядных и нормализованных целочисленных компонентов.  |
| [**XMSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort4) | Вектор 4D, состоящий из 16-разрядных целочисленных компонентов со знаком.  |
| [**XMSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn2) | Двумерный вектор для хранения подписанных, нормализованных значений как 16-разрядных целых чисел со знаком (тип `int16_t` ).  |
| [**XMSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn4) | Вектор 4D для хранения подписанных нормализованных значений как 16-разрядных целых чисел со знаком (тип `int16_t` ).  |
| [**XMU555**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu555) | Вектор 4D с компонентами x, y и z, представленными в виде 5 битовых целочисленных значений без знака, а компонент w-Component — в виде одноразрядного целочисленного значения.  |
| [**XMU565**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565) | Трехмерный вектор с компонентами x и z, представленный как 5-разрядные целочисленные значения без знака, а компонент y — как 6-разрядное целочисленное значение без знака. |
| [**XMUBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyte2) | Описывает 2D-вектор, в котором каждый компонент представляет собой целое число без знака, 8 бит (1 байт) в длину. |
| [**XMUBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyte4) | Описывает вектор 4D, где каждый компонент представляет собой целое число без знака, 8 бит (1 байт) в длину.  |
| [**XMUBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyten2) | Двумерный вектор для хранения беззнаковых нормализованных значений как целые 8-разрядные (1 байтовые) целочисленные значения. |
| [**XMUBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4) | Трехмерный вектор для хранения беззнаковых нормализованных значений как целочисленных 8-разрядных (1 байтовых) целых чисел.  |
| [**XMUDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudec4) | Вектор 4D с компонентами x, y и z, представленными в виде 10-разрядных целочисленных значений без знака, а компонент w-компонента — как целое число без знака в 2 бита.  |
| [**XMUDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudecn4) | Объект 4D для хранения беззнаковых нормализованных целочисленных значений в виде 10-разрядных неподписанных компонентов x-, y и z и 2-разрядного неподписанного w-компонента.  |
| [**XMUINT2**](/windows/win32/api/directxmath/ns-directxmath-xmuint2) | 2D-вектор, где каждый компонент является целым числом без знака. |
| [**XMUINT3**](/windows/win32/api/directxmath/ns-directxmath-xmuint3) | Трехмерный вектор, в котором каждый компонент является целым числом без знака. |
| [**XMUINT4**](/windows/win32/api/directxmath/ns-directxmath-xmuint4) | Вектор 4D, в котором каждый компонент является целым числом без знака. |
| [**XMUNIBBLE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmunibble4) | Вектор 4D с четырьмя неподписанными 4-разрядными целочисленными компонентами.  |
| [**XMUSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort2) | Описывает двумерный вектор, состоящий из 16-разрядных беззнаковых целочисленных компонентов.  |
| [**XMUSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort4) | Вектор 4D, состоящий из 16-разрядных беззнаковых целочисленных компонентов.  |
| [**XMUSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn2) | Двумерный вектор для хранения беззнаковых нормализованных значений как 16-разрядных целых чисел без знака (тип `uint16_t` ).  |
| [**XMUSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn4) | Вектор 4D для хранения беззнаковых нормализованных значений как 16-разрядных целых чисел со знаком (тип `uint16_t` ).  |
| [**XMXDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmxdec4) | Вектор 4D с компонентами x, y и z, представленными в виде 10-разрядных целочисленных значений со знаком, а компонент w-Component — как целое число без знака в 2 бита.  |
| [**XMXDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmxdecn4) | Вектор 4D для хранения подписанных нормализованных значений в виде 10-разрядных компонентов x-, y и z, а также неподписанного значения без знака, нормализованного как 2-разрядное неподписанное.  |

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по программированию Директксмас](ovw-xnamath-reference.md)
</dt> </dl>
