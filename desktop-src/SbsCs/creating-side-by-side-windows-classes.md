---
description: Контексты приложений можно использовать для создания параллельных классов Windows.
ms.assetid: 4941ae1b-f9c6-45ff-b39b-a4078a12a58c
title: Создание параллельных классов Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161732522a12fb6924a2850031d77cff53e44eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910640"
---
# <a name="creating-side-by-side-windows-classes"></a><span data-ttu-id="ab0f4-103">Создание параллельных классов Windows</span><span class="sxs-lookup"><span data-stu-id="ab0f4-103">Creating Side-By-Side Windows Classes</span></span>

<span data-ttu-id="ab0f4-104">Контексты приложений можно использовать для создания параллельных классов Windows.</span><span class="sxs-lookup"><span data-stu-id="ab0f4-104">Application contexts can be used to create side-by-side Windows classes.</span></span> <span data-ttu-id="ab0f4-105">При использовании параллельных классов Windows приложение может одновременно иметь разные версии класса в отдельном родительском окне.</span><span class="sxs-lookup"><span data-stu-id="ab0f4-105">By using side-by-side Windows classes, your application can have different versions of a class active at the same time in a lone parent window.</span></span> <span data-ttu-id="ab0f4-106">Чтобы создать параллельный класс Windows, приложение должно активировать контекст активации перед вызовом [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) для получения маркера для нового окна.</span><span class="sxs-lookup"><span data-stu-id="ab0f4-106">To create a side-by-side Windows class, your application must activate an activation context before calling [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to obtain a handle to the new window.</span></span>

<span data-ttu-id="ab0f4-107">Например, стандартные элементы управления Windows версии 5,82 и 6,0 имеют элемент управления Edit.</span><span class="sxs-lookup"><span data-stu-id="ab0f4-107">For example, Windows Common Controls version 5.82 and version 6.0 both had an Edit control.</span></span> <span data-ttu-id="ab0f4-108">Windows по умолчанию использует элемент управления Edit версии 5,82.</span><span class="sxs-lookup"><span data-stu-id="ab0f4-108">Windows defaults to using the version 5.82 Edit control.</span></span> <span data-ttu-id="ab0f4-109">Чтобы получить параллельное окно с элементом управления редактирования версии 6,0, перед вызовом [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) в обычном режиме приложение может ссылаться на сборку, которая предоставляет именованные классы окон, а затем активировать контекст активации, который ссылается на элементы управления версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="ab0f4-109">To obtain a side-by-side window that has the version 6.0 Edit control, before calling [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) as usual, your application can reference an assembly that exposes named window classes and then activate the activation context that references the version 6.0 controls.</span></span>

 

 
