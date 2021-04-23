---
title: Атрибуты производительности
description: Используйте следующие атрибуты в IDL-файле, чтобы уменьшить размер кода-заглушки или иным образом повысить производительность.
ms.assetid: 0f23265e-7f3e-4a15-ac3b-1d852a8110eb
keywords:
- IDL-MIDL, атрибуты, производительность
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbfa518b400d237c9fd3789f61b7e74a0c38276
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068613"
---
# <a name="performance-attributes"></a><span data-ttu-id="3a176-104">Атрибуты производительности</span><span class="sxs-lookup"><span data-stu-id="3a176-104">Performance Attributes</span></span>

<span data-ttu-id="3a176-105">Используйте следующие атрибуты в IDL-файле, чтобы уменьшить размер кода-заглушки или иным образом повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="3a176-105">Use the following attributes in an IDL file to reduce the size of the stub code or otherwise improve performance.</span></span>



| <span data-ttu-id="3a176-106">attribute</span><span class="sxs-lookup"><span data-stu-id="3a176-106">Attribute</span></span>                             | <span data-ttu-id="3a176-107">Использование</span><span class="sxs-lookup"><span data-stu-id="3a176-107">Usage</span></span>                                                                                                                                                |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a176-108">**обращать**</span><span class="sxs-lookup"><span data-stu-id="3a176-108">**ignore**</span></span>](ignore.md)              | <span data-ttu-id="3a176-109">Указывает, что указатель, содержащийся в структуре или объединении, и объект, указанный указателем, не передаются.</span><span class="sxs-lookup"><span data-stu-id="3a176-109">Designates that a pointer contained in a structure or union and the object indicated by the pointer is not to be transmitted.</span></span>                        |
| [<span data-ttu-id="3a176-110">**Языковые**</span><span class="sxs-lookup"><span data-stu-id="3a176-110">**local**</span></span>](local.md)                | <span data-ttu-id="3a176-111">Определяет локальную функцию для приложения, для которой MIDL не должен создавать код-заглушку.</span><span class="sxs-lookup"><span data-stu-id="3a176-111">Designates a function that is local to the application for which MIDL does not need to generate stub code.</span></span>                                           |
| [<span data-ttu-id="3a176-112">**проводное \_ маршалирование**</span><span class="sxs-lookup"><span data-stu-id="3a176-112">**wire\_marshal**</span></span>](wire-marshal.md) | <span data-ttu-id="3a176-113">Определяет тип данных как более простой тип для передачи по сети и позволяет реализовать упаковку и деупаковку подпрограмм для типа.</span><span class="sxs-lookup"><span data-stu-id="3a176-113">Defines a data type as a simpler type for transmission over a network and allows you to implement marshaling and unmarshaling routines for the type.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3a176-114">См. также</span><span class="sxs-lookup"><span data-stu-id="3a176-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a176-115">Атрибуты ACF управления памятью</span><span class="sxs-lookup"><span data-stu-id="3a176-115">Memory Management ACF Attributes</span></span>](memory-management-acf-attributes.md)
</dt> <dt>

[<span data-ttu-id="3a176-116">Атрибуты ACF для оптимизации заглушек</span><span class="sxs-lookup"><span data-stu-id="3a176-116">Stub Optimization ACF Attributes</span></span>](stub-optimization-acf-attributes.md)
</dt> </dl>

 

 




