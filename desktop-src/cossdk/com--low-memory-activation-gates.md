---
description: Шлюзы активации COM+ Low-Memory
ms.assetid: 9805dc94-da38-4b2c-b18c-5f494b49691b
title: Шлюзы активации COM+ Low-Memory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad955cb1ed47008f52f1cf9b17edfc43b92aa674
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496074"
---
# <a name="com-low-memory-activation-gates"></a><span data-ttu-id="0fc69-103">Шлюзы активации COM+ Low-Memory</span><span class="sxs-lookup"><span data-stu-id="0fc69-103">COM+ Low-Memory Activation Gates</span></span>

<span data-ttu-id="0fc69-104">Служба "шлюзы активации нехватки памяти COM+" автоматически проверяет память перед созданием сервера или объекта COM+.</span><span class="sxs-lookup"><span data-stu-id="0fc69-104">The COM+ low-memory activation gates service automatically checks memory before a COM+ server or object is created.</span></span> <span data-ttu-id="0fc69-105">Если процентная доля виртуальной памяти, доступная для приложения, падает ниже фиксированного порога, активация завершается ошибкой до создания объекта.</span><span class="sxs-lookup"><span data-stu-id="0fc69-105">If the percentage of virtual memory available to the application falls below a fixed threshold, the activation fails before the object is created.</span></span> <span data-ttu-id="0fc69-106">Таким образом, служба шлюза активации нехватки памяти значительно повышает надежность системы.</span><span class="sxs-lookup"><span data-stu-id="0fc69-106">In this way, the low-memory activation gates service greatly enhances system reliability.</span></span>

<span data-ttu-id="0fc69-107">В следующих разделах содержатся сведения о фоновом и задаче службы шлюза активации нехватки памяти COM+.</span><span class="sxs-lookup"><span data-stu-id="0fc69-107">The following topics provide background and task information about the COM+ low-memory activation gates service.</span></span>



| <span data-ttu-id="0fc69-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="0fc69-108">Topic</span></span>                                                                                                 | <span data-ttu-id="0fc69-109">Описание</span><span class="sxs-lookup"><span data-stu-id="0fc69-109">Description</span></span>                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="0fc69-110">Основные понятия о шлюзах активации COM+ Low-Memory</span><span class="sxs-lookup"><span data-stu-id="0fc69-110">COM+ Low-Memory Activation Gates Concepts</span></span>](com--low-memory-activation-gates-concepts.md)<br/> | <span data-ttu-id="0fc69-111">Содержит общие сведения о службе шлюза активации нехватки памяти COM+.</span><span class="sxs-lookup"><span data-stu-id="0fc69-111">Provides an overview of the COM+ low-memory activation gates service.</span></span><br/>       |
| [<span data-ttu-id="0fc69-112">Задачи шлюза активации COM+ Low-Memory</span><span class="sxs-lookup"><span data-stu-id="0fc69-112">COM+ Low-Memory Activation Gates Tasks</span></span>](com--low-memory-activation-gates-tasks.md)<br/>       | <span data-ttu-id="0fc69-113">Эта функция не настраивается, поэтому нет связанных с ней задач.</span><span class="sxs-lookup"><span data-stu-id="0fc69-113">This feature is not configurable, so there are no tasks associated with it.</span></span><br/> |



 

 

 




