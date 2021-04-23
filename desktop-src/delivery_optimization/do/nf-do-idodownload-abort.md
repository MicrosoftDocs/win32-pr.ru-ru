---
title: 'Метод Идодовнлоад:: Abort'
description: Прерывает скачивание.
keywords:
- 'Метод Идодовнлоад:: Abort'
topic_type:
- apiref
api_name:
- IDODownload.Abort
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: babcd5ee00689ac103288074467980777f644668
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "105719086"
---
# <a name="idodownloadabort-method"></a><span data-ttu-id="146c8-104">Метод Идодовнлоад:: Abort</span><span class="sxs-lookup"><span data-stu-id="146c8-104">IDODownload::Abort method</span></span>

<span data-ttu-id="146c8-105">Прерывает скачивание.</span><span class="sxs-lookup"><span data-stu-id="146c8-105">Aborts the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="146c8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="146c8-106">Syntax</span></span>

```cpp
HRESULT Abort();
```

## <a name="return-value"></a><span data-ttu-id="146c8-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="146c8-107">Return Value</span></span>

<span data-ttu-id="146c8-108">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="146c8-108">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="146c8-109">В противном случае возвращается [](/windows/desktop/com/structure-of-com-error-codes) [код ошибки](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="146c8-109">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="146c8-110">Требования</span><span class="sxs-lookup"><span data-stu-id="146c8-110">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="146c8-111">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="146c8-111">**Minimum supported client**</span></span> | <span data-ttu-id="146c8-112">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="146c8-112">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="146c8-113">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="146c8-113">**Minimum supported server**</span></span> | <span data-ttu-id="146c8-114">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="146c8-114">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="146c8-115">**Header**</span><span class="sxs-lookup"><span data-stu-id="146c8-115">**Header**</span></span> | <span data-ttu-id="146c8-116">Do. h</span><span class="sxs-lookup"><span data-stu-id="146c8-116">Do.h</span></span> |
