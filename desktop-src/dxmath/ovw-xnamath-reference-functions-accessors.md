---
description: Содержит список функций доступа к вектору, предоставляемых библиотекой Директксмас.
ms.assetid: 6e7453b8-0dee-6fc5-cbac-fe20e4e3ef60
title: Функции доступа векторной библиотеки Директксмас
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2107638a6ccd5805858b4c67b74c0811675f2492
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701856"
---
# <a name="directxmath-library-vector-accessor-functions"></a>Функции доступа векторной библиотеки Директксмас

Содержит список функций доступа к вектору, предоставляемых библиотекой Директксмас.

Методы доступа вектора Директксмас позволяют разработчикам писать код, который получает и устанавливает отдельные компоненты вектора в переносимом и оптимальном режиме.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                   | Описание                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ксмвекторжетбиндекс**](/previous-versions/windows/desktop/legacy/hh404786(v=vs.85))<br/>             | Получите значение одного из четырех компонентов [**типа данных ксмвектор**](xmvector-data-type.md) , содержащего данные с плавающей запятой по индексу.<br/>                                                                          |
| [**ксмвекторжетбиндексптр**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetbyindexptr)<br/>       | Извлечение в экземпляр объекта с плавающей запятой, на который ссылается указатель, значение одного из четырех компонентов [**типа данных ксмвектор**](xmvector-data-type.md) , содержащего данные с плавающей запятой, на которые ссылается индекс.<br/> |
| [**ксмвекторжетинтбиндекс**](/previous-versions/windows/desktop/legacy/hh404788(v=vs.85))<br/>       | Получите значение одного из четырех компонентов [**типа данных ксмвектор**](xmvector-data-type.md) , содержащего целочисленные данные по индексу.<br/>                                                                                 |
| [**ксмвекторжетинтбиндексптр**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintbyindexptr)<br/> | Извлечение в экземпляр целого числа, на который ссылается указатель, значение одного из четырех компонентов [**типа данных ксмвектор**](xmvector-data-type.md) , содержащего целочисленные данные по индексу.<br/>                          |
| [**ксмвекторжетинтв**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintw)<br/>                   | Получение `w` компонента [**типа данных ксмвектор**](xmvector-data-type.md).<br/>                                                                                                                                        |
| [**ксмвекторжетинтвптр**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintwptr)<br/>             | Извлекает `w` компонент [**типа данных ксмвектор**](xmvector-data-type.md) , содержащего целочисленные данные, и сохраняет значение этого компонента в экземпляре UInt32 \_ t, на который указывает указатель.<br/>                       |
| [**ксмвекторжетинткс**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintx)<br/>                   | Получение `x` компонента [**типа данных ксмвектор**](xmvector-data-type.md).<br/>                                                                                                                                        |
| [**ксмвекторжетинтксптр**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintxptr)<br/>             | Извлекает `x` компонент [**типа данных ксмвектор**](xmvector-data-type.md) , содержащего целочисленные данные, и сохраняет значение этого компонента в экземпляре UInt32 \_ t, на который указывает указатель.<br/>                       |
| [**ксмвекторжетинти**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetinty)<br/>                   | Получение `y` компонента [**типа данных ксмвектор**](xmvector-data-type.md).<br/>                                                                                                                                        |
| [**ксмвекторжетинтиптр**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintyptr)<br/>             | Извлекает `y` компонент [**типа данных ксмвектор**](xmvector-data-type.md) , содержащего целочисленные данные, и сохраняет значение этого компонента в экземпляре UInt32 \_ t, на который указывает указатель.<br/>                       |
| [**ксмвекторжетинтз**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintz)<br/>                   | Получение `z` компонента [**типа данных ксмвектор**](xmvector-data-type.md).<br/>                                                                                                                                        |
| [**ксмвекторжетинтзптр**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintzptr)<br/>             | Извлекает `z` компонент [**типа данных ксмвектор**](xmvector-data-type.md) , содержащего целочисленные данные, и сохраняет значение этого компонента в экземпляре UInt32 \_ t, на который указывает указатель.<br/>                       |
| [**ксмвекторжетв**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetw)<br/>                         | Получение `w` компонента [**типа данных ксмвектор**](xmvector-data-type.md).<br/>                                                                                                                                        |
| [**ксмвекторжетвптр**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetwptr)<br/>                   | Извлечение `w` компонента [**типа данных ксмвектор**](xmvector-data-type.md) , содержащего данные с плавающей запятой, и сохранение значения этого компонента в экземпляре float, на который ссылается указатель.<br/>                    |
| [**ксмвекторжеткс**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetx)<br/>                         | Получение `x` компонента [**типа данных ксмвектор**](xmvector-data-type.md).<br/>                                                                                                                                        |
| [**ксмвекторжетксптр**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetxptr)<br/>                   | Извлечение `x` компонента [**типа данных ксмвектор**](xmvector-data-type.md) , содержащего данные с плавающей запятой, и сохранение значения этого компонента в экземпляре float, на который ссылается указатель.<br/>                    |
| [**ксмвекторжети**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgety)<br/>                         | Получение `y` компонента [**типа данных ксмвектор**](xmvector-data-type.md).<br/>                                                                                                                                        |
| [**ксмвекторжетиптр**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetyptr)<br/>                   | Извлечение `y` компонента [**типа данных ксмвектор**](xmvector-data-type.md) , содержащего данные с плавающей запятой, и сохранение значения этого компонента в экземпляре float, на который ссылается указатель.<br/>                    |
| [**ксмвекторжетз**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetz)<br/>                         | Получение `z` компонента [**типа данных ксмвектор**](xmvector-data-type.md).<br/>                                                                                                                                        |
| [**ксмвекторжетзптр**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetzptr)<br/>                   | Извлечение `z` компонента [**типа данных ксмвектор**](xmvector-data-type.md) , содержащего данные с плавающей запятой, и сохранение значения этого компонента в экземпляре float, на который ссылается указатель.<br/>                    |
| [**ксмвекторсетбиндекс**](/previous-versions/windows/desktop/legacy/hh404810(v=vs.85))<br/>             | Используйте объект с плавающей запятой, чтобы задать значение одного из четырех компонентов [**типа данных ксмвектор**](xmvector-data-type.md) , содержащего целочисленные данные, на которые ссылается индекс.<br/>                                         |
| [**ксмвекторсетбиндексптр**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetbyindexptr)<br/>       | Используйте указатель на экземпляр с плавающей запятой, чтобы задать значение одного из четырех компонентов [**типа данных ксмвектор**](xmvector-data-type.md) , содержащего данные с плавающей запятой, на которые ссылается индекс.<br/>                   |
| [**ксмвекторсетинтбиндекс**](/previous-versions/windows/desktop/legacy/hh404813(v=vs.85))<br/>       | Используйте целочисленный экземпляр, чтобы задать значение одного из четырех компонентов [**типа данных ксмвектор**](xmvector-data-type.md) , содержащего целочисленные данные, на которые ссылается индекс.<br/>                                             |
| [**ксмвекторсетинтбиндексптр**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintbyindexptr)<br/> | Используйте указатель на экземпляр целого числа, чтобы задать значение одного из четырех компонентов [**типа данных ксмвектор**](xmvector-data-type.md) , содержащего целочисленные данные, на которые ссылается индекс.<br/>                                |
| [**ксмвекторсетинтв**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintw)<br/>                   | Задайте значение `w` компонента [**типа данных ксмвектор**](xmvector-data-type.md).<br/>                                                                                                                                |
| [**ксмвекторсетинтвптр**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintwptr)<br/>             | Задает `w` компонент [**ксмвектор**](xmvector-data-type.md) , содержащий целочисленные данные, со значением, содержащимся в экземпляре UInt32 \_ t, на который указывает указатель.<br/>                                                 |
| [**ксмвекторсетинткс**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintx)<br/>                   | Задайте значение `x` компонента [**типа данных ксмвектор**](xmvector-data-type.md).<br/>                                                                                                                                |
| [**ксмвекторсетинтксптр**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintxptr)<br/>             | Задает `x` компонент [**ксмвектор**](xmvector-data-type.md) , содержащий целочисленные данные, со значением, содержащимся в экземпляре UInt32 \_ t, на который указывает указатель.<br/>                                                 |
| [**ксмвекторсетинти**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetinty)<br/>                   | Задайте значение `y` компонента [**типа данных ксмвектор**](xmvector-data-type.md).<br/>                                                                                                                                |
| [**ксмвекторсетинтиптр**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintyptr)<br/>             | Задает `y` компонент [**ксмвектор**](xmvector-data-type.md) , содержащий целочисленные данные, со значением, содержащимся в экземпляре UInt32 \_ t, на который указывает указатель.<br/>                                                 |
| [**ксмвекторсетинтз**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintz)<br/>                   | Задайте значение `z` компонента [**типа данных ксмвектор**](xmvector-data-type.md).<br/>                                                                                                                                |
| [**ксмвекторсетинтзптр**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintzptr)<br/>             | Задает `z` компонент [**ксмвектор**](xmvector-data-type.md) , содержащий целочисленные данные, со значением, содержащимся в экземпляре UInt32 \_ t, на который указывает указатель.<br/>                                                 |
| [**ксмвекторсетв**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetw)<br/>                         | Задайте значение `w` компонента [**типа данных ксмвектор**](xmvector-data-type.md).<br/>                                                                                                                                |
| [**ксмвекторсетвптр**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetwptr)<br/>                   | Задает `w` компонент [**ксмвектор**](xmvector-data-type.md) , содержащий данные с плавающей запятой, со значением, содержащимся в экземпляре float, на который ссылается указатель.<br/>                                              |
| [**ксмвекторсеткс**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetx)<br/>                         | Задайте значение `x` компонента [**типа данных ксмвектор**](xmvector-data-type.md).<br/>                                                                                                                                |
| [**ксмвекторсетксптр**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetxptr)<br/>                   | Задает `x` компонент [**ксмвектор**](xmvector-data-type.md) , содержащий данные с плавающей запятой, со значением, содержащимся в экземпляре float, на который ссылается указатель.<br/>                                              |
| [**ксмвекторсети**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsety)<br/>                         | Задайте значение `y` компонента [**типа данных ксмвектор**](xmvector-data-type.md).<br/>                                                                                                                                |
| [**ксмвекторсетиптр**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetyptr)<br/>                   | Задает `y` компонент [**ксмвектор**](xmvector-data-type.md) , содержащий данные с плавающей запятой, со значением, содержащимся в экземпляре float, на который ссылается указатель.<br/>                                              |
| [**ксмвекторсетз**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetz)<br/>                         | Задайте значение `z` компонента [**типа данных ксмвектор**](xmvector-data-type.md).<br/>                                                                                                                                |
| [**ксмвекторсетзптр**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetzptr)<br/>                   | Задает `z` компонент [**ксмвектор**](xmvector-data-type.md) , содержащий данные с плавающей запятой, со значением, содержащимся в экземпляре float, на который ссылается указатель.<br/>                                              |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Функции библиотеки Директксмас](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
