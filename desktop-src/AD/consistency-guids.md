---
title: Идентификаторы GUID согласованности
description: Идентификаторы GUID согласованности — это стратегия обнаружения, позволяющая приложению обнаруживать частичные обновления.
ms.assetid: 3418667f-4d5a-4a4b-b0f5-7744a21608f7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcfb25d0f04a459217811a2ff0393fac47e3206
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067268"
---
# <a name="consistency-guids"></a><span data-ttu-id="d5dc4-103">Идентификаторы GUID согласованности</span><span class="sxs-lookup"><span data-stu-id="d5dc4-103">Consistency GUIDs</span></span>

<span data-ttu-id="d5dc4-104">Идентификаторы GUID согласованности — это стратегия обнаружения, позволяющая приложению обнаруживать частичные обновления.</span><span class="sxs-lookup"><span data-stu-id="d5dc4-104">Consistency GUIDs are a detection strategy that allows an application to detect partial updates.</span></span> <span data-ttu-id="d5dc4-105">Идентификатор GUID согласованности (глобальный уникальный идентификатор) применяется к каждому объекту в связанном наборе.</span><span class="sxs-lookup"><span data-stu-id="d5dc4-105">A consistency GUID (Globally Unique IDentifier) is applied to each object in a related set.</span></span> <span data-ttu-id="d5dc4-106">В реализации исходное приложение создает новый идентификатор GUID и применяет его к каждому объекту, который он обновляет, в наборе связанных объектов.</span><span class="sxs-lookup"><span data-stu-id="d5dc4-106">In implementation, a source application generates a new GUID and applies it to each object it updates in the set of related objects.</span></span> <span data-ttu-id="d5dc4-107">Затем он применяет новый идентификатор GUID к остальным объектам в наборе и завершает работу, применяя новый идентификатор GUID к объекту «Master».</span><span class="sxs-lookup"><span data-stu-id="d5dc4-107">It then applies the new GUID to the rest of the objects in the set, and finishes by applying the new GUID to the "master" object.</span></span> <span data-ttu-id="d5dc4-108">Как правило, объект "Master" будет контейнером, который является родительским для других объектов в наборе.</span><span class="sxs-lookup"><span data-stu-id="d5dc4-108">Typically, the "master" object will be a container that is the parent of the other objects in the set.</span></span>

<span data-ttu-id="d5dc4-109">Важные сведения</span><span class="sxs-lookup"><span data-stu-id="d5dc4-109">Some important considerations:</span></span>

-   <span data-ttu-id="d5dc4-110">Идентификаторы GUID согласованности в сочетании с количеством объектов или контрольными суммами более эффективны, чем только идентификаторы GUID согласованности, так как приложение, считывающее объекты, может не узнать, сколько объектов с идентификатором GUID.</span><span class="sxs-lookup"><span data-stu-id="d5dc4-110">Consistency GUIDs combined with object counts or checksums are more effective than consistency GUIDs alone, because the application reading the objects may not know how many objects with the GUID should be present.</span></span>
-   <span data-ttu-id="d5dc4-111">Приложения должны создавать собственные идентификаторы GUID (Microsoft Win32 API, Ууидкреате, предоставляет эту функцию) и не использовать созданные системой идентификаторы GUID, находящиеся в атрибуте **objectGUID** объекта.</span><span class="sxs-lookup"><span data-stu-id="d5dc4-111">Applications must generate their own GUIDs (a Microsoft Win32 API, UuidCreate, provides this function), and not use the system-generated GUIDs found in an object's **objectGUID** attribute.</span></span> <span data-ttu-id="d5dc4-112">Это обусловлено тем, что идентификатор GUID согласованности необходимо изменить каждый раз при обновлении набора объектов.</span><span class="sxs-lookup"><span data-stu-id="d5dc4-112">This is because a consistency GUID needs to change each time the set of objects is updated.</span></span> <span data-ttu-id="d5dc4-113">Идентификаторы GUID идентификаторов объектов, найденные в **objectGUID** , никогда не изменяются после создания объекта.</span><span class="sxs-lookup"><span data-stu-id="d5dc4-113">Object identity GUIDs found in **objectGUID** never change after the object has been created.</span></span>
-   <span data-ttu-id="d5dc4-114">Идентификаторы GUID согласованности предполагают, что ни один объект не является общим для множества, поэтому каждый набор может иметь уникальный идентификатор GUID согласованности.</span><span class="sxs-lookup"><span data-stu-id="d5dc4-114">Consistency GUIDs assume that no object is shared among sets, so each set can have a unique consistency GUID.</span></span>

 

 




