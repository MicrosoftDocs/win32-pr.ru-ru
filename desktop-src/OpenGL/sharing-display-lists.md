---
title: Совместное использование списков вывода
description: При создании контекста отрисовки он имеет свой собственный список отображения.
ms.assetid: 8ace5684-a27b-4d6e-a80b-58a0b7064879
keywords:
- OpenGL в Windows, совместное использование списков вывода
- Общий доступ списки дисплеев OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d8d012e8e04455f76ca5d7bfe74229ac0b0ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332059"
---
# <a name="sharing-display-lists"></a>Совместное использование списков вывода

При создании контекста отрисовки он имеет свой собственный список отображения. Функция [**вглшарелистс**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists) позволяет контексту отрисовки совместно использовать пространство списка другого контекста визуализации. Любое количество контекстов отрисовки может совместно использовать одно пространство отображения.

 

 




