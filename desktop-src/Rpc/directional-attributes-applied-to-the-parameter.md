---
title: Атрибуты направления, применяемые к параметру
description: Атрибуты направления \ в \ и \ "определяют, как клиент и сервер распределяют и освобождают память. В следующей таблице приводится сводка по применению атрибутов направления для выделения памяти.
ms.assetid: 21ab54c4-a707-4ee3-bea8-8ba216e25c16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 752432836075b319483e3a17421f691a111689b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672363"
---
# <a name="directional-attributes-applied-to-the-parameter"></a><span data-ttu-id="6d85a-104">Атрибуты направления, применяемые к параметру</span><span class="sxs-lookup"><span data-stu-id="6d85a-104">Directional Attributes Applied to the Parameter</span></span>

<span data-ttu-id="6d85a-105">Атрибуты направления \[ [в](/windows/desktop/Midl/in) \] и \[ [out](/windows/desktop/Midl/out-idl) \] определяют, как клиент и сервер распределяют и освобождают память.</span><span class="sxs-lookup"><span data-stu-id="6d85a-105">The directional attributes \[ [in](/windows/desktop/Midl/in)\] and \[ [out](/windows/desktop/Midl/out-idl)\] determine how the client and server allocate and free memory.</span></span> <span data-ttu-id="6d85a-106">В следующей таблице приводится сводка по применению атрибутов направления для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="6d85a-106">The following table summarizes the effect of directional attributes on memory allocation.</span></span>



| <span data-ttu-id="6d85a-107">Атрибут Direction</span><span class="sxs-lookup"><span data-stu-id="6d85a-107">Directional attribute</span></span>    | <span data-ttu-id="6d85a-108">Память на клиенте</span><span class="sxs-lookup"><span data-stu-id="6d85a-108">Memory on client</span></span>                                                                                            | <span data-ttu-id="6d85a-109">Память на сервере</span><span class="sxs-lookup"><span data-stu-id="6d85a-109">Memory on server</span></span>                                                                                                                                        |
|--------------------------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d85a-110">\[[в](/windows/desktop/Midl/in)\]</span><span class="sxs-lookup"><span data-stu-id="6d85a-110">\[ [in](/windows/desktop/Midl/in)\]</span></span>       | <span data-ttu-id="6d85a-111">Клиентское приложение должно выделить перед вызовом.</span><span class="sxs-lookup"><span data-stu-id="6d85a-111">Client application must allocate before the call.</span></span>                                                           | <span data-ttu-id="6d85a-112">Заглушка сервера выделяет.</span><span class="sxs-lookup"><span data-stu-id="6d85a-112">Server stub allocates.</span></span>                                                                                                                                  |
| <span data-ttu-id="6d85a-113">\[[исходящий трафик](/windows/desktop/Midl/out-idl)\]</span><span class="sxs-lookup"><span data-stu-id="6d85a-113">\[ [out](/windows/desktop/Midl/out-idl)\]</span></span> | <span data-ttu-id="6d85a-114">Заглушка клиента выделяется при возврате.</span><span class="sxs-lookup"><span data-stu-id="6d85a-114">Client stub allocates on return.</span></span>                                                                            | <span data-ttu-id="6d85a-115">Заглушка сервера выделяет только указатель верхнего уровня; серверное приложение должно выделить все внедренные указатели.</span><span class="sxs-lookup"><span data-stu-id="6d85a-115">Server stub allocates top-level pointer only; the server application must allocate all embedded pointers.</span></span> <span data-ttu-id="6d85a-116">Сервер также выделяет новые данные по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="6d85a-116">The server also allocates new data as needed.</span></span> |
| <span data-ttu-id="6d85a-117">\[**в**, **out**\]</span><span class="sxs-lookup"><span data-stu-id="6d85a-117">\[**in**, **out**\]</span></span>      | <span data-ttu-id="6d85a-118">Клиентское приложение должно распределять начальные данные, передаваемые на сервер; Заглушка клиента выделяет дополнительные данные.</span><span class="sxs-lookup"><span data-stu-id="6d85a-118">Client application must allocate initial data transmitted to server; client stub allocates additional data.</span></span> | <span data-ttu-id="6d85a-119">Заглушка сервера выделяет начальные данные, передаваемые от клиента; серверное приложение выделяет новые данные по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="6d85a-119">Server stub allocates initial data transmitted from client; the server application allocates new data as needed.</span></span>                                        |



 

<span data-ttu-id="6d85a-120">Во всех этих случаях клиентская заглушка не освобождает память.</span><span class="sxs-lookup"><span data-stu-id="6d85a-120">In all of these cases the client stub does not free memory.</span></span> <span data-ttu-id="6d85a-121">Клиентское приложение должно освободить память до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="6d85a-121">The client application must free the memory before it terminates.</span></span> <span data-ttu-id="6d85a-122">Заглушка сервера освобождает память при возвращении удаленного вызова процедуры (в соответствии с \[ [](/windows/desktop/Midl/allocate) \] атрибутом выделения ACF).</span><span class="sxs-lookup"><span data-stu-id="6d85a-122">The server stub frees memory when the remote procedure call returns (subject to the \[ [allocate](/windows/desktop/Midl/allocate)\] ACF attribute).</span></span>

 

 