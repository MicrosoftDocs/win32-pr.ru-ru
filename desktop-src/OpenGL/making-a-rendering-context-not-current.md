---
title: Неактуальный контекст подготовки к просмотру
description: Чтобы отсоединить контекст подготовки к просмотру от потока, сделайте его неактуальным. Это можно сделать, вызвав функцию Вглмакекуррент с параметрами, для которых задано значение NULL. Ниже приведен пример этой простой задачи.
ms.assetid: fe76e3d3-5480-448d-95aa-a5af0da309f3
keywords:
- OpenGL на Windows, контексты отрисовки
- Контексты отрисовки OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914bbed6e2d595d23cfcf8dc38820efc18153f4433a2a48446090ec16818b671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937367"
---
# <a name="making-a-rendering-context-not-current"></a>Неактуальный контекст подготовки к просмотру

Чтобы отсоединить контекст подготовки к просмотру от потока, сделайте его неактуальным. Это можно сделать, вызвав функцию [**вглмакекуррент**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) с параметрами, для которых задано **значение NULL**. Ниже приведен пример этой простой задачи.

``` syntax
// detach the current rendering context from the thread  
wglMakeCurrent(NULL, NULL);
```

 

 




