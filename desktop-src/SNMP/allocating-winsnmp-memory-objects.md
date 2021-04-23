---
title: Выделение объектов WinSNMP Memory
description: Дескрипторы ресурсов и строки в стиле C — это три типа объектов памяти в среде WinSNMP.
ms.assetid: 7f51f02b-7c9f-4aa0-b0cf-83551a312e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d70ed4d9d52452b5067a6d1e51392b84f95ccce8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067300"
---
# <a name="allocating-winsnmp-memory-objects"></a><span data-ttu-id="ce93d-103">Выделение объектов WinSNMP Memory</span><span class="sxs-lookup"><span data-stu-id="ce93d-103">Allocating WinSNMP Memory Objects</span></span>

<span data-ttu-id="ce93d-104">Дескрипторы ресурсов и строки в стиле C — это три типа объектов памяти в среде WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="ce93d-104">Descriptors, resource handles and C-style strings are the three types of memory objects in the WinSNMP programming environment.</span></span>

<span data-ttu-id="ce93d-105">Тип объекта определяет, будет ли реализация Microsoft WinSNMP или WinSNMP приложение распределять и освобождать память для объекта.</span><span class="sxs-lookup"><span data-stu-id="ce93d-105">The type of object determines whether the Microsoft WinSNMP implementation or the WinSNMP application allocates and deallocates the memory for the object.</span></span> <span data-ttu-id="ce93d-106">Это сокращает ненужное выделение временного буферного пространства и ненужные копии буферов.</span><span class="sxs-lookup"><span data-stu-id="ce93d-106">This reduces unnecessary allocation of temporary buffer space and unnecessary copying of buffers.</span></span>

<span data-ttu-id="ce93d-107">В следующей таблице приведены сведения о выделении и освобождении ресурсов для объектов WinSNMP Memory.</span><span class="sxs-lookup"><span data-stu-id="ce93d-107">The following table summarizes the allocation and deallocation of resources for WinSNMP memory objects.</span></span>



| <span data-ttu-id="ce93d-108">Тип объекта</span><span class="sxs-lookup"><span data-stu-id="ce93d-108">Object type</span></span>                                                                   | <span data-ttu-id="ce93d-109">Описание:</span><span class="sxs-lookup"><span data-stu-id="ce93d-109">Description</span></span>                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce93d-110">дескриптор [**смиоид**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) или [**смиоктетс**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)</span><span class="sxs-lookup"><span data-stu-id="ce93d-110">[**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) or [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) descriptor</span></span> | <span data-ttu-id="ce93d-111">Если приложение WinSNMP выделяет память, оно должно освободить память с помощью вызова соответствующей функции.</span><span class="sxs-lookup"><span data-stu-id="ce93d-111">If the WinSNMP application allocates the memory, it must deallocate the memory with a call to an appropriate function.</span></span> <span data-ttu-id="ce93d-112">Если реализация выделяет память, приложение должно вызвать функцию [**снмпфридескриптор**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="ce93d-112">If the implementation allocates the memory, the application must call the [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) function to deallocate the memory.</span></span> |
| <span data-ttu-id="ce93d-113">Структура [**смивалуе**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)</span><span class="sxs-lookup"><span data-stu-id="ce93d-113">[**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) structure</span></span>                                    | <span data-ttu-id="ce93d-114">Если элемент value является [**смиоид**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) или дескриптором [**смиоктетс**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) , приложение должно быть продолжено, как указано выше в **параметре** дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="ce93d-114">If the **value** member is an [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) or an [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) descriptor, the application must proceed as indicated above for descriptors.</span></span>                                                                                                     |
| <span data-ttu-id="ce93d-115">Маркер ресурса</span><span class="sxs-lookup"><span data-stu-id="ce93d-115">Resource handle</span></span>                                                               | <span data-ttu-id="ce93d-116">Реализация выделяет, управляет и освобождает память.</span><span class="sxs-lookup"><span data-stu-id="ce93d-116">The implementation allocates, manages, and frees the memory.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="ce93d-117">Строка в стиле C</span><span class="sxs-lookup"><span data-stu-id="ce93d-117">C-style string</span></span>                                                                | <span data-ttu-id="ce93d-118">Приложение WinSNMP должно управлять и освобождать выделенную память.</span><span class="sxs-lookup"><span data-stu-id="ce93d-118">The WinSNMP application must manage and free the memory it allocates.</span></span>                                                                                                                                                                                                                |



 

<span data-ttu-id="ce93d-119">Дополнительные сведения см. в разделе [освобожденные дескрипторы WinSNMP](freeing-winsnmp-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="ce93d-119">For more information, see [Freeing WinSNMP Descriptors](freeing-winsnmp-descriptors.md).</span></span>

 

 




