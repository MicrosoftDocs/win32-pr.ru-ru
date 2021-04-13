---
title: Обработка ошибок (OpenGL)
description: Функция Глуеррорстринг извлекает строки ошибок, соответствующие кодам ошибок OpenGL или GLU.
ms.assetid: 59f93c1c-9d15-4980-b246-19257c66b6b8
keywords:
- Служебная программа OpenGL (GLU), коды ошибок
- GLU (служебная программа OpenGL), коды ошибок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab319fd978cd5ea901133fc9961caf1c66f3185d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340020"
---
# <a name="handling-errors-opengl"></a>Обработка ошибок (OpenGL)

Функция **глуеррорстринг** извлекает строки ошибок, соответствующие кодам ошибок OpenGL или Glu. Определенные в настоящее время коды ошибок OpenGL описаны в [**глжетеррор**](glgeterror.md). Коды ошибок GLU перечислены в [**глуеррорстринг**](gluerrorstring.md), [*глутесскаллбакк*](glutess.md), [*глукуадриккаллбакк*](gluquadric.md)и [*глунурбскаллбакк*](glunurbs.md).

Возвращаемое значение для **глуеррорстринг** — это указатель на описательную строку, которая соответствует номеру ошибки OpenGL, Glu или глкс, переданному в параметре *ErrorCode* . Определенные коды ошибок описаны в *справочном руководстве по OpenGL* , а также функции или функции, которые могут их создавать.

 

 




