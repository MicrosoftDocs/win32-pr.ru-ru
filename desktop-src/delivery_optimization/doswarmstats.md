---
title: Структура Досвармстатс (Deliveryoptimization. h)
description: Содержит поля для загрузки и передачи статистики для файла.
ms.assetid: 66B2498A-38E0-44E4-96C1-F778BD9AA593
keywords:
- Структура Досвармстатс
topic_type:
- apiref
api_name:
- DOSwarmStats
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53d1702c25716ffe90c35727a258134311d5f427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710552"
---
# <a name="doswarmstats-structure"></a><span data-ttu-id="242f4-104">Структура Досвармстатс</span><span class="sxs-lookup"><span data-stu-id="242f4-104">DOSwarmStats structure</span></span>

<span data-ttu-id="242f4-105">Содержит поля для загрузки и передачи статистики для файла.</span><span class="sxs-lookup"><span data-stu-id="242f4-105">Contains fields for download and upload statistics for a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="242f4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="242f4-106">Syntax</span></span>


```C++
typedef struct _DOSwarmStats {
  LPWSTR       fileId;
  LPWSTR       sourceURL;
  UINT64       fileSize;
  UINT64       totalBytesDownloaded;
  UINT64       bytesFromLanPeers;
  UINT64       bytesFromGroupPeers;
  UINT64       bytesFromInternetPeers;
  UINT64       bytesFromHttp;
  UINT64       bytesFromDoinc;
  UINT64       bytesToLanPeers;
  UINT64       bytesToGroupPeers;
  UINT64       bytesToInternetPeers;
  UINT         httpConnectionCount;
  UINT         doincConnectionCount;
  UINT         lanConnectionCount;
  UINT         groupConnectionCount;
  UINT         internetConnectionCount;
  UINT         downloadDuration;
  DownloadMode downloadMode;
  SwarmStatus  status;
  BOOL         isBackground;
} DOSwarmStats;
```



## <a name="members"></a><span data-ttu-id="242f4-107">Члены</span><span class="sxs-lookup"><span data-stu-id="242f4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="242f4-108">**ИД**</span><span class="sxs-lookup"><span data-stu-id="242f4-108">**fileId**</span></span>
</dt> <dd>

<span data-ttu-id="242f4-109">Строка, завершающаяся нулем, которая была указана с помощью вызова **аддфилевисранжес** .</span><span class="sxs-lookup"><span data-stu-id="242f4-109">Null-terminated string that was specified with the **AddFileWithRanges** call.</span></span>

</dd> <dt>

<span data-ttu-id="242f4-110">**саурцеурл**</span><span class="sxs-lookup"><span data-stu-id="242f4-110">**sourceURL**</span></span>
</dt> <dd>

