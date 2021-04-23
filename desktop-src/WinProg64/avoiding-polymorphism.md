---
title: Предотвращение полиморфизма
description: Новые типы данных включают два полиморфизма типа, INT \_ PTR и long \_ ptr.
ms.assetid: 3d18016d-772c-45bc-8057-7281e71a8707
keywords:
- Полиморфизм 64-разрядное программирование для Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec0fd26944d58a9ba0d253da8b8dbcd68156436
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332099"
---
# <a name="avoiding-polymorphism"></a><span data-ttu-id="cbf3c-104">Предотвращение полиморфизма</span><span class="sxs-lookup"><span data-stu-id="cbf3c-104">Avoiding Polymorphism</span></span>

<span data-ttu-id="cbf3c-105">Новые типы данных включают два полиморфизма типа, **int \_ ptr** и **Long \_ ptr**.</span><span class="sxs-lookup"><span data-stu-id="cbf3c-105">The new data types include two polymorphic types, **INT\_PTR** and **LONG\_PTR**.</span></span> <span data-ttu-id="cbf3c-106">В 32-разрядной Windows значение **int \_ ptr** сопоставляется с **int** и **Long \_ ptr** **.**</span><span class="sxs-lookup"><span data-stu-id="cbf3c-106">On 32-bit Windows, the **INT\_PTR** maps to **int** and the **LONG\_PTR** maps to **long**.</span></span> <span data-ttu-id="cbf3c-107">В 64-разрядных Windows оба типа сопоставляются с встроенным типом **\_ \_ Int64** .</span><span class="sxs-lookup"><span data-stu-id="cbf3c-107">On 64-bit Windows, both types map to the **\_\_int64** intrinsic type.</span></span> <span data-ttu-id="cbf3c-108">Компилятор MIDL поддерживает эти типы для удаленных вызовов процедур, но существует ряд ограничений, которые следует помнить при использовании в распределенной среде.</span><span class="sxs-lookup"><span data-stu-id="cbf3c-108">The MIDL compiler supports these types for remote procedure calls, but there is an inherent limitation that you must keep in mind when using them in a distributed environment.</span></span> <span data-ttu-id="cbf3c-109">Обязательно закомментируйте код соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="cbf3c-109">Be sure to comment your code accordingly.</span></span>

<span data-ttu-id="cbf3c-110">Независимо от размера платформы, размер данных в этих преводных типах всегда равен 32 бит.</span><span class="sxs-lookup"><span data-stu-id="cbf3c-110">Regardless of the platform size, the wire size of these polymorphic types is always 32 bits.</span></span> <span data-ttu-id="cbf3c-111">При распаковке в 64-разрядной версии Windows знак библиотеки времени выполнения расширяет значения со знаком и присваивает нулевое значение байтов в высоком порядке для значения без знака.</span><span class="sxs-lookup"><span data-stu-id="cbf3c-111">When unmarshaling on 64-bit Windows, the run-time library sign extends signed values and assigns zero to the high-order bytes for an unsigned value.</span></span> <span data-ttu-id="cbf3c-112">При помещении в канал 64-битного значения время выполнения усекает байты высокого порядка.</span><span class="sxs-lookup"><span data-stu-id="cbf3c-112">When putting a 64-bit value on the wire, the run time truncates the high-order bytes.</span></span> <span data-ttu-id="cbf3c-113">Поэтому можно использовать только младшие 32-разрядные значения.</span><span class="sxs-lookup"><span data-stu-id="cbf3c-113">Thus, only the low-order 32-bit values are usable.</span></span>

<span data-ttu-id="cbf3c-114">Используйте полиморфизмы, только если это необходимо для переноса.</span><span class="sxs-lookup"><span data-stu-id="cbf3c-114">Use the polymorphic types only when necessary for porting.</span></span> <span data-ttu-id="cbf3c-115">Для новых интерфейсов используйте встроенные целочисленные типы с интерфейсом MIDL **\_ \_ Int32** и **\_ \_ Int64** или используйте тип указателя или маркер контекста, в зависимости от типа передаваемых данных.</span><span class="sxs-lookup"><span data-stu-id="cbf3c-115">For new interfaces, use the MIDL intrinsic integer types **\_\_int32** and **\_\_int64**, or use a pointer type or context handle, whichever is most appropriate for the kind of data being transferred.</span></span>

<span data-ttu-id="cbf3c-116">64-разрядный компилятор поддерживает новый полиморфизм **\_ \_ int3264**.</span><span class="sxs-lookup"><span data-stu-id="cbf3c-116">The 64-bit compiler supports a new polymorphic intrinsic **\_\_int3264**.</span></span> <span data-ttu-id="cbf3c-117">Опять же, этот тип был разработан для поддержки усилий по переносу, в данном случае для прозрачной поддержки типов **uint \_ ptr** .</span><span class="sxs-lookup"><span data-stu-id="cbf3c-117">Again, this type was developed to support porting efforts, in this case to support the **UINT\_PTR** types transparently.</span></span> <span data-ttu-id="cbf3c-118">(Другой внутренний, **\_ \_ long3264**, будет поддерживать тип **типа \_ ulong** .) Не используйте **\_ \_ int3264** напрямую; используйте тип **int \_ ptr** , если требуется тип с полиморфизмом для целей переноса.</span><span class="sxs-lookup"><span data-stu-id="cbf3c-118">(Another intrinsic, **\_\_long3264**, will support the **ULONG\_PTR** type.) Do not use **\_\_int3264** directly; use the **INT\_PTR** type when you need a polymorphic type for porting reasons.</span></span>

 

 




