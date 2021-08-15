---
description: Приложение выполняет проверку нажатия для регионов, чтобы определить координаты текущей позиции курсора.
ms.assetid: 861a2558-0967-43f6-be3f-580992da05ff
title: Регионы проверки попадания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5734ffb886bd2978d3ee0b49773d752d4abf43a4d98dc060f3dfaf2956e3084a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118760980"
---
# <a name="hit-testing-regions"></a>Регионы проверки попадания

Приложение выполняет проверку нажатия для регионов, чтобы определить координаты текущей позиции курсора. Затем он передает эти координаты, а также маркер, определяющий регион для функции [**птинрегион**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) . Координаты курсора можно получить, обрабатывая различные сообщения мыши, такие как [**WM \_ лбуттондовн**](../inputdev/wm-lbuttondown.md) , [**WM \_ Лбуттонуп**](../inputdev/wm-lbuttonup.md) , [**WM \_ рбуттондовн**](../inputdev/wm-rbuttondown.md) и [**WM \_ рбуттонуп**](../inputdev/wm-rbuttonup.md). Возвращаемое значение для Птинрегион указывает, находится ли расположение курсора в заданной области.

 

 
