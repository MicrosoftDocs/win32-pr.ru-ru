---
description: Содержит список векторных арифметических функций.
ms.assetid: d7ed4516-74a6-81ec-79a2-2e39cf112d11
title: Векторные арифметические функции
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 783e60ad3ca17b7394fc801baaeedd61d89649b2f4ae5ccd3b3fa7e774ff6a4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118500354"
---
# <a name="vector-arithmetic-functions"></a>Векторные арифметические функции

Содержит список векторных арифметических функций.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                   | Описание                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**ксмвекторабс**](/windows/win32/api/directxmath/nf-directxmath-xmvectorabs)<br/>                                           | Выполняет вычисление абсолютного значения каждого компонента [**ксмвектор**](xmvector-data-type.md).<br/>                    |
| [**ксмвекторадд**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)<br/>                                           | Вычисляет сумму двух векторов.<br/>                                                                               |
| [**ксмвекторадданглес**](/windows/win32/api/directxmath/nf-directxmath-xmvectoraddangles)<br/>                               | Складывает два вектора, представляющие углы.<br/>                                                                          |
| [**ксмвекторцеилинг**](/windows/win32/api/directxmath/nf-directxmath-xmvectorceiling)<br/>                                   | Вычисление самого потолока каждого компонента [**ксмвектор**](xmvector-data-type.md).<br/>                           |
| [**ксмвекторкламп**](/windows/win32/api/directxmath/nf-directxmath-xmvectorclamp)<br/>                                       | Применяет фиксацию компонентов вектора к указанному минимальному и максимальному диапазону.<br/>                                    |
| [**ксмвектордивиде**](/windows/win32/api/directxmath/nf-directxmath-xmvectordivide)<br/>                                     | Делит один экземпляр `XMVECTOR` на второй экземпляр, возвращая результат в третьем экземпляре.<br/>             |
| [**ксмвекторфлур**](/windows/win32/api/directxmath/nf-directxmath-xmvectorfloor)<br/>                                       | Вычисляются основания каждого компонента [**ксмвектор**](xmvector-data-type.md).<br/>                             |
| [**ксмвекторисинфините**](/windows/win32/api/directxmath/nf-directxmath-xmvectorisinfinite)<br/>                             | Выполняет тест для каждого компонента в векторе +/-Infinity.<br/>                                                    |
| [**ксмвекториснан**](/windows/win32/api/directxmath/nf-directxmath-xmvectorisnan)<br/>                                       | Выполняет проверку NaN для каждого компонента в векторе.<br/>                                                                 |
| [**ксмвектормакс**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)<br/>                                           | Выполняет сравнение каждого компонента между двумя векторами и возвращает вектор, содержащий самые большие компоненты.<br/>  |
| [**ксмвектормин**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)<br/>                                           | Выполняет сравнение каждого компонента между двумя векторами и возвращает вектор, содержащий наименьшие компоненты.<br/> |
| [**ксмвектормод**](/windows/win32/api/directxmath/nf-directxmath-xmvectormod)<br/>                                           | Выполняет вычисление остатка числа с плавающей запятой для каждого компонента в частях двух векторов.<br/>                            |
| [**ксмвектормоданглес**](/windows/win32/api/directxmath/nf-directxmath-xmvectormodangles)<br/>                               | Выполняет вычисление угла для каждого компонента в 2PI.<br/>                                                                   |
| [**ксмвектормултипли**](/windows/win32/api/directxmath/nf-directxmath-xmvectormultiply)<br/>                                 | Выполняет вычисление произведения для каждого компонента двух векторов.<br/>                                                             |
| [**ксмвектормултиплядд**](/windows/win32/api/directxmath/nf-directxmath-xmvectormultiplyadd)<br/>                           | Выполняет вычисление произведения первых двух векторов, добавленных к третьему вектору.<br/>                                       |
| [**ксмвекторнегате**](/windows/win32/api/directxmath/nf-directxmath-xmvectornegate)<br/>                                     | Вычисление отрицания вектора.<br/>                                                                             |
| [**ксмвекторнегативемултиплисубтракт**](/windows/win32/api/directxmath/nf-directxmath-xmvectornegativemultiplysubtract)<br/> | Вычисление разности между третьим вектором и произведением первых двух векторов.<br/>                            |
| [**ксмвекторпов**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)<br/>                                           | Выводит значение *v1* , возведенное в степень *2*.<br/>                                                                     |
| [**ксмвекторреЦипрокал**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocal)<br/>                             | Выполняет вычисление обратной стороны для каждого компонента вектора.<br/>                                                             |
| [**ксмвекторреЦипрокалест**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalest)<br/>                       | Вычисляет значение обратной стороны вектора для каждого компонента.<br/>                                                            |
| [**ксмвекторреЦипрокалскрт**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalsqrt)<br/>                     | Вычисляет однокомпонентный квадратный корень в векторе.<br/>                                                 |
| [**ксмвекторреЦипрокалскртест**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalsqrtest)<br/>               | Оценивает однокомпонентный квадратный корень в векторе.<br/>                                                |
| [**ксмвекторраунд**](/windows/win32/api/directxmath/nf-directxmath-xmvectorround)<br/>                                       | Округляет каждый компонент вектора до ближайшего целого числа.<br/>                                                      |
| [**ксмвекторсатурате**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsaturate)<br/>                                 | Насыщенность каждого компонента вектора в диапазоне от 0,0 f до 1,0 f.<br/>                                                |
| [**ксмвекторскале**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)<br/>                                       | Скалярная величина умножает вектор на значение с плавающей запятой.<br/>                                                          |
| [**ксмвекторскрт**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsqrt)<br/>                                         | Вычисляет квадратный корень для каждого компонента вектора.<br/>                                                            |
| [**ксмвекторскртест**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsqrtest)<br/>                                   | Оценивает квадратный корень для каждого компонента вектора.<br/>                                                           |
| [**ксмвекторсубтракт**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)<br/>                                 | Вычисление разности двух векторов.<br/>                                                                        |
| [**ксмвекторсубтрактанглес**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtractangles)<br/>                     | Вычитает два вектора, представляющие углы.<br/>                                                                     |
| [**ксмвекторсум**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsum)<br/>                                           | Вычисляет горизонтальную сумму компонентов [**ксмвектор**](xmvector-data-type.md).<br/>                    |
| [**ксмвектортрункате**](/windows/win32/api/directxmath/nf-directxmath-xmvectortruncate)<br/>                                 | Округляет каждый компонент вектора до ближайшего целочисленного значения в направлении нуля.<br/>                       |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Функции векторной библиотеки Директксмас](ovw-xnamath-reference-functions-vector.md)
</dt> </dl>

 

 
