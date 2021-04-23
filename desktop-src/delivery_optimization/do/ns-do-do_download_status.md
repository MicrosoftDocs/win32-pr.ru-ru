---
title: Структура DO_DOWNLOAD_STATUS
description: Используется для получения состояния определенного скачивания.
keywords:
- Структура DO_DOWNLOAD_STATUS
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_STATUS
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 5e113bb4866ef1033886dbb1579d21aa296d0e5e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "105719079"
---
# <a name="do_download_status-structure"></a><span data-ttu-id="c1c14-104">Структура DO_DOWNLOAD_STATUS</span><span class="sxs-lookup"><span data-stu-id="c1c14-104">DO_DOWNLOAD_STATUS structure</span></span>

<span data-ttu-id="c1c14-105">Структура **DO_DOWNLOAD_STATUS** используется для получения состояния определенного скачивания.</span><span class="sxs-lookup"><span data-stu-id="c1c14-105">The **DO_DOWNLOAD_STATUS** structure is used to obtain the status of a specific download.</span></span> <span data-ttu-id="c1c14-106">Он получается путем вызова функции **идодовнлоад::-Status** .</span><span class="sxs-lookup"><span data-stu-id="c1c14-106">It is obtained by calling the **IDODownload::GetStatus** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1c14-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1c14-107">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_STATUS
{
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  DODownloadState State;
  HRESULT Error;
  HRESULT ExtendedError;
} DO_DOWNLOAD_STATUS;
```

## <a name="members"></a><span data-ttu-id="c1c14-108">Члены</span><span class="sxs-lookup"><span data-stu-id="c1c14-108">Members</span></span>

`BytesTotal`

<span data-ttu-id="c1c14-109">Общее число байтов для скачивания.</span><span class="sxs-lookup"><span data-stu-id="c1c14-109">The total number of bytes to download.</span></span>

`BytesTransferred`

<span data-ttu-id="c1c14-110">Число уже скачанных байтов.</span><span class="sxs-lookup"><span data-stu-id="c1c14-110">The number of bytes that have already been downloaded.</span></span>

`State`

<span data-ttu-id="c1c14-111">Текущее состояние загрузки в соответствии с определением перечисления **додовнлоадстате** .</span><span class="sxs-lookup"><span data-stu-id="c1c14-111">The current download state as defined by the **DODownloadState** enumeration.</span></span>

`Error`

<span data-ttu-id="c1c14-112">Сведения об ошибке (если они существуют), связанные с текущей загрузкой.</span><span class="sxs-lookup"><span data-stu-id="c1c14-112">The error information (if it exists) that is associated with the current download.</span></span>

`ExtendedError`

<span data-ttu-id="c1c14-113">Расширенные сведения об ошибке (если они существуют), связанные с текущей загрузкой.</span><span class="sxs-lookup"><span data-stu-id="c1c14-113">The extended error information (if it exists) that is associated with the current download.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1c14-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c1c14-114">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c1c14-115">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="c1c14-115">**Minimum supported client**</span></span> | <span data-ttu-id="c1c14-116">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="c1c14-116">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="c1c14-117">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="c1c14-117">**Minimum supported server**</span></span> | <span data-ttu-id="c1c14-118">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="c1c14-118">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="c1c14-119">**Header**</span><span class="sxs-lookup"><span data-stu-id="c1c14-119">**Header**</span></span> | <span data-ttu-id="c1c14-120">Do. h</span><span class="sxs-lookup"><span data-stu-id="c1c14-120">Do.h</span></span> |
