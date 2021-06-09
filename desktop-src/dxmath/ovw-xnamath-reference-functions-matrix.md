---
description: Содержит список функций матрицы, предоставляемых Директксмас.
ms.assetid: d59d0dcc-deae-3f7e-55c5-0c5ff383343b
title: Функции матрицы Директксмас Library
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a91ecdef8389bf60594d370c2b3de01995bc1169
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826769"
---
# <a name="directxmath-library-matrix-functions"></a>Функции матрицы Директксмас Library

Содержит список функций матрицы, предоставляемых Директксмас.

> [!Note]  
> Директксмас предлагает как левые, так и правые версии функций матрицы с "правой или левой", но всегда предполагает, что это основной формат строки.

 

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                               | Описание                                                                                                                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**ксмматриксаффинетрансформатион**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation)<br/>                     | Формирует матрицу аффинного преобразования.<br/>                                                                                     |
| [**XMMatrixAffineTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation2d)<br/>                 | Строит матрицу 2D-преобразования в плоскости XY. <br/>                                                                  |
| [**ксмматриксдекомпосе**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdecompose)<br/>                                           | Разделяет общую матрицу трехмерного преобразования на скалярные, ротации и преобразованные компоненты.<br/>                   |
| [**ксмматриксдетерминант**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdeterminant)<br/>                                       | Выполняет вычисление определителя матрицы.<br/>                                                                                       |
| [**ксмматриксидентити**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixidentity)<br/>                                             | Формирует матрицу удостоверений.<br/>                                                                                                 |
| [**ксмматриксинверсе**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixinverse)<br/>                                               | Вычисление инверсии матрицы.<br/>                                                                                           |
| [**ксмматриксисидентити**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixisidentity)<br/>                                         | Проверяет, является ли матрица матрицей идентификаторов.<br/>                                                                              |
| [**ксмматриксисинфините**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixisinfinite)<br/>                                         | Проверяет, являются ли какие-либо элементы матрицы положительными или отрицательными бесконечными.<br/>                                            |
| [**ксмматриксиснан**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixisnan)<br/>                                                   | Проверяет, являются ли какие-либо элементы матрицы NaN.<br/>                                                                      |
| [**XMMatrixLookAtLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatlh)<br/>                                             | Строит матрицу представления для левовинтовой системы координат, используя позицию камеры, направление вверх и фокальную точку.<br/>       |
| [**XMMatrixLookAtRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatrh)<br/>                                             | Строит матрицу представления для правовинтовой системы координат, используя позицию камеры, направление вверх и фокальную точку.<br/>      |
| [**XMMatrixLookToLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlooktolh)<br/>                                             | Строит матрицу представления для левовинтовой системы координат, используя позицию камеры, направление вверх и направление камеры.<br/>  |
| [**XMMatrixLookToRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlooktorh)<br/>                                             | Строит матрицу представления для правовинтовой системы координат, используя позицию камеры, направление вверх и направление камеры.<br/> |
| [**ксмматриксмултипли**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiply)<br/>                                             | Выполняет вычисление произведения двух матриц.<br/>                                                                                       |
| [**ксмматриксмултиплитранспосе**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiplytranspose)<br/>                           | Выполняет перестановку произведения двух матриц.<br/>                                                                      |
| [**XMMatrixOrthographicLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographiclh)<br/>                                 | Строит матрицу ортогональной проекции для левовинтовой системы координат.<br/>                                                 |
| [**XMMatrixOrthographicOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterlh)<br/>               | Строит пользовательскую матрицу ортогональной проекции для левовинтовой системы координат.<br/>                                           |
| [**XMMatrixOrthographicOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterrh)<br/>               | Строит пользовательскую матрицу ортогональной проекции для правовинтовой системы координат.<br/>                                          |
| [**XMMatrixOrthographicRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicrh)<br/>                                 | Строит матрицу ортогональной проекции для правовинтовой системы координат.<br/>                                                |
| [**XMMatrixPerspectiveFovLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovlh)<br/>                             | Строит левовинтовую матрицу перспективной проекции на основании поля зрения.<br/>                                                |
| [**XMMatrixPerspectiveFovRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovrh)<br/>                             | Строит правовинтовую матрицу перспективной проекции на основании поля зрения.<br/>                                               |
| [**XMMatrixPerspectiveLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivelh)<br/>                                   | Строит левовинтовую матрицу перспективной проекции.<br/>                                                                         |
| [**XMMatrixPerspectiveOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterlh)<br/>                 | Строит пользовательскую версию левовинтовой матрицы перспективной проекции.<br/>                                                     |
| [**XMMatrixPerspectiveOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterrh)<br/>                 | Строит пользовательскую версию правовинтовой матрицы перспективной проекции.<br/>                                                    |
| [**XMMatrixPerspectiveRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiverh)<br/>                                   | Строит правовинтовую матрицу перспективной проекции.<br/>                                                                        |
| [**ксмматриксрефлект**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixreflect)<br/>                                               | Формирует матрицу преобразования, предназначенную для отражения векторов через заданную плоскость.<br/>                                           |
| [**ксмматриксротатионаксис**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationaxis)<br/>                                     | Строит матрицу, которая поворачивается вокруг произвольной оси.<br/>                                                                      |
| [**ксмматриксротатионнормал**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationnormal)<br/>                                 | Строит матрицу, которая поворачивается вокруг произвольного вектора нормали.<br/>                                                             |
| [**ксмматриксротатионкуатернион**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationquaternion)<br/>                         | Строит матрицу вращения из кватерниона.<br/>                                                                                 |
| [**ксмматриксротатионроллпитчяв**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationrollpitchyaw)<br/>                     | Строит матрицу вращения на основе заданных тон, значения нутации и рулона (Эйлера углы).<br/>                                              |
| [**ксмматриксротатионроллпитчявфромвектор**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationrollpitchyawfromvector)<br/> | Строит матрицу вращения на основе вектора, содержащего Углы Эйлера (шаг, значения нутации и рулон).<br/>                              |
| [**ксмматриксротатионкс**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationx)<br/>                                           | Строит матрицу, которая поворачивается вокруг оси x.<br/>                                                                             |
| [**ксмматриксротатиони**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationy)<br/>                                           | Строит матрицу, которая поворачивается вокруг оси y.<br/>                                                                             |
| [**ксмматриксротатионз**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationz)<br/>                                           | Строит матрицу, которая поворачивается вокруг оси z.<br/>                                                                             |
| [**ксмматриксскалинг**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixscaling)<br/>                                               | Строит матрицу, которая масштабируется вдоль оси x, оси y и оси z.<br/>                                                           |
| [**ксмматриксскалингфромвектор**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixscalingfromvector)<br/>                           | Строит матрицу масштабирования из трехмерного вектора.<br/>                                                                                   |
| [**ксмматрикссет**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixset)<br/>                                                       | Создает матрицу с значениями **float** .<br/>                                                                                     |
| [**ксмматриксшадов**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixshadow)<br/>                                                 | Формирует матрицу преобразования, которая выравнивает геометрию по плоскости.<br/>                                                         |
| [**ксмматрикстрансформатион**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation)<br/>                                 | Формирует матрицу преобразования.<br/>                                                                                             |
| [**XMMatrixTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation2d)<br/>                             | Строит матрицу 2D-преобразования в плоскости XY.<br/>                                                                          |
| [**ксмматрикстранслатион**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranslation)<br/>                                       | Создает матрицу перевода на основе указанных смещений.<br/>                                                                     |
| [**ксмматрикстранслатионфромвектор**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranslationfromvector)<br/>                   | Создает матрицу перевода из вектора.<br/>                                                                                  |
| [**ксмматрикстранспосе**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranspose)<br/>                                           | Выполняет перестановку матрицы.<br/>                                                                                         |
| [**ксмматриксвектортенсорпродукт**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixvectortensorproduct)<br/>                                           | Вычислит внешнее тензорныеное произведение 2 векторов.<br/>                                                                                         |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Функции библиотеки Директксмас](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
