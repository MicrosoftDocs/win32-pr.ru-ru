---
description: Обратите внимание, что этот API не рекомендуется к использованию. Новые приложения не должны использовать его. Тип данных МСПИД определяет назначение Steam мультимедиа.
ms.assetid: 83a84eb7-a72c-4ca7-b152-8cc81a5bfdaf
title: МСПИД (Ммстреам. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8464882aa018a373345f15c0a5639107d9beebf9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689158"
---
# <a name="mspid"></a><span data-ttu-id="4bed9-105">мспид</span><span class="sxs-lookup"><span data-stu-id="4bed9-105">MSPID</span></span>

> [!Note]  
> <span data-ttu-id="4bed9-106">Это нерекомендуемый API.</span><span class="sxs-lookup"><span data-stu-id="4bed9-106">This API is deprecated.</span></span> <span data-ttu-id="4bed9-107">Новые приложения не должны использовать его.</span><span class="sxs-lookup"><span data-stu-id="4bed9-107">New applications should not use it.</span></span>

 

<span data-ttu-id="4bed9-108">Тип данных **мспид** определяет назначение Steam мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4bed9-108">The **MSPID** data type identifies the purpose of a media steam.</span></span>


```C++
typedef GUID MSPID;
typedef REFGUID REFMSPID;
```



## <a name="remarks"></a><span data-ttu-id="4bed9-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4bed9-109">Remarks</span></span>

<span data-ttu-id="4bed9-110">**Мспид** — это просто typedef для идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="4bed9-110">**MSPID** is simply a typedef for GUID.</span></span> <span data-ttu-id="4bed9-111">Определены следующие Мспидс.</span><span class="sxs-lookup"><span data-stu-id="4bed9-111">The following MSPIDs are defined.</span></span>



| <span data-ttu-id="4bed9-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4bed9-112">Value</span></span>               | <span data-ttu-id="4bed9-113">Описание</span><span class="sxs-lookup"><span data-stu-id="4bed9-113">Description</span></span>           |
|---------------------|-----------------------|
| <span data-ttu-id="4bed9-114">МСПИД \_ примаривидео</span><span class="sxs-lookup"><span data-stu-id="4bed9-114">MSPID\_PrimaryVideo</span></span> | <span data-ttu-id="4bed9-115">Основной видеопоток.</span><span class="sxs-lookup"><span data-stu-id="4bed9-115">Primary video stream.</span></span> |
| <span data-ttu-id="4bed9-116">МСПИД \_ примаряудио</span><span class="sxs-lookup"><span data-stu-id="4bed9-116">MSPID\_PrimaryAudio</span></span> | <span data-ttu-id="4bed9-117">Основной звуковой поток.</span><span class="sxs-lookup"><span data-stu-id="4bed9-117">Primary audio stream.</span></span> |



 

<span data-ttu-id="4bed9-118">Тип **рефмспид** определяет ссылку на **мспид**.</span><span class="sxs-lookup"><span data-stu-id="4bed9-118">The **REFMSPID** type defines a reference to an **MSPID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bed9-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4bed9-119">Requirements</span></span>



| <span data-ttu-id="4bed9-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4bed9-120">Requirement</span></span> | <span data-ttu-id="4bed9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4bed9-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4bed9-122">Header</span><span class="sxs-lookup"><span data-stu-id="4bed9-122">Header</span></span><br/> | <dl> <span data-ttu-id="4bed9-123"><dt>Ммстреам. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bed9-123"><dt>Mmstream.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bed9-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4bed9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bed9-125">Типы данных потоковой передачи мультимедиа</span><span class="sxs-lookup"><span data-stu-id="4bed9-125">Multimedia Streaming Data Types</span></span>](multimedia-streaming-data-types.md)
</dt> </dl>

 

 




