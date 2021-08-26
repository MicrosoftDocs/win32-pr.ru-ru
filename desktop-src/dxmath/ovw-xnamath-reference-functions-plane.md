---
description: Список функций плоскости, предоставляемых Директксмас.
ms.assetid: 6505e72e-4af5-5db3-4fc0-f83fa77692b1
title: Функции плоскости библиотеки Директксмас
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a91e58ddad68c31bcc5579b2727891fdddd5b6737761c89d9db70ca21c56bfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841204"
---
# <a name="directxmath-library-plane-functions"></a>Функции плоскости библиотеки Директксмас

Список функций плоскости, предоставляемых Директксмас.

Эти функции используют КСМВЕКТОР 4-Vector для представления коэффициентов уравнения плоскости, AX + by + CZ + D = 0, где X-компонент — это, компонент Y — B, компонент Z — C, а W-компонент — D.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                               | Описание                                                                                                      |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**ксмпланедот**](/windows/win32/api/directxmath/nf-directxmath-xmplanedot)<br/>                         | Вычисляет точку произведения между входной плоскостью и вектором 4D.<br/>                                    |
| [**ксмпланедоткурд**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotcoord)<br/>               | Вычисляет точку произведения между входной плоскостью и трехмерным вектором.<br/>                                    |
| [**ксмпланедотнормал**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotnormal)<br/>             | Вычисляет точку произведения между нормальным вектором плоскости и трехмерным вектором.<br/>                      |
| [**ксмпланикуал**](/windows/win32/api/directxmath/nf-directxmath-xmplaneequal)<br/>                     | Определяет, равны ли две плоскости.<br/>                                                                   |
| [**ксмпланефромпоинтнормал**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompointnormal)<br/> | Выполняет вычисление уравнения плоскости, созданной на основе точки в плоскости и обычного вектора.<br/>           |
| [**ксмпланефромпоинтс**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompoints)<br/>           | Вычисление уравнения плоскости, построенной на основе трех точек в плоскости.<br/>                          |
| [**ксмпланеинтерсектлине**](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectline)<br/>     | Находит пересечение между плоскостью и линией.<br/>                                                    |
| [**ксмпланеинтерсектплане**](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectplane)<br/>   | Находит пересечение двух плоскостей.<br/>                                                                 |
| [**ксмпланеисинфините**](/windows/win32/api/directxmath/nf-directxmath-xmplaneisinfinite)<br/>           | Проверяет, является ли любая из коэффициентов плоскости положительной или отрицательной бесконечностью.<br/>                    |
| [**ксмпланеиснан**](/windows/win32/api/directxmath/nf-directxmath-xmplaneisnan)<br/>                     | Проверяет, является ли ни одно из коэффициентов плоскости значением NaN.<br/>                                            |
| [**ксмпланенеарекуал**](/windows/win32/api/directxmath/nf-directxmath-xmplanenearequal)<br/>             | Определяет, являются ли две плоскости почти равными.<br/>                                                       |
| [**ксмпланенормализе**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalize)<br/>             | Нормализует коэффициенты плоскости таким образом, чтобы коэффициенты координат x, y и z были вектором обычной единицы.<br/> |
| [**ксмпланенормализист**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalizeest)<br/>       | Оценивает коэффициенты плоскости таким образом, что коэффициенты x, y и z образуют вектор нормали единицы.<br/>  |
| [**ксмпланенотекуал**](/windows/win32/api/directxmath/nf-directxmath-xmplanenotequal)<br/>               | Определяет, являются ли две плоскости неравными.<br/>                                                                 |
| [**ксмпланетрансформ**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransform)<br/>             | Преобразует плоскость в заданную матрицу.<br/>                                                                 |
| [**ксмпланетрансформстреам**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransformstream)<br/> | Преобразует поток плоскостей по заданной матрице.<br/>                                                      |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Функции библиотеки Директксмас](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
