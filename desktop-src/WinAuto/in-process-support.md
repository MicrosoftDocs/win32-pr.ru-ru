---
title: Поддержка In-Process
description: Текущая реализация динамической аннотации полностью обрабатывается и, следовательно, позволяет закомментировать процессы, владеющие этими элементами пользовательского интерфейса, только элементами пользовательского интерфейса.
ms.assetid: 3d32c444-47fb-49fe-be18-0330fea77926
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4cf9ed1c17d84ddc824ce5ac6d412f1ee12b8e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328947"
---
# <a name="in-process-support"></a><span data-ttu-id="a17a7-103">Поддержка In-Process</span><span class="sxs-lookup"><span data-stu-id="a17a7-103">In-Process Support</span></span>

<span data-ttu-id="a17a7-104">Текущая реализация динамической аннотации полностью обрабатывается и, следовательно, позволяет закомментировать процессы, владеющие этими элементами пользовательского интерфейса, только элементами пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a17a7-104">The current implementation of Dynamic Annotation is entirely in-process and consequently allows only UI elements to be annotated by the process that owns those UI elements.</span></span> <span data-ttu-id="a17a7-105">Один процесс не может закомментировать элементы пользовательского интерфейса другого процесса.</span><span class="sxs-lookup"><span data-stu-id="a17a7-105">It is not possible for one process to annotate the UI elements of another process.</span></span>

<span data-ttu-id="a17a7-106">Обратите внимание, что это влияет только на действие настройки заметки. Он не мешает клиентам обращаться к свойствам (с заметками или иным способом) элементов пользовательского интерфейса в других процессах.</span><span class="sxs-lookup"><span data-stu-id="a17a7-106">Note that this only affects the act of setting an annotation; it does not interfere with the ability of clients to access the properties (annotated or otherwise) of UI elements in other processes.</span></span>

 

 




