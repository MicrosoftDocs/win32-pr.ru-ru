---
title: Эффекты оттенков серого
description: Преобразовывает изображение с использованием монохромных серых оттенков.
ms.assetid: 4e0b26ed-ba71-5f8f-db1e-f1b4e28fbd11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b74e553074b3ee0c9ad4e0d5121b9b084884ddb030c75308eb9964531fc6b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075344"
---
# <a name="grayscale-effect"></a>Эффекты оттенков серого

Преобразовывает изображение с использованием монохромных серых оттенков.

В градациях серого используется Цветовая матрица для преобразования в градации серого с использованием следующей матрицы:

![Матрица преобразования](images/grayscale-effect-matrix.png)

Идентификатором CLSID для этого действия является CLSID \_ D2D1Grayscale.

-   [Пример изображения](#example-image)
-   [Свойства эффектов](#effect-properties)
-   [Требования](#requirements)
-   [Связанные темы](#related-topics)

## <a name="example-image"></a>Пример изображения

![Пример выходных данных эффектов](images/grayscale-effect.png)

## <a name="effect-properties"></a>Свойства эффектов

У этого действия нет свойств.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------------|---------------------------------------------------|
| Минимальная версия клиента | Windows 10 \[ классические приложения \| Windows приложения магазина\] |
| Минимальная версия сервера | Windows 10 \[ классические приложения \| Windows приложения магазина\] |
| Header                   | d2d1effects \_ 2. h                                  |
| Библиотека                  | D2D1. lib, дксгуид. lib                              |


## <a name="related-topics"></a>Связанные темы

* [Интерфейс ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
