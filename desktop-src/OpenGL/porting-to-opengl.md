---
title: Перенос в OpenGL
description: Перенос в OpenGL
ms.assetid: 6799e10b-2f7c-4516-92ea-43667784f8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8efd2a34ac5d7fb6fc52aef3f24a556712b2c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411118"
---
# <a name="porting-to-opengl"></a><span data-ttu-id="fa5e4-103">Перенос в OpenGL</span><span class="sxs-lookup"><span data-stu-id="fa5e4-103">Porting to OpenGL</span></span>

<span data-ttu-id="fa5e4-104">OpenGL предназначен для обеспечения совместимости в операционных системах и оборудовании.</span><span class="sxs-lookup"><span data-stu-id="fa5e4-104">OpenGL is designed for compatibility across hardware and operating systems.</span></span> <span data-ttu-id="fa5e4-105">Такая схема упрощает для программистов перенос программ OpenGL с одной системы на другую.</span><span class="sxs-lookup"><span data-stu-id="fa5e4-105">This design makes it easier for programmers to port OpenGL programs from one system to another.</span></span> <span data-ttu-id="fa5e4-106">Хотя каждая операционная система имеет уникальные требования, большая часть кода OpenGL в текущих программах может использоваться как есть.</span><span class="sxs-lookup"><span data-stu-id="fa5e4-106">While each operating system has unique requirements, much of the OpenGL code in your current programs can be used as is.</span></span> <span data-ttu-id="fa5e4-107">Чтобы перенести приложение OpenGL в Microsoft Windows, необходимо изменить программы для работы с системными окнами Windows.</span><span class="sxs-lookup"><span data-stu-id="fa5e4-107">To port your OpenGL application to Microsoft Windows, you'll have to modify your programs to work with the Windows windowing systems.</span></span>

<span data-ttu-id="fa5e4-108">В целом приложения переносятся на OpenGL для Windows с одной из двух платформ:</span><span class="sxs-lookup"><span data-stu-id="fa5e4-108">In general applications are ported to OpenGL for Windows from one of two platforms:</span></span>

-   <span data-ttu-id="fa5e4-109">Приложения OpenGL, разработанные для системы Window X и библиотеки X (Кслиб)</span><span class="sxs-lookup"><span data-stu-id="fa5e4-109">OpenGL applications developed for the X Window System and the X library (Xlib)</span></span>
-   <span data-ttu-id="fa5e4-110">Приложения IRI GL</span><span class="sxs-lookup"><span data-stu-id="fa5e4-110">IRIS GL applications</span></span>

<span data-ttu-id="fa5e4-111">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="fa5e4-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="fa5e4-112">Общие сведения о переносе в OpenGL для Windows</span><span class="sxs-lookup"><span data-stu-id="fa5e4-112">Introduction to Porting to OpenGL for Windows</span></span>](introduction-to-porting-to-opengl-for-windows-nt--windows-2000--and-windows-95-98.md)
-   [<span data-ttu-id="fa5e4-113">Функции OpenGL и их эквиваленты ДИАФРАГМы в ГК</span><span class="sxs-lookup"><span data-stu-id="fa5e4-113">OpenGL Functions and Their IRIS GL Equivalents</span></span>](opengl-functions-and-their-iris-gl-equivalents.md)
-   [<span data-ttu-id="fa5e4-114">Различия в ГК и OpenGL для IRI</span><span class="sxs-lookup"><span data-stu-id="fa5e4-114">IRIS GL and OpenGL Differences</span></span>](iris-gl-and-opengl-differences.md)

 

 




