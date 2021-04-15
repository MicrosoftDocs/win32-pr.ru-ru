---
title: Структура MPRESOURCE_STATS (Мпклиент. h)
description: Статистика, связанная с ресурсами.
ms.assetid: D1DC4BC9-911D-448C-A421-11D2F51F0A61
keywords:
- MPRESOURCE_STATS структуры устаревшие функции среды Windows
- Функции PMPRESOURCE_STATS указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPRESOURCE_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afbe1ce6734aabd1093f7acd886af757c51ed83e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491550"
---
# <a name="mpresource_stats-structure"></a><span data-ttu-id="d5e09-105">\_Структура статистики мпресаурце</span><span class="sxs-lookup"><span data-stu-id="d5e09-105">MPRESOURCE\_STATS structure</span></span>

<span data-ttu-id="d5e09-106">Статистика, связанная с ресурсами.</span><span class="sxs-lookup"><span data-stu-id="d5e09-106">Resource-related statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5e09-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5e09-107">Syntax</span></span>


```C++
typedef struct tagMPRESOURCE_STATS {
  DWORD  PPMProgress;
  UINT64 ProcessCount;
  UINT64 FileCount;
  UINT64 FileBytesCount;
  UINT64 RegKeyCount;
  UINT64 Reserved[4];
} MPRESOURCE_STATS, *PMPRESOURCE_STATS;
```



## <a name="members"></a><span data-ttu-id="d5e09-108">Члены</span><span class="sxs-lookup"><span data-stu-id="d5e09-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d5e09-109">**ппмпрогресс**</span><span class="sxs-lookup"><span data-stu-id="d5e09-109">**PPMProgress**</span></span>
</dt> <dd>

<span data-ttu-id="d5e09-110">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d5e09-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="d5e09-111">Приблизительный ход выполнения проверки в ppm (штук в миллион).</span><span class="sxs-lookup"><span data-stu-id="d5e09-111">Approximate progress for scan in ppm (parts per million).</span></span> <span data-ttu-id="d5e09-112">Задайте значение **мппрогресс \_ недопустимо** , если сведения о ходе выполнения недоступны.</span><span class="sxs-lookup"><span data-stu-id="d5e09-112">Set to **MPPROGRESS\_INVALID** if progress information is not available.</span></span>

</dd> <dt>

<span data-ttu-id="d5e09-113">**процесскаунт**</span><span class="sxs-lookup"><span data-stu-id="d5e09-113">**ProcessCount**</span></span>
</dt> <dd>

<span data-ttu-id="d5e09-114">Тип: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="d5e09-114">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="d5e09-115">Число проверенных процессов.</span><span class="sxs-lookup"><span data-stu-id="d5e09-115">Number of processes scanned.</span></span>

</dd> <dt>

<span data-ttu-id="d5e09-116">**FileCount**</span><span class="sxs-lookup"><span data-stu-id="d5e09-116">**FileCount**</span></span>
</dt> <dd>

<span data-ttu-id="d5e09-117">Тип: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="d5e09-117">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="d5e09-118">Число проверенных файлов.</span><span class="sxs-lookup"><span data-stu-id="d5e09-118">Number of files scanned.</span></span>

</dd> <dt>

<span data-ttu-id="d5e09-119">**филебитескаунт**</span><span class="sxs-lookup"><span data-stu-id="d5e09-119">**FileBytesCount**</span></span>
</dt> <dd>

<span data-ttu-id="d5e09-120">Тип: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="d5e09-120">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="d5e09-121">Число байтов, проверенных на наличие файлов.</span><span class="sxs-lookup"><span data-stu-id="d5e09-121">Number of bytes scanned for files.</span></span>

</dd> <dt>

<span data-ttu-id="d5e09-122">**регкэйкаунт**</span><span class="sxs-lookup"><span data-stu-id="d5e09-122">**RegKeyCount**</span></span>
</dt> <dd>

<span data-ttu-id="d5e09-123">Тип: **UINT64**</span><span class="sxs-lookup"><span data-stu-id="d5e09-123">Type: **UINT64**</span></span>

</dd> <dd>

<span data-ttu-id="d5e09-124">Число сканированных Регкэйс.</span><span class="sxs-lookup"><span data-stu-id="d5e09-124">Number of RegKeys scanned.</span></span>

</dd> <dt>

<span data-ttu-id="d5e09-125">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="d5e09-125">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="d5e09-126">Тип: **UINT64 \[ 4 \]**</span><span class="sxs-lookup"><span data-stu-id="d5e09-126">Type: **UINT64\[4\]**</span></span>

</dd> <dd>

<span data-ttu-id="d5e09-127">Поля, зарезервированные для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="d5e09-127">Fields reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5e09-128">Требования</span><span class="sxs-lookup"><span data-stu-id="d5e09-128">Requirements</span></span>



| <span data-ttu-id="d5e09-129">Требование</span><span class="sxs-lookup"><span data-stu-id="d5e09-129">Requirement</span></span> | <span data-ttu-id="d5e09-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d5e09-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5e09-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d5e09-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d5e09-132">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d5e09-132">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d5e09-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d5e09-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d5e09-134">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d5e09-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5e09-135">Header</span><span class="sxs-lookup"><span data-stu-id="d5e09-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5e09-136"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5e09-136"><dt>MpClient.h</dt></span></span> </dl> |



 

 