<span data-ttu-id="242f4-111">Строка, завершающаяся нулем, которая содержит имя файла на сервере (например, HTTPS:// &lt; Server &gt; / &lt; path &gt; /филе.екст).</span><span class="sxs-lookup"><span data-stu-id="242f4-111">Null-terminated string that contains the name of the file on the server (for example, https://&lt;server&gt;/&lt;path&gt;/file.ext).</span></span>

</dd> <dt>

<span data-ttu-id="242f4-112">**Размер файла**</span><span class="sxs-lookup"><span data-stu-id="242f4-112">**fileSize**</span></span>
</dt> <dd>

<span data-ttu-id="242f4-113">Размер файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="242f4-113">Size of the file in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="242f4-114">**тоталбитесдовнлоадед**</span><span class="sxs-lookup"><span data-stu-id="242f4-114">**totalBytesDownloaded**</span></span>
</dt> <dd>

<span data-ttu-id="242f4-115">Общее число переданных байтов.</span><span class="sxs-lookup"><span data-stu-id="242f4-115">Total number of bytes transferred.</span></span>

</dd> <dt>

<span data-ttu-id="242f4-116">**битесфромланпирс**</span><span class="sxs-lookup"><span data-stu-id="242f4-116">**bytesFromLanPeers**</span></span>
</dt> <dd>

<span data-ttu-id="242f4-117">Число байтов, передаваемых с одноранговых узлов.</span><span class="sxs-lookup"><span data-stu-id="242f4-117">Number of bytes transferred from LAN peers.</span></span>

</dd> <dt>

<span data-ttu-id="242f4-118">**битесфромграуппирс**</span><span class="sxs-lookup"><span data-stu-id="242f4-118">**bytesFromGroupPeers**</span></span>
</dt> <dd>

<span data-ttu-id="242f4-119">Число байтов, переданных с одноранговых узлов.</span><span class="sxs-lookup"><span data-stu-id="242f4-119">Number of bytes transferred from group peers.</span></span>

</dd> <dt>

<span data-ttu-id="242f4-120">**битесфроминтернетпирс**</span><span class="sxs-lookup"><span data-stu-id="242f4-120">**bytesFromInternetPeers**</span></span>
</dt> <dd>

<span data-ttu-id="242f4-121">Число байтов, передаваемых одноранговыми узлами Интернета.</span><span class="sxs-lookup"><span data-stu-id="242f4-121">Number of bytes transferred from Internet peers.</span></span>

</dd> <dt>

<span data-ttu-id="242f4-122">**битесфромхттп**</span><span class="sxs-lookup"><span data-stu-id="242f4-122">**bytesFromHttp**</span></span>
</dt> <dd>

<span data-ttu-id="242f4-123">Число байтов, передаваемых из HTTP.</span><span class="sxs-lookup"><span data-stu-id="242f4-123">Number of bytes transferred from http.</span></span>

</dd> <dt>

<span data-ttu-id="242f4-124">**битесфромдоинк**</span><span class="sxs-lookup"><span data-stu-id="242f4-124">**bytesFromDoinc**</span></span>
</dt> <dd>

<span data-ttu-id="242f4-125">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="242f4-125">For internal use only.</span></span>

</dd> <dt>

<span data-ttu-id="242f4-126">**битестоланпирс**</span><span class="sxs-lookup"><span data-stu-id="242f4-126">**bytesToLanPeers**</span></span>
</dt> <dd>

<span data-ttu-id="242f4-127">Число байтов, передаваемых одноранговым узлам локальной сети.</span><span class="sxs-lookup"><span data-stu-id="242f4-127">Number of bytes transferred to LAN peers.</span></span>

</dd> <dt>

<span data-ttu-id="242f4-128">**битестограуппирс**</span><span class="sxs-lookup"><span data-stu-id="242f4-128">**bytesToGroupPeers**</span></span>
</dt> <dd>

<span data-ttu-id="242f4-129">Число байтов, передаваемых одноранговым узлам группы.</span><span class="sxs-lookup"><span data-stu-id="242f4-129">Number of bytes transferred to group peers.</span></span>

</dd> <dt>

<span data-ttu-id="242f4-130">**битестоинтернетпирс**</span><span class="sxs-lookup"><span data-stu-id="242f4-130">**bytesToInternetPeers**</span></span>
</dt> <dd>

<span data-ttu-id="242f4-131">Число байтов, передаваемых одноранговым узлам Интернета.</span><span class="sxs-lookup"><span data-stu-id="242f4-131">Number of bytes transferred to Internet peers.</span></span>

</dd> <dt>

<span data-ttu-id="242f4-132">**хттпконнектионкаунт**</span><span class="sxs-lookup"><span data-stu-id="242f4-132">**httpConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="242f4-133">Число HTTP-соединений.</span><span class="sxs-lookup"><span data-stu-id="242f4-133">Count of http connections.</span></span>

</dd> <dt>

<span data-ttu-id="242f4-134">**доинкконнектионкаунт**</span><span class="sxs-lookup"><span data-stu-id="242f4-134">**doincConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="242f4-135">Только для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="242f4-135">For internal use only.</span></span>

</dd> <dt>

<span data-ttu-id="242f4-136">**ланконнектионкаунт**</span><span class="sxs-lookup"><span data-stu-id="242f4-136">**lanConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="242f4-137">Число подключений к локальной сети.</span><span class="sxs-lookup"><span data-stu-id="242f4-137">Count of LAN connections.</span></span>

</dd> <dt>

<span data-ttu-id="242f4-138">**граупконнектионкаунт**</span><span class="sxs-lookup"><span data-stu-id="242f4-138">**groupConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="242f4-139">Число подключений к группе.</span><span class="sxs-lookup"><span data-stu-id="242f4-139">Count of group connections.</span></span>

</dd> <dt>

<span data-ttu-id="242f4-140">**интернетконнектионкаунт**</span><span class="sxs-lookup"><span data-stu-id="242f4-140">**internetConnectionCount**</span></span>
</dt> <dd>

<span data-ttu-id="242f4-141">Число подключений к Интернету.</span><span class="sxs-lookup"><span data-stu-id="242f4-141">Count of Internet connections.</span></span>

</dd> <dt>

<span data-ttu-id="242f4-142">**довнлоаддуратион**</span><span class="sxs-lookup"><span data-stu-id="242f4-142">**downloadDuration**</span></span>
</dt> <dd>

<span data-ttu-id="242f4-143">Длительность обмена файлами в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="242f4-143">Duration of the file transfer in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="242f4-144">**downloadMode**</span><span class="sxs-lookup"><span data-stu-id="242f4-144">**downloadMode**</span></span>
</dt> <dd>

<span data-ttu-id="242f4-145">Используемом режиме загрузки см. в разделе [**DownloadMode**](downloadmode.md).</span><span class="sxs-lookup"><span data-stu-id="242f4-145">The download mode used, see [**DownloadMode**](downloadmode.md).</span></span>

</dd> <dt>

<span data-ttu-id="242f4-146">**status**</span><span class="sxs-lookup"><span data-stu-id="242f4-146">**status**</span></span>
</dt> <dd>

<span data-ttu-id="242f4-147">Состояние перемещения файла см. в разделе [**свармстатус**](swarmstatus.md).</span><span class="sxs-lookup"><span data-stu-id="242f4-147">The status of a file transfer, see [**SwarmStatus**](swarmstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="242f4-148">**на задний план**</span><span class="sxs-lookup"><span data-stu-id="242f4-148">**isBackground**</span></span>
</dt> <dd>

<span data-ttu-id="242f4-149">Значение true, если это перенос в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="242f4-149">True, if this is a background transfer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="242f4-150">Требования</span><span class="sxs-lookup"><span data-stu-id="242f4-150">Requirements</span></span>



| <span data-ttu-id="242f4-151">Требование</span><span class="sxs-lookup"><span data-stu-id="242f4-151">Requirement</span></span> | <span data-ttu-id="242f4-152">Значение</span><span class="sxs-lookup"><span data-stu-id="242f4-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="242f4-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="242f4-153">Minimum supported client</span></span><br/> | <span data-ttu-id="242f4-154">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="242f4-154">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="242f4-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="242f4-155">Minimum supported server</span></span><br/> | <span data-ttu-id="242f4-156">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="242f4-156">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="242f4-157">Header</span><span class="sxs-lookup"><span data-stu-id="242f4-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="242f4-158"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="242f4-158"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





