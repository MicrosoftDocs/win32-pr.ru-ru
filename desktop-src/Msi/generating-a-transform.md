---
description: Следующая процедура описывает сценарий создания преобразования, которое окончательно скрывает функцию.
ms.assetid: 43f36866-a9df-4035-a8ae-5ccbcb628a90
title: Создание преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0543ae74f71155e6fcd504ebee677558f21bbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081069"
---
# <a name="generating-a-transform"></a>Создание преобразования

Следующая процедура описывает сценарий создания преобразования, которое окончательно скрывает функцию.

**Постоянное скрытие функции продукта**

1.  Скопируйте исходный установочный пакет.
2.  Измените копию, установив значение столбца отобразить в [таблице Features](feature-table.md) равным нулю. Это позволяет скрыть функцию.
3.  Создайте преобразование из исходного пакета установки в новые пакеты установки, вызвав [**мсидатабасеженератетрансформ**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma).
4.  Создайте сводные данные в преобразовании, вызвав [**мсикреатетрансформсуммаринфо**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).

Преобразование затем Готово к применению во время установки. Дополнительные сведения см. в разделе [применение преобразований](applying-transforms.md).

 

 



