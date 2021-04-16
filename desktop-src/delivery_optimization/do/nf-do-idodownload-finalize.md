---
title: 'Метод Идодовнлоад:: Finalize'
description: Завершает скачивание.
keywords:
- 'Метод Идодовнлоад:: Finalize'
topic_type:
- apiref
api_name:
- IDODownload.Finalize
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 6befc9a7e64fb0963d45257d68d6bb8d2ba7a2cb
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "105719085"
---
# <a name="idodownloadfinalize-method"></a><span data-ttu-id="2a45a-104">Метод Идодовнлоад:: Finalize</span><span class="sxs-lookup"><span data-stu-id="2a45a-104">IDODownload::Finalize method</span></span>

<span data-ttu-id="2a45a-105">Завершает скачивание.</span><span class="sxs-lookup"><span data-stu-id="2a45a-105">Finalizes the download.</span></span> <span data-ttu-id="2a45a-106">После завершения обновления скачивание невозможно возобновить, вызвав **Start**.</span><span class="sxs-lookup"><span data-stu-id="2a45a-106">Once finalized, a download cannot be resumed by calling **Start**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a45a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a45a-107">Syntax</span></span>

```cpp
HRESULT Finalize();
```

## <a name="return-value"></a><span data-ttu-id="2a45a-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a45a-108">Return Value</span></span>

<span data-ttu-id="2a45a-109">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="2a45a-109">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="2a45a-110">В противном случае возвращается [](/windows/desktop/com/structure-of-com-error-codes) [код ошибки](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="2a45a-110">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a45a-111">Требования</span><span class="sxs-lookup"><span data-stu-id="2a45a-111">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2a45a-112">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="2a45a-112">**Minimum supported client**</span></span> | <span data-ttu-id="2a45a-113">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="2a45a-113">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="2a45a-114">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="2a45a-114">**Minimum supported server**</span></span> | <span data-ttu-id="2a45a-115">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="2a45a-115">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="2a45a-116">**Header**</span><span class="sxs-lookup"><span data-stu-id="2a45a-116">**Header**</span></span> | <span data-ttu-id="2a45a-117">Do. h</span><span class="sxs-lookup"><span data-stu-id="2a45a-117">Do.h</span></span> |
