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
# <a name="handling-errors-opengl"></a><span data-ttu-id="7764a-105">Обработка ошибок (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="7764a-105">Handling Errors (OpenGL)</span></span>

<span data-ttu-id="7764a-106">Функция **глуеррорстринг** извлекает строки ошибок, соответствующие кодам ошибок OpenGL или Glu.</span><span class="sxs-lookup"><span data-stu-id="7764a-106">The **gluErrorString** function retrieves error strings that correspond to OpenGL or GLU error codes.</span></span> <span data-ttu-id="7764a-107">Определенные в настоящее время коды ошибок OpenGL описаны в [**глжетеррор**](glgeterror.md).</span><span class="sxs-lookup"><span data-stu-id="7764a-107">The currently defined OpenGL error codes are described in [**glGetError**](glgeterror.md).</span></span> <span data-ttu-id="7764a-108">Коды ошибок GLU перечислены в [**глуеррорстринг**](gluerrorstring.md), [*глутесскаллбакк*](glutess.md), [*глукуадриккаллбакк*](gluquadric.md)и [*глунурбскаллбакк*](glunurbs.md).</span><span class="sxs-lookup"><span data-stu-id="7764a-108">The GLU error codes are listed in [**gluErrorString**](gluerrorstring.md), [*gluTessCallback*](glutess.md), [*gluQuadricCallback*](gluquadric.md), and [*gluNurbsCallback*](glunurbs.md).</span></span>

<span data-ttu-id="7764a-109">Возвращаемое значение для **глуеррорстринг** — это указатель на описательную строку, которая соответствует номеру ошибки OpenGL, Glu или глкс, переданному в параметре *ErrorCode* .</span><span class="sxs-lookup"><span data-stu-id="7764a-109">The return value for **gluErrorString** is a pointer to a descriptive string that corresponds to the OpenGL, GLU, or GLX error number passed in the *errorCode* parameter.</span></span> <span data-ttu-id="7764a-110">Определенные коды ошибок описаны в *справочном руководстве по OpenGL* , а также функции или функции, которые могут их создавать.</span><span class="sxs-lookup"><span data-stu-id="7764a-110">The defined error codes are described in the *OpenGL Reference Manual* along with the function or function that can generate them.</span></span>

 

 




