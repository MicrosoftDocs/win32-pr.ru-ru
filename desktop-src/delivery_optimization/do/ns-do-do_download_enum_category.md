---
title: Структура DO_DOWNLOAD_ENUM_CATEGORY
description: 'Используется **идоманажер:: енумдовнлоадс** для фильтрации перечисления Downloads по значению конкретного свойства.'
keywords:
- Структура DO_DOWNLOAD_ENUM_CATEGORY
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_ENUM_CATEGORY
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a78c94cd9d8854453517976300e12a031f65b8cb
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "105719081"
---
# <a name="do_download_enum_category-structure"></a><span data-ttu-id="d6615-104">Структура DO_DOWNLOAD_ENUM_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="d6615-104">DO_DOWNLOAD_ENUM_CATEGORY structure</span></span>

<span data-ttu-id="d6615-105">Структура **DO_DOWNLOAD_ENUM_CATEGORY** используется **Идоманажер:: енумдовнлоадс** для фильтрации перечисления Downloads по значению конкретного свойства.</span><span class="sxs-lookup"><span data-stu-id="d6615-105">The **DO_DOWNLOAD_ENUM_CATEGORY** structure is used by **IDOManager::EnumDownloads** to filter the downloads enumeration by the specific property's value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6615-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6615-106">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_ENUM_CATEGORY
{
  DODownloadProperty Property;
  LPCWSTR Value;
} DO_DOWNLOAD_ENUM_CATEGORY;
```

## <a name="members"></a><span data-ttu-id="d6615-107">Члены</span><span class="sxs-lookup"><span data-stu-id="d6615-107">Members</span></span>

`Property`

<span data-ttu-id="d6615-108">Имя свойства, используемого для перечисления загрузки.</span><span class="sxs-lookup"><span data-stu-id="d6615-108">The property name to be used for the download enumeration.</span></span> <span data-ttu-id="d6615-109">Эти свойства поддерживаются в целях перечисления.</span><span class="sxs-lookup"><span data-stu-id="d6615-109">These properties are supported for enumeration purposes.</span></span>
- <span data-ttu-id="d6615-110">**DODownloadProperty_Id**</span><span class="sxs-lookup"><span data-stu-id="d6615-110">**DODownloadProperty_Id**</span></span>
- <span data-ttu-id="d6615-111">**DODownloadProperty_Uri**</span><span class="sxs-lookup"><span data-stu-id="d6615-111">**DODownloadProperty_Uri**</span></span>
- <span data-ttu-id="d6615-112">**DODownloadProperty_ContentId**</span><span class="sxs-lookup"><span data-stu-id="d6615-112">**DODownloadProperty_ContentId**</span></span>
- <span data-ttu-id="d6615-113">**DODownloadProperty_DisplayName**</span><span class="sxs-lookup"><span data-stu-id="d6615-113">**DODownloadProperty_DisplayName**</span></span>
- <span data-ttu-id="d6615-114">**DODownloadProperty_LocalPath**</span><span class="sxs-lookup"><span data-stu-id="d6615-114">**DODownloadProperty_LocalPath**</span></span>

`Value`

<span data-ttu-id="d6615-115">Значение свойства.</span><span class="sxs-lookup"><span data-stu-id="d6615-115">The property's value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6615-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d6615-116">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d6615-117">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="d6615-117">**Minimum supported client**</span></span> | <span data-ttu-id="d6615-118">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="d6615-118">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="d6615-119">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="d6615-119">**Minimum supported server**</span></span> | <span data-ttu-id="d6615-120">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="d6615-120">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="d6615-121">**Header**</span><span class="sxs-lookup"><span data-stu-id="d6615-121">**Header**</span></span> | <span data-ttu-id="d6615-122">Do. h</span><span class="sxs-lookup"><span data-stu-id="d6615-122">Do.h</span></span> |
