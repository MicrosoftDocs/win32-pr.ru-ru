---
title: Использование списков вывода
description: Использование списков вывода
ms.assetid: f5edff21-0928-4ec9-9718-5189bf8ce2d7
keywords:
- OpenGL, списки вывода
- Отображение списков OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 793ec78af0b19ac437e44f16e13b93db6eab32a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888052"
---
# <a name="using-display-lists"></a><span data-ttu-id="4776c-105">Использование списков вывода</span><span class="sxs-lookup"><span data-stu-id="4776c-105">Using Display Lists</span></span>

<span data-ttu-id="4776c-106">Список отображений — это группа функций OpenGL, сохраненная для последующего выполнения.</span><span class="sxs-lookup"><span data-stu-id="4776c-106">A display list is a group of OpenGL functions that has been stored for subsequent execution.</span></span> <span data-ttu-id="4776c-107">Функция [**глневлист**](glnewlist.md) начинает создание списка просмотра, а [**глендлист**](glendlist.md) завершает его.</span><span class="sxs-lookup"><span data-stu-id="4776c-107">The [**glNewList**](glnewlist.md) function begins the creation of a display list, and [**glEndList**](glendlist.md) ends it.</span></span> <span data-ttu-id="4776c-108">За некоторыми исключениями в список отображение добавляются функции OpenGL, вызываемые между **глневлист** и **глендлист** .</span><span class="sxs-lookup"><span data-stu-id="4776c-108">With few exceptions, OpenGL functions called between **glNewList** and **glEndList** are appended to the display list.</span></span> <span data-ttu-id="4776c-109">(См. **глневлист** для получения списка функций, которые не могут храниться и выполняться из списка экранов.) Чтобы активировать выполнение списка или набора списков, используйте [**глкалллист**](glcalllist.md) или [**глкалллистс**](glcalllists.md) и укажите идентификационный номер определенного списка или списков.</span><span class="sxs-lookup"><span data-stu-id="4776c-109">(See **glNewList** for a list of the functions that you can't store and execute from within a display list.) To trigger the execution of a list or set of lists, use [**glCallList**](glcalllist.md) or [**glCallLists**](glcalllists.md) and supply the identifying number of a particular list or lists.</span></span> <span data-ttu-id="4776c-110">Вы управляете индексами, используемыми для обнаружения списков вывода с помощью [**глженлистс**](glgenlists.md), [**гллистбасе**](gllistbase.md)и [**глислист**](glislist.md).</span><span class="sxs-lookup"><span data-stu-id="4776c-110">You manage the indexes used to identify display lists with [**glGenLists**](glgenlists.md), [**glListBase**](gllistbase.md), and [**glIsList**](glislist.md).</span></span> <span data-ttu-id="4776c-111">Чтобы удалить набор списков вывода, используйте [**глделетелистс**](gldeletelists.md).</span><span class="sxs-lookup"><span data-stu-id="4776c-111">To delete a set of display lists, use [**glDeleteLists**](gldeletelists.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4776c-112">См. также</span><span class="sxs-lookup"><span data-stu-id="4776c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4776c-113">Справочник по отображаемым спискам</span><span class="sxs-lookup"><span data-stu-id="4776c-113">Display Lists Reference</span></span>](display-lists-reference.md)
</dt> </dl>

 

 




