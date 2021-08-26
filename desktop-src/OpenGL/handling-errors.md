---
title: Обработка ошибок (OpenGL)
description: Функция Глуеррорстринг извлекает строки ошибок, соответствующие кодам ошибок OpenGL или GLU.
ms.assetid: 59f93c1c-9d15-4980-b246-19257c66b6b8
keywords:
- Служебная программа OpenGL (GLU), коды ошибок
- GLU (служебная программа OpenGL), коды ошибок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ac3fd9010862dd9c567cb7688f7f96286cae06f7e3b0e4ffe73d3b41ca9b67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035194"
---
# <a name="handling-errors-opengl"></a>Обработка ошибок (OpenGL)

Функция **глуеррорстринг** извлекает строки ошибок, соответствующие кодам ошибок OpenGL или Glu. Определенные в настоящее время коды ошибок OpenGL описаны в [**глжетеррор**](glgeterror.md). Коды ошибок GLU перечислены в [**глуеррорстринг**](gluerrorstring.md), [*глутесскаллбакк*](glutess.md), [*глукуадриккаллбакк*](gluquadric.md)и [*глунурбскаллбакк*](glunurbs.md).

Возвращаемое значение для **глуеррорстринг** — это указатель на описательную строку, которая соответствует номеру ошибки OpenGL, Glu или глкс, переданному в параметре *ErrorCode* . Определенные коды ошибок описаны в *справочном руководстве по OpenGL* , а также функции или функции, которые могут их создавать.

 

 




