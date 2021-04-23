---
description: Интерфейс Искардкмд предоставляет следующие методы.
ms.assetid: C5CC6A53-FF4B-4B54-B495-B6D43A382C09
title: Методы Искардкмд
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f8b1087f0baebc73785f7878f4eff528960413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072764"
---
# <a name="iscardcmd-methods"></a><span data-ttu-id="5eef9-103">Методы Искардкмд</span><span class="sxs-lookup"><span data-stu-id="5eef9-103">ISCardCmd Methods</span></span>

<span data-ttu-id="5eef9-104">Интерфейс [**искардкмд**](iscardcmd.md) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="5eef9-104">The [**ISCardCmd**](iscardcmd.md) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5eef9-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="5eef9-105">In this section</span></span>

-   [<span data-ttu-id="5eef9-106">**Метод Буилдкмд**</span><span class="sxs-lookup"><span data-stu-id="5eef9-106">**BuildCmd Method**</span></span>](iscardcmd-buildcmd.md)
-   [<span data-ttu-id="5eef9-107">**Метод Clear**</span><span class="sxs-lookup"><span data-stu-id="5eef9-107">**Clear Method**</span></span>](iscardcmd-clear.md)
-   [<span data-ttu-id="5eef9-108">**Метод инкапсуляции**</span><span class="sxs-lookup"><span data-stu-id="5eef9-108">**Encapsulate Method**</span></span>](iscardcmd-encapsulate.md)
-   [<span data-ttu-id="5eef9-109">**получение \_ метода алтернатеклассид**</span><span class="sxs-lookup"><span data-stu-id="5eef9-109">**get\_AlternateClassId Method**</span></span>](iscardcmd-get-alternateclassid.md)
-   [<span data-ttu-id="5eef9-110">**получение \_ метода категориях APDU**</span><span class="sxs-lookup"><span data-stu-id="5eef9-110">**get\_Apdu Method**</span></span>](iscardcmd-get-apdu.md)
-   [<span data-ttu-id="5eef9-111">**получение \_ метода апдуленгс**</span><span class="sxs-lookup"><span data-stu-id="5eef9-111">**get\_ApduLength Method**</span></span>](iscardcmd-get-apdulength.md)
-   [<span data-ttu-id="5eef9-112">**получение \_ метода апдурепли**</span><span class="sxs-lookup"><span data-stu-id="5eef9-112">**get\_ApduReply Method**</span></span>](iscardcmd-get-apdureply.md)
-   [<span data-ttu-id="5eef9-113">**получение \_ метода апдуреплиленгс**</span><span class="sxs-lookup"><span data-stu-id="5eef9-113">**get\_ApduReplyLength Method**</span></span>](iscardcmd-get-apdureplylength.md)
-   [<span data-ttu-id="5eef9-114">**получение \_ метода ClassID**</span><span class="sxs-lookup"><span data-stu-id="5eef9-114">**get\_ClassId Method**</span></span>](iscardcmd-get-classid.md)
-   [<span data-ttu-id="5eef9-115">**получение \_ метода данных**</span><span class="sxs-lookup"><span data-stu-id="5eef9-115">**get\_Data Method**</span></span>](iscardcmd-get-data.md)
-   [<span data-ttu-id="5eef9-116">**получение \_ метода инструктионид**</span><span class="sxs-lookup"><span data-stu-id="5eef9-116">**get\_InstructionId Method**</span></span>](iscardcmd-get-instructionid.md)
-   [<span data-ttu-id="5eef9-117">**получение \_ метода лефиелд**</span><span class="sxs-lookup"><span data-stu-id="5eef9-117">**get\_LeField Method**</span></span>](iscardcmd-get-lefield.md)
-   [<span data-ttu-id="5eef9-118">**получение \_ метода P1**</span><span class="sxs-lookup"><span data-stu-id="5eef9-118">**get\_P1 Method**</span></span>](iscardcmd-get-p1.md)
-   [<span data-ttu-id="5eef9-119">**получение \_ метода P2**</span><span class="sxs-lookup"><span data-stu-id="5eef9-119">**get\_P2 Method**</span></span>](iscardcmd-get-p2.md)
-   [<span data-ttu-id="5eef9-120">**получение \_ метода P3**</span><span class="sxs-lookup"><span data-stu-id="5eef9-120">**get\_P3 Method**</span></span>](iscardcmd-get-p3.md)
-   [<span data-ttu-id="5eef9-121">**получение \_ метода реплинад**</span><span class="sxs-lookup"><span data-stu-id="5eef9-121">**get\_ReplyNad Method**</span></span>](iscardcmd-get-replynad.md)
-   [<span data-ttu-id="5eef9-122">**получение \_ метода реплистатус**</span><span class="sxs-lookup"><span data-stu-id="5eef9-122">**get\_ReplyStatus Method**</span></span>](iscardcmd-get-replystatus.md)
-   [<span data-ttu-id="5eef9-123">**получение \_ метода ReplyStatusSW1**</span><span class="sxs-lookup"><span data-stu-id="5eef9-123">**get\_ReplyStatusSW1 Method**</span></span>](iscardcmd-get-replystatussw1.md)
-   [<span data-ttu-id="5eef9-124">**получение \_ метода ReplyStatusSW2**</span><span class="sxs-lookup"><span data-stu-id="5eef9-124">**get\_ReplyStatusSW2 Method**</span></span>](iscardcmd-get-replystatussw2.md)
-   [<span data-ttu-id="5eef9-125">**\_метод алтернатеклассид**</span><span class="sxs-lookup"><span data-stu-id="5eef9-125">**put\_AlternateClassId Method**</span></span>](iscardcmd-put-alternateclassid.md)
-   [<span data-ttu-id="5eef9-126">**\_метод категориях APDU**</span><span class="sxs-lookup"><span data-stu-id="5eef9-126">**put\_Apdu Method**</span></span>](iscardcmd-put-apdu.md)
-   [<span data-ttu-id="5eef9-127">**\_метод апдурепли**</span><span class="sxs-lookup"><span data-stu-id="5eef9-127">**put\_ApduReply Method**</span></span>](iscardcmd-put-apdureply.md)
-   [<span data-ttu-id="5eef9-128">**Размещение \_ метода ClassID**</span><span class="sxs-lookup"><span data-stu-id="5eef9-128">**put\_ClassId Method**</span></span>](iscardcmd-put-classid.md)
-   [<span data-ttu-id="5eef9-129">**\_метод размещения данных**</span><span class="sxs-lookup"><span data-stu-id="5eef9-129">**put\_Data Method**</span></span>](iscardcmd-put-data.md)
-   [<span data-ttu-id="5eef9-130">**\_метод инструктионид**</span><span class="sxs-lookup"><span data-stu-id="5eef9-130">**put\_InstructionId Method**</span></span>](iscardcmd-put-instructionid.md)
-   [<span data-ttu-id="5eef9-131">**разместить \_ метод NAD**</span><span class="sxs-lookup"><span data-stu-id="5eef9-131">**put\_Nad Method**</span></span>](iscardcmd-put-nad.md)
-   [<span data-ttu-id="5eef9-132">**\_метод размещения P1**</span><span class="sxs-lookup"><span data-stu-id="5eef9-132">**put\_P1 Method**</span></span>](iscardcmd-put-p1.md)
-   [<span data-ttu-id="5eef9-133">**разместить \_ метод P2**</span><span class="sxs-lookup"><span data-stu-id="5eef9-133">**put\_P2 Method**</span></span>](iscardcmd-put-p2.md)
-   [<span data-ttu-id="5eef9-134">**\_метод реплистатус**</span><span class="sxs-lookup"><span data-stu-id="5eef9-134">**put\_ReplyStatus Method**</span></span>](iscardcmd-put-replystatus.md)

 

 



