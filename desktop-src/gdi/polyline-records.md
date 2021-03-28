---
description: Записи ломаной линии — это ряд точек; линии, нарисованные между точками, описывают контур символа.
ms.assetid: 6f0de0bb-ad23-471f-9771-8f28614ee28d
title: Записи ломаной линии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e9a9e87a730d06d15eae219f6f626f1d6d3848
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263657"
---
# <a name="polyline-records"></a>Записи ломаной линии

Записи [ломаной линии](/windows/desktop/api/Wingdi/nf-wingdi-polyline) — это ряд точек; линии, нарисованные между точками, описывают контур символа. Запись ломаной линии начинается с последней точки предыдущей записи (или для первой записи в контуре, начальной точки). Каждая точка в записи находится в структуре глифа и может быть подключена просто с помощью прямых линий.

 

 



