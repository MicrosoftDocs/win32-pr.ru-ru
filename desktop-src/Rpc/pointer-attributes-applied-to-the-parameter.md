---
title: Атрибуты указателя, применяемые к параметру
description: Каждый атрибут указателя (\ ref \, \ Unique \ и \ PTR \) имеет характеристики, влияющие на выделение памяти. В следующей таблице приведена сводка этих характеристик.
ms.assetid: 25a609cd-efe7-4cbb-b80e-b6a3ad8cda38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c7710fb3c39702b2b2fdb789ed1218dc88d44ea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070451"
---
# <a name="pointer-attributes-applied-to-the-parameter"></a><span data-ttu-id="41102-104">Атрибуты указателя, применяемые к параметру</span><span class="sxs-lookup"><span data-stu-id="41102-104">Pointer Attributes Applied to the Parameter</span></span>

<span data-ttu-id="41102-105">Каждый атрибут указателя ( \[ [ref](/windows/desktop/Midl/ref) \] , \[ [UNIQUE](/windows/desktop/Midl/unique) \] и \[ [ptr](/windows/desktop/Midl/ptr) \] ) имеет характеристики, влияющие на выделение памяти.</span><span class="sxs-lookup"><span data-stu-id="41102-105">Each pointer attribute (\[ [ref](/windows/desktop/Midl/ref)\], \[ [unique](/windows/desktop/Midl/unique)\], and \[ [ptr](/windows/desktop/Midl/ptr)\]) has characteristics that affect memory allocation.</span></span> <span data-ttu-id="41102-106">В следующей таблице приведена сводка этих характеристик.</span><span class="sxs-lookup"><span data-stu-id="41102-106">The following table summarizes these characteristics.</span></span>



| <span data-ttu-id="41102-107">Атрибут указателя</span><span class="sxs-lookup"><span data-stu-id="41102-107">Pointer attribute</span></span>       | <span data-ttu-id="41102-108">Клиент</span><span class="sxs-lookup"><span data-stu-id="41102-108">Client</span></span>                                                                                                                                                                                                            | <span data-ttu-id="41102-109">Сервер</span><span class="sxs-lookup"><span data-stu-id="41102-109">Server</span></span>                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="41102-110">Ссылка ( \[ **ref** \] )</span><span class="sxs-lookup"><span data-stu-id="41102-110">Reference (\[**ref**\])</span></span> | <span data-ttu-id="41102-111">Клиентское приложение должно выделить.</span><span class="sxs-lookup"><span data-stu-id="41102-111">Client application must allocate.</span></span>                                                                                                                                                                                 | <span data-ttu-id="41102-112">Требуется специальная обработка для нонтоп указателей уровня "только для **\[ выхода \]**".</span><span class="sxs-lookup"><span data-stu-id="41102-112">Special handling needed for **\[out\]**-only nontop-level pointers.</span></span> |
| <span data-ttu-id="41102-113">Уникальный ( \[ **уникальный** \] )</span><span class="sxs-lookup"><span data-stu-id="41102-113">Unique (\[**unique**\])</span></span> | <span data-ttu-id="41102-114">Если параметр, клиентское приложение должно выделить; Если внедрено, может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="41102-114">If a parameter, the client application must allocate; if embedded, can be null.</span></span> <span data-ttu-id="41102-115">Переход от NULL к значению, отличному от NULL, приводит к выделению клиентской заглушки; изменение значения, отличного от NULL, может привести к потере.</span><span class="sxs-lookup"><span data-stu-id="41102-115">Changing from null to non-null causes the client stub to allocate; changing from non-null to null can cause orphaning.</span></span><br/> |                                                                     |
| <span data-ttu-id="41102-116">Full ( \[ **ptr** \] )</span><span class="sxs-lookup"><span data-stu-id="41102-116">Full (\[**ptr**\])</span></span>      | <span data-ttu-id="41102-117">Если параметр, клиентское приложение должно выделить; Если внедрено, может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="41102-117">If a parameter, the client application must allocate; if embedded, can be null.</span></span> <span data-ttu-id="41102-118">Переход от NULL к значению, отличному от NULL, приводит к выделению клиентской заглушки; изменение значения, отличного от NULL, может привести к потере.</span><span class="sxs-lookup"><span data-stu-id="41102-118">Changing from null to non-null causes the client stub to allocate; changing from non-null to null can cause orphaning.</span></span><br/> |                                                                     |



 

<span data-ttu-id="41102-119">Атрибут **\[ ref \]** указывает на то, что указатель указывает на допустимую память.</span><span class="sxs-lookup"><span data-stu-id="41102-119">The **\[ref\]** attribute indicates that the pointer points to valid memory.</span></span> <span data-ttu-id="41102-120">По определению клиентское приложение должно выделить всю память, требуемую для ссылочных указателей.</span><span class="sxs-lookup"><span data-stu-id="41102-120">By definition, the client application must allocate all the memory that the reference pointers require.</span></span>

<span data-ttu-id="41102-121">Уникальный указатель может изменяться со значения NULL на значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="41102-121">The unique pointer can change from null to non-null.</span></span> <span data-ttu-id="41102-122">Если уникальный указатель меняется со значения NULL на значение, отличное от NULL, на клиенте выделяется новая память.</span><span class="sxs-lookup"><span data-stu-id="41102-122">If the unique pointer changes from null to non-null, new memory is allocated on the client.</span></span> <span data-ttu-id="41102-123">Если уникальный указатель изменяется со значения, отличного от NULL, результат может быть потерян.</span><span class="sxs-lookup"><span data-stu-id="41102-123">If the unique pointer changes from non-null to null, orphaning can result.</span></span> <span data-ttu-id="41102-124">Дополнительные сведения см. в разделе [потеря памяти](memory-orphaning.md).</span><span class="sxs-lookup"><span data-stu-id="41102-124">For more information, see [Memory Orphaning](memory-orphaning.md).</span></span>

 

