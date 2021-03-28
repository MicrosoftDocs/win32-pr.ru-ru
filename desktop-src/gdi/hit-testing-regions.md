---
description: Приложение выполняет проверку нажатия для регионов, чтобы определить координаты текущей позиции курсора.
ms.assetid: 861a2558-0967-43f6-be3f-580992da05ff
title: Регионы проверки попадания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe136c3ba9ab4babfc1150ae4c3eee878cb42327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263676"
---
# <a name="hit-testing-regions"></a>Регионы проверки попадания

Приложение выполняет проверку нажатия для регионов, чтобы определить координаты текущей позиции курсора. Затем он передает эти координаты, а также маркер, определяющий регион для функции [**птинрегион**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) . Координаты курсора можно получить, обрабатывая различные сообщения мыши, такие как [**WM \_ лбуттондовн**](../inputdev/wm-lbuttondown.md) , [**WM \_ Лбуттонуп**](../inputdev/wm-lbuttonup.md) , [**WM \_ рбуттондовн**](../inputdev/wm-rbuttondown.md) и [**WM \_ рбуттонуп**](../inputdev/wm-rbuttonup.md). Возвращаемое значение для Птинрегион указывает, находится ли расположение курсора в заданной области.

 

 
