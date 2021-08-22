---
title: Расширение функций OpenGL
description: Библиотека OpenGL поддерживает несколько реализаций своих функций.
ms.assetid: 9eb08fd4-899a-4610-9491-d7f377a19b46
keywords:
- OpenGL на Windows, функции расширения
- функции расширения OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dce68498d5a3e672e63da1ae05d9bb513a4121d110237d90cdad75df0ff84d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361346"
---
# <a name="extending-opengl-functions"></a>Расширение функций OpenGL

Библиотека OpenGL поддерживает несколько реализаций своих функций. Функции расширения, поддерживаемые в одном контексте отрисовки, не обязательно поддерживаются в другом контексте отрисовки. Для данного контекста отрисовки в приложении, использующем функции расширения, используйте только адреса функций, возвращенные функцией [**вглжетпрокаддресс**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress) .

 

 




