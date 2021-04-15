---
title: Функции Direct2D
description: Direct2D предоставляет следующие функции.
ms.assetid: 1a7ae962-9b70-442c-a676-f172a2d9bfd3
keywords:
- Direct2D, функции
ms.topic: article
ms.date: 09/19/2019
ms.openlocfilehash: 9cbe07a6c1054036030395ff965610919ee48a97
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104488493"
---
# <a name="direct2d-functions"></a>Функции Direct2D

Direct2D предоставляет следующие функции. Дополнительные функции определяются в [пространстве имен D2D1](d2d1-namespace.md).

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|-|-|
| [**D2D1ComputeMaximumScaleFactor**](/windows/desktop/api/d2d1_2/nf-d2d1_2-d2d1computemaximumscalefactor) | Вычисление максимального коэффициента, на который данное преобразование может растянуться для любого вектора. |
| [**D2D1CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) | Создает новое устройство Direct2D, связанное с указанным устройством DXGI.  |
| [**D2D1CreateDeviceContext**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevicecontext) | Создает новый контекст устройства Direct2D, связанный с поверхностью DXGI.  |
| [**D2D1CreateFactory (D2D1_FACTORY_TYPE, РЕФИИД, void \* \* )**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory-r1) | Создает объект фабрики, который можно использовать для создания ресурсов Direct2D. |
| [**D2D1CreateFactory (D2D1_FACTORY_TYPE, РЕФИИД, D2D1_FACTORY_OPTIONS \* , void \* \* )**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) | Создает объект фабрики, который можно использовать для создания ресурсов Direct2D. |
| [**D2D1GetGradientMeshInteriorPointsFromCoonsPatch**](/windows/desktop/api/d2d1_3/nf-d2d1_3-d2d1getgradientmeshinteriorpointsfromcoonspatch) | Возвращает внутренние точки для исправления сетки градиента на основе точек, определяющих исправление Кунс. |
| [**D2D1InvertMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1invertmatrix) | Пытается инвертировать указанную матрицу. |
| [**D2D1IsMatrixInvertible**](/windows/desktop/api/d2d1/nf-d2d1-d2d1ismatrixinvertible) | Указывает, является ли указанная матрица обратимой. |
| [**D2D1MakeRotateMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1makerotatematrix) | Создает преобразование поворота, которое поворачивается на указанный угол относительно заданной точки. |
| [**D2D1MakeSkewMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1makeskewmatrix) | Создает преобразование «наклон» с заданным углом оси x, углом оси y и Центральной точкой.  |
| [**operator \* (const D2D1\MATRIX\3X2\F&, const D2D1\MATRIX\3X2\F&)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-setproduct) | Умножает две матрицы и возвращает результат. |
| [**блобжеттер**](blobgetter.md) | Вызывает обратный вызов метода получения свойства функции-члена для свойства типа BLOB. |
| [**блобсеттер**](blobsetter.md) | Вызывает обратный вызов метода задания свойства для функции-члена для свойства типа BLOB. |
| [**дедуЦингблобжеттер**](deducingblobgetter.md) | Выводит класс и аргументы, а затем вызывает обратный вызов метода получения свойства функции-члена для свойства типа BLOB. |
| [**дедуЦингблобсеттер**](deducingblobsetter.md) | Выводит класс и аргументы, а затем вызывает обратный вызов свойства функции-члена для свойства типа BLOB. |
| [**дедуЦингстрингжеттер**](deducingstringgetter.md) | Выводит класс и аргументы, а затем вызывает обратный вызов метода получения свойства функции-члена для свойства строкового типа. |
| [**дедуЦингстрингсеттер**](deducingstringsetter.md) | Выводит класс и аргументы, а затем вызывает обратный вызов свойства функции-члена для свойства строкового типа. |
| [**дедуЦингвалуежеттер**](deducingvaluegetter.md) | Выводит класс и аргументы, а затем вызывает обратный вызов метода получения свойства функции-члена для свойства типа значения. |
| [**дедуЦингвалуесеттер**](deducingvaluesetter.md) | Выводит класс и аргументы, а затем вызывает обратный вызов свойства функции-члена для свойства типа значения. |
| [**GetType**](/previous-versions/windows/desktop/legacy/hh847962(v=vs.85)) | Извлекает тип данного свойства. |
| [**стрингжеттер**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-stringgetter) | Вызывает обратный вызов метода получения свойства функции-члена для свойства строкового типа. |
| [**стрингсеттер**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-stringsetter) | Вызывает обратный вызов метода задания свойства для функции-члена для свойства строкового типа. |
| [**валуежеттер**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-valuegetter) | Вызывает обратный вызов метода задания свойства для функции-члена для свойства типа значения. |
| [**валуесеттер**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-valuesetter) | Вызывает обратный вызов метода задания свойства для функции-члена для свойства типа значения. |
| [**D2D1ConvertColorSpace**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1convertcolorspace) | Преобразует заданный цвет из одного колорспаце в другой. |
| [**D2D1SinCos**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1sincos) | Возвращает синус и косинус угла. |
| [**D2D1Tan**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1tan) | Возвращает тангенс угла. |
| [**D2D1Vec3Length**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1vec3length) | Возвращает длину трехмерного вектора. |
| [**PD2D1\PROPERTY\GET\FUNCTION**](/windows/desktop/api/D2d1effectauthor/nc-d2d1effectauthor-pd2d1_property_get_function) | Возвращает свойство из результата. |
| [**PD2D1\PROPERTY\SET\FUNCTION**](/windows/desktop/api/D2d1effectauthor/nc-d2d1effectauthor-pd2d1_property_set_function) | Задает свойство для воздействия. |