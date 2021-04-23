---
title: 'Метод Идодовнлоад:: with Status'
description: Получает указатель на структуру **DO_DOWNLOAD_STATUS** , отражающую текущее состояние загрузки.
keywords:
- 'Метод Идодовнлоад:: with Status'
topic_type:
- apiref
api_name:
- IDODownload.GetStatus
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 8b9b2603354bbb5345cf866ee0c94785a254952d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104412293"
---
# <a name="idodownloadgetstatus-method"></a><span data-ttu-id="faab8-104">Метод Идодовнлоад:: with Status</span><span class="sxs-lookup"><span data-stu-id="faab8-104">IDODownload::GetStatus method</span></span>

<span data-ttu-id="faab8-105">Получает указатель на структуру **DO_DOWNLOAD_STATUS** , отражающую текущее состояние загрузки.</span><span class="sxs-lookup"><span data-stu-id="faab8-105">Retrieves a pointer to a **DO_DOWNLOAD_STATUS** structure that reflects the current status of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="faab8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="faab8-106">Syntax</span></span>

```cpp
HRESULT GetStatus(
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a><span data-ttu-id="faab8-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="faab8-107">Parameters</span></span>

`status`

<span data-ttu-id="faab8-108">Указатель на структуру **DO_DOWNLOAD_STATUS** .</span><span class="sxs-lookup"><span data-stu-id="faab8-108">A pointer to a **DO_DOWNLOAD_STATUS** structure.</span></span>

## <a name="return-value"></a><span data-ttu-id="faab8-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="faab8-109">Return Value</span></span>

<span data-ttu-id="faab8-110">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="faab8-110">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="faab8-111">В противном случае возвращается [](/windows/desktop/com/structure-of-com-error-codes) [код ошибки](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="faab8-111">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="faab8-112">Требования</span><span class="sxs-lookup"><span data-stu-id="faab8-112">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="faab8-113">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="faab8-113">**Minimum supported client**</span></span> | <span data-ttu-id="faab8-114">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="faab8-114">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="faab8-115">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="faab8-115">**Minimum supported server**</span></span> | <span data-ttu-id="faab8-116">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="faab8-116">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="faab8-117">**Header**</span><span class="sxs-lookup"><span data-stu-id="faab8-117">**Header**</span></span> | <span data-ttu-id="faab8-118">Do. h</span><span class="sxs-lookup"><span data-stu-id="faab8-118">Do.h</span></span> |
