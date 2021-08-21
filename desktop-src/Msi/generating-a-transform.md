---
description: Следующая процедура описывает сценарий создания преобразования, которое окончательно скрывает функцию.
ms.assetid: 43f36866-a9df-4035-a8ae-5ccbcb628a90
title: Создание преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df605dd01a494089d2e6ecd38c8b3c6d03ecb5d6335e2348682e1af16f79faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635992"
---
# <a name="generating-a-transform"></a>Создание преобразования

Следующая процедура описывает сценарий создания преобразования, которое окончательно скрывает функцию.

**Постоянное скрытие функции продукта**

1.  Скопируйте исходный установочный пакет.
2.  Измените копию, установив значение столбца отобразить в [таблице Features](feature-table.md) равным нулю. Это позволяет скрыть функцию.
3.  Создайте преобразование из исходного пакета установки в новые пакеты установки, вызвав [**мсидатабасеженератетрансформ**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma).
4.  Создайте сводные данные в преобразовании, вызвав [**мсикреатетрансформсуммаринфо**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).

Преобразование затем Готово к применению во время установки. Дополнительные сведения см. в разделе [применение преобразований](applying-transforms.md).

 

 



