---
description: Windows GDI+ предоставляет плоский API, состоящий из примерно 600 функций. Эти плоские функции API упаковываются классом C++ Аджустаблеарровкап.
ms.assetid: 809d8b1e-ccdd-4156-b650-1bb7443a59fa
title: Функции Аджустаблеарровкап
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52487252c5b684cc762248b35c0fe5f45e8e3759993ba3b99ab01343b84c412d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977834"
---
# <a name="adjustablearrowcap-functions"></a>Функции Аджустаблеарровкап

Windows GDI+ предоставляет плоский API, который состоит из примерно 600 функций, реализованных в Gdiplus.dll и объявленных в гдиплусфлат. h. функции в GDI+ плоском API упаковываются в коллекцию из примерно 40 классов C++. Не рекомендуется напрямую вызывать функции в плоском API. всякий раз, когда вы вызываете GDI+, это необходимо сделать, вызвав методы и функции, предоставляемые оболочками C++. Служба технической поддержки Майкрософт не предоставит поддержку для кода, который напрямую вызывает плоский API. дополнительные сведения об использовании этих методов-оболочек см. в разделе [GDI+ плоский API](-gdiplus-flatapi-flat.md).

Следующие плоские функции API упаковываются классом C++ [**аджустаблеарровкап**](/windows/desktop/api/gdipluslinecaps/nl-gdipluslinecaps-adjustablearrowcap) .

## <a name="adjustablearrowcap-functions-and-corresponding-wrapper-methods"></a>Функции Аджустаблеарровкап и соответствующие методы-оболочки



| Плоская функция                                                                                                          | Метод-оболочка                                                                                                                | Описание                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Гпстатус ВИНГДИПАПИ Гдипкреатеаджустаблеарровкап (ФАКТическая высота, ВЕЩЕСТВЕНная ширина, BOOL, заполнение, Гпаджустаблеарровкап \* \* CAP) | [**Аджустаблеарровкап:: Аджустаблеарровкап**](/windows/win32/api/gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-adjustablearrowcap(inreal_inreal_inbool)) | Создает настраиваемое ограничение линии стрелки с заданной высотой и шириной. Конец линии стрелки может быть заполнен или незаполненным. По умолчанию средняя Вставка равна нулю.                                                                              |
| Гпстатус ВИНГДИПАПИ Гдипсетаджустаблеарровкафеигхт (Гпаджустаблеарровкап \* Cap, вещественная высота)                           | [**Аджустаблеарровкап:: Сесеигхт**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight)                                  | Метод [**аджустаблеарровкап:: сесеигхт**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight) задает высоту наконечника стрелки. Это расстояние от базовой стрелки до вершины.                                 |
| Гпстатус ВИНГДИПАПИ Гдипжетаджустаблеарровкафеигхт (Гпаджустаблеарровкап \* Cap, вещественная \* высота)                         | [**Аджустаблеарровкап:: Height**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight)                                         | Метод [**аджустаблеарровкап:: Height**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight) Получает высоту наконечника стрелки. Высота — это расстояние от базовой стрелки до вершины.                                  |
| Гпстатус ВИНГДИПАПИ Гдипсетаджустаблеарровкапвидс (Гпаджустаблеарровкап \* Cap, вещественная ширина)                             | [**Аджустаблеарровкап:: Сетвидс**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth)                                     | Метод [**аджустаблеарровкап:: сетвидс**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth) задает ширину наконечника стрелки. Ширина — это расстояние между конечными точками в базе стрелки.                          |
| Гпстатус ВИНГДИПАПИ Гдипжетаджустаблеарровкапвидс (Гпаджустаблеарровкап \* Cap, вещественная \* ширина)                           | [**Аджустаблеарровкап:: Полуширинный**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth)                                           | Метод [**аджустаблеарровкап:: полуширинные**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth) Возвращает ширину наконечника стрелки. Ширина — это расстояние между конечными точками в базе стрелки.                                |
| Гпстатус ВИНГДИПАПИ Гдипсетаджустаблеарровкапмиддлеинсет (Гпаджустаблеарровкап \* буквица, Real миддлеинсет)                 | [**Аджустаблеарровкап:: Сетмиддлеинсет**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset)                   | Метод [**аджустаблеарровкап:: сетмиддлеинсет**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset) задает количество единиц, на которое середина базовой перемещается в сторону вершины.                                 |
| Гпстатус ВИНГДИПАПИ Гдипжетаджустаблеарровкапмиддлеинсет (Гпаджустаблеарровкап \* буквица, Real \* миддлеинсет)<br/>    | [**Аджустаблеарровкап:: Жетмиддлеинсет**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset)                               | Метод [**аджустаблеарровкап:: жетмиддлеинсет**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset) получает значение отступа. Средний отступ — это количество единиц, на которое основано смещение базовой точки к вершине. |
| Гпстатус ВИНГДИПАПИ Гдипсетаджустаблеарровкапфиллстате (Гпаджустаблеарровкап \* Cap, bool филлстате)<br/>          | [**Аджустаблеарровкап:: Сетфиллстате**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate)                          | Метод [**аджустаблеарровкап:: сетфиллстате**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate) задает состояние заполнения для наконечника стрелки. Если наконечник стрелки не заполнен, рисуется только контур.                         |
| Гпстатус ВИНГДИПАПИ Гдипжетаджустаблеарровкапфиллстате (Гпаджустаблеарровкап \* Cap, bool \* филлстате)<br/>        | [**Аджустаблеарровкап:: заполнил**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled)                                           | Метод [**аджустаблеарровкап:: Fill**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled) определяет, заполнена ли стрелка.                                                                                               |



 

 

