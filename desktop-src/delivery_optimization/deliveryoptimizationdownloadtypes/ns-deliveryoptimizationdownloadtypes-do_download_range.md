---
title: Структура DO_DOWNLOAD_RANGE
description: Определяет один диапазон байтов для скачивания из файла.
keywords:
- Структура DO_DOWNLOAD_RANGE
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0f328565c80350a05cbfb23f178ea3580586f326
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "105719089"
---
# <a name="do_download_range-structure"></a><span data-ttu-id="5e6dc-104">Структура DO_DOWNLOAD_RANGE</span><span class="sxs-lookup"><span data-stu-id="5e6dc-104">DO_DOWNLOAD_RANGE structure</span></span>

<span data-ttu-id="5e6dc-105">Структура **DO_DOWNLOAD_RANGE** определяет один диапазон байтов для загрузки из файла.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-105">The **DO_DOWNLOAD_RANGE** structure identifies a single range of bytes to download from a file.</span></span> <span data-ttu-id="5e6dc-106">Структура **DO_DOWNLOAD_RANGE** включается в структуру **DO_DOWNLOAD_RANGES_INFO** , чтобы предоставить массив диапазонов для загрузки.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-106">The **DO_DOWNLOAD_RANGE** structure is included within **DO_DOWNLOAD_RANGES_INFO** structure to provide an array of ranges to download.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e6dc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e6dc-107">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_RANGE
{
  UINT64 Offset;
  UINT64 Length;
} DO_DOWNLOAD_RANGE;
```

## <a name="members"></a><span data-ttu-id="5e6dc-108">Члены</span><span class="sxs-lookup"><span data-stu-id="5e6dc-108">Members</span></span>

`Offset`

<span data-ttu-id="5e6dc-109">Смещение от нуля до начала диапазона байтов для скачивания из файла.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-109">Zero-based offset to the beginning of the range of bytes to download from a file.</span></span>

`Length`

<span data-ttu-id="5e6dc-110">Длина диапазона в байтах.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-110">The length of the range, in bytes.</span></span> <span data-ttu-id="5e6dc-111">Не указывайте нулевую длину в байтах.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-111">Do not specify a zero-byte length.</span></span> <span data-ttu-id="5e6dc-112">Чтобы указать, что диапазон расширяется до конца файла, укажите **DO_LENGTH_TO_EOF**.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-112">To indicate that the range extends to the end of the file, specify **DO_LENGTH_TO_EOF**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e6dc-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5e6dc-113">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5e6dc-114">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="5e6dc-114">**Minimum supported client**</span></span> | <span data-ttu-id="5e6dc-115">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="5e6dc-115">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="5e6dc-116">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="5e6dc-116">**Minimum supported server**</span></span> | <span data-ttu-id="5e6dc-117">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="5e6dc-117">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="5e6dc-118">**Header**</span><span class="sxs-lookup"><span data-stu-id="5e6dc-118">**Header**</span></span> | <span data-ttu-id="5e6dc-119">Деливерйоптимизатиондовнлоадтипес. h</span><span class="sxs-lookup"><span data-stu-id="5e6dc-119">DeliveryOptimizationDownloadTypes.h</span></span> |
