---
title: Основные понятия программирования C++ и OLE
description: Основные понятия программирования C++ и OLE
ms.assetid: 2c6c3f29-aa5d-4e55-8c4d-16c5fb223fb9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c47ef5ff2d89930b5d4138f12e3ebc15385a7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889180"
---
# <a name="c-and-ole-programming-concepts"></a><span data-ttu-id="e953c-103">Основные понятия программирования C++ и OLE</span><span class="sxs-lookup"><span data-stu-id="e953c-103">C++ and OLE Programming Concepts</span></span>

<span data-ttu-id="e953c-104">Обработчики файлов и потоков, входящие в состав Windows, используют объектно-ориентированную структуру для продвижения стандартного интерфейса и совместного использования функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="e953c-104">The file and stream handlers included with Windows use an object-oriented design to promote a standard interface and to share functionality.</span></span> <span data-ttu-id="e953c-105">Эти обработчики написаны на языке C++ и используют модель объектов OLE Component.</span><span class="sxs-lookup"><span data-stu-id="e953c-105">These handlers are written in C++ and use the OLE Component Object Model.</span></span>

<span data-ttu-id="e953c-106">Вы можете разрабатывать пользовательские обработчики с помощью систем разработки C или C++. Однако настоятельно рекомендуется использовать C++, так как он предоставляет более простой и простой подход к реализации обработчика.</span><span class="sxs-lookup"><span data-stu-id="e953c-106">You can develop custom handlers using the C or C++ development systems; however, using C++ is strongly recommended, because it provides an easier and more straightforward approach to implement a handler.</span></span> <span data-ttu-id="e953c-107">С помощью C++ можно явно определять данные как объекты, а также связывать функции, которые управляют данными, с помощью функций элементов объекта.</span><span class="sxs-lookup"><span data-stu-id="e953c-107">Using C++, you can explicitly define data as objects, and you can associate the functions that manipulate the data with the member functions of an object.</span></span>

<span data-ttu-id="e953c-108">В этом разделе приводится краткое описание важных концепций C++ и объектной модели OLE, применяемой для проектирования и реализации обработчиков файлов и потоков.</span><span class="sxs-lookup"><span data-stu-id="e953c-108">This section identifies and briefly summarizes the important concepts of C++ and the OLE Component Object Model that apply to designing and implementing file and stream handlers.</span></span> <span data-ttu-id="e953c-109">Существует множество книг по программированию на C++, на которые можно ознакомиться за дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="e953c-109">There are many books written about C++ programming that you can reference for more information.</span></span> <span data-ttu-id="e953c-110">Дополнительные сведения о OLE см. в *справочнике по программированию OLE*.</span><span class="sxs-lookup"><span data-stu-id="e953c-110">For more information on OLE, please see the *OLE Programmer's Reference*.</span></span>

 

 




