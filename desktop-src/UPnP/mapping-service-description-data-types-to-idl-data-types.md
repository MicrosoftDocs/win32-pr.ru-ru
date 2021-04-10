---
title: Сопоставление типов данных описания службы с типами данных IDL
description: В следующей таблице показано сопоставление типов данных XML, указанных в описании службы, с соответствующими типами данных, используемыми в IDL.
ms.assetid: eeb86177-8c3b-47f1-bbe1-f9aabd2dde76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b5fac697c41f54279ecde7436900434895ff23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068437"
---
# <a name="mapping-service-description-data-types-to-idl-data-types"></a><span data-ttu-id="ea660-103">Сопоставление типов данных описания службы с типами данных IDL</span><span class="sxs-lookup"><span data-stu-id="ea660-103">Mapping Service Description Data Types to IDL Data Types</span></span>

<span data-ttu-id="ea660-104">В следующей таблице показано сопоставление типов данных XML, указанных в описании службы, с соответствующими типами данных, используемыми в IDL.</span><span class="sxs-lookup"><span data-stu-id="ea660-104">The following table shows the mapping of XML data types specified in a service description to the corresponding data types used in IDL.</span></span>



| <span data-ttu-id="ea660-105">Тип данных XML</span><span class="sxs-lookup"><span data-stu-id="ea660-105">XML Data Type</span></span> | <span data-ttu-id="ea660-106">Тип данных IDL</span><span class="sxs-lookup"><span data-stu-id="ea660-106">IDL Data Type</span></span>  |
|---------------|----------------|
| <span data-ttu-id="ea660-107">bin.base64</span><span class="sxs-lookup"><span data-stu-id="ea660-107">bin.base64</span></span>    | <span data-ttu-id="ea660-108">SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="ea660-108">SAFEARRAY</span></span>      |
| <span data-ttu-id="ea660-109">bin.hex</span><span class="sxs-lookup"><span data-stu-id="ea660-109">bin.hex</span></span>       | <span data-ttu-id="ea660-110">SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="ea660-110">SAFEARRAY</span></span>      |
| <span data-ttu-id="ea660-111">Логическое</span><span class="sxs-lookup"><span data-stu-id="ea660-111">boolean</span></span>       | <span data-ttu-id="ea660-112">VARIANT \_ bool</span><span class="sxs-lookup"><span data-stu-id="ea660-112">VARIANT\_BOOL</span></span>  |
| <span data-ttu-id="ea660-113">char</span><span class="sxs-lookup"><span data-stu-id="ea660-113">char</span></span>          | <span data-ttu-id="ea660-114">WCHAR \_ t</span><span class="sxs-lookup"><span data-stu-id="ea660-114">wchar\_t</span></span>       |
| <span data-ttu-id="ea660-115">Дата</span><span class="sxs-lookup"><span data-stu-id="ea660-115">date</span></span>          | <span data-ttu-id="ea660-116">DATE</span><span class="sxs-lookup"><span data-stu-id="ea660-116">DATE</span></span>           |
| <span data-ttu-id="ea660-117">dateTime</span><span class="sxs-lookup"><span data-stu-id="ea660-117">dateTime</span></span>      | <span data-ttu-id="ea660-118">DATE</span><span class="sxs-lookup"><span data-stu-id="ea660-118">DATE</span></span>           |
| <span data-ttu-id="ea660-119">dateTime.tz</span><span class="sxs-lookup"><span data-stu-id="ea660-119">dateTime.tz</span></span>   | <span data-ttu-id="ea660-120">DATE</span><span class="sxs-lookup"><span data-stu-id="ea660-120">DATE</span></span>           |
| <span data-ttu-id="ea660-121">fixed.14.4</span><span class="sxs-lookup"><span data-stu-id="ea660-121">fixed.14.4</span></span>    | <span data-ttu-id="ea660-122">CY</span><span class="sxs-lookup"><span data-stu-id="ea660-122">CY</span></span>             |
| <span data-ttu-id="ea660-123">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ea660-123">float</span></span>         | <span data-ttu-id="ea660-124">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ea660-124">float</span></span>          |
| <span data-ttu-id="ea660-125">i1</span><span class="sxs-lookup"><span data-stu-id="ea660-125">i1</span></span>            | <span data-ttu-id="ea660-126">char</span><span class="sxs-lookup"><span data-stu-id="ea660-126">char</span></span>           |
| <span data-ttu-id="ea660-127">i2</span><span class="sxs-lookup"><span data-stu-id="ea660-127">i2</span></span>            | <span data-ttu-id="ea660-128">short</span><span class="sxs-lookup"><span data-stu-id="ea660-128">short</span></span>          |
| <span data-ttu-id="ea660-129">i4</span><span class="sxs-lookup"><span data-stu-id="ea660-129">i4</span></span>            | <span data-ttu-id="ea660-130">long</span><span class="sxs-lookup"><span data-stu-id="ea660-130">long</span></span>           |
| <span data-ttu-id="ea660-131">INT</span><span class="sxs-lookup"><span data-stu-id="ea660-131">int</span></span>           | <span data-ttu-id="ea660-132">long</span><span class="sxs-lookup"><span data-stu-id="ea660-132">long</span></span>           |
| <span data-ttu-id="ea660-133">number</span><span class="sxs-lookup"><span data-stu-id="ea660-133">number</span></span>        | <span data-ttu-id="ea660-134">BSTR</span><span class="sxs-lookup"><span data-stu-id="ea660-134">BSTR</span></span>           |
| <span data-ttu-id="ea660-135">r4</span><span class="sxs-lookup"><span data-stu-id="ea660-135">r4</span></span>            | <span data-ttu-id="ea660-136">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ea660-136">float</span></span>          |
| <span data-ttu-id="ea660-137">r8</span><span class="sxs-lookup"><span data-stu-id="ea660-137">r8</span></span>            | <span data-ttu-id="ea660-138">double</span><span class="sxs-lookup"><span data-stu-id="ea660-138">double</span></span>         |
| <span data-ttu-id="ea660-139">строка</span><span class="sxs-lookup"><span data-stu-id="ea660-139">string</span></span>        | <span data-ttu-id="ea660-140">BSTR</span><span class="sxs-lookup"><span data-stu-id="ea660-140">BSTR</span></span>           |
| <span data-ttu-id="ea660-141">time</span><span class="sxs-lookup"><span data-stu-id="ea660-141">time</span></span>          | <span data-ttu-id="ea660-142">DATE</span><span class="sxs-lookup"><span data-stu-id="ea660-142">DATE</span></span>           |
| <span data-ttu-id="ea660-143">time.tz</span><span class="sxs-lookup"><span data-stu-id="ea660-143">time.tz</span></span>       | <span data-ttu-id="ea660-144">DATE</span><span class="sxs-lookup"><span data-stu-id="ea660-144">DATE</span></span>           |
| <span data-ttu-id="ea660-145">ui1</span><span class="sxs-lookup"><span data-stu-id="ea660-145">ui1</span></span>           | <span data-ttu-id="ea660-146">unsigned char</span><span class="sxs-lookup"><span data-stu-id="ea660-146">unsigned char</span></span>  |
| <span data-ttu-id="ea660-147">ui2</span><span class="sxs-lookup"><span data-stu-id="ea660-147">ui2</span></span>           | <span data-ttu-id="ea660-148">unsigned short</span><span class="sxs-lookup"><span data-stu-id="ea660-148">unsigned short</span></span> |
| <span data-ttu-id="ea660-149">ui4</span><span class="sxs-lookup"><span data-stu-id="ea660-149">ui4</span></span>           | <span data-ttu-id="ea660-150">unsigned long</span><span class="sxs-lookup"><span data-stu-id="ea660-150">unsigned long</span></span>  |
| <span data-ttu-id="ea660-151">uri</span><span class="sxs-lookup"><span data-stu-id="ea660-151">uri</span></span>           | <span data-ttu-id="ea660-152">BSTR</span><span class="sxs-lookup"><span data-stu-id="ea660-152">BSTR</span></span>           |
| <span data-ttu-id="ea660-153">uuid</span><span class="sxs-lookup"><span data-stu-id="ea660-153">uuid</span></span>          | <span data-ttu-id="ea660-154">BSTR</span><span class="sxs-lookup"><span data-stu-id="ea660-154">BSTR</span></span>           |



 

 

 




