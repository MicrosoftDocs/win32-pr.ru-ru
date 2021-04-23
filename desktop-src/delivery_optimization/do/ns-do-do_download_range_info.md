---
title: Структура DO_DOWNLOAD_RANGE_INFO
description: Определяет массив диапазонов байтов для скачивания из файла.
keywords:
- Структура DO_DOWNLOAD_RANGE_INFO
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE_INFO
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 01628ea29895012f60552e696b7f68854f426f8d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104412289"
---
# <a name="do_download_range_info-structure"></a><span data-ttu-id="b36b0-104">Структура DO_DOWNLOAD_RANGE_INFO</span><span class="sxs-lookup"><span data-stu-id="b36b0-104">DO_DOWNLOAD_RANGE_INFO structure</span></span>

<span data-ttu-id="b36b0-105">Структура **DO_DOWNLOAD_RANGE_INFO** определяет массив диапазонов байтов для скачивания из файла.</span><span class="sxs-lookup"><span data-stu-id="b36b0-105">The **DO_DOWNLOAD_RANGE_INFO** structure identifies an array of ranges of bytes to download from a file.</span></span> <span data-ttu-id="b36b0-106">Обычно он передается как необязательный аргумент функции **идодовнлоад:: Start** .</span><span class="sxs-lookup"><span data-stu-id="b36b0-106">It is typically passed as an optional argument to the **IDODownload::Start** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="b36b0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b36b0-107">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_RANGES_INFO
{
  UINT RangeCount;
  [size_is(RangeCount)] DO_DOWNLOAD_RANGE Ranges[];
} DO_DOWNLOAD_RANGES_INFO;
```

## <a name="members"></a><span data-ttu-id="b36b0-108">Члены</span><span class="sxs-lookup"><span data-stu-id="b36b0-108">Members</span></span>

`RangeCount`

<span data-ttu-id="b36b0-109">Число элементов в диапазонах.</span><span class="sxs-lookup"><span data-stu-id="b36b0-109">Number of elements in Ranges.</span></span>

`Ranges`

<span data-ttu-id="b36b0-110">Массив из одной или нескольких структур **DO_DOWNLOAD_RANGE** , указывающих диапазоны для загрузки.</span><span class="sxs-lookup"><span data-stu-id="b36b0-110">Array of one or more **DO_DOWNLOAD_RANGE** structures that specify the ranges to download.</span></span>

## <a name="requirements"></a><span data-ttu-id="b36b0-111">Требования</span><span class="sxs-lookup"><span data-stu-id="b36b0-111">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b36b0-112">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="b36b0-112">**Minimum supported client**</span></span> | <span data-ttu-id="b36b0-113">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="b36b0-113">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="b36b0-114">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="b36b0-114">**Minimum supported server**</span></span> | <span data-ttu-id="b36b0-115">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="b36b0-115">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="b36b0-116">**Header**</span><span class="sxs-lookup"><span data-stu-id="b36b0-116">**Header**</span></span> | <span data-ttu-id="b36b0-117">Do. h</span><span class="sxs-lookup"><span data-stu-id="b36b0-117">Do.h</span></span> |
