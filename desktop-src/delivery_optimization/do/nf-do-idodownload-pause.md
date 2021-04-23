---
title: 'Идодовнлоад: метод:P Аусе'
description: Приостанавливает скачивание.
keywords:
- 'Идодовнлоад: метод:P Аусе'
topic_type:
- apiref
api_name:
- IDODownload.Pause
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a7239253238b0d9b7e606329b10f05b3645b7e16
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104133366"
---
# <a name="idodownloadpause-method"></a><span data-ttu-id="0b8c1-104">Идодовнлоад: метод:P Аусе</span><span class="sxs-lookup"><span data-stu-id="0b8c1-104">IDODownload::Pause method</span></span>

<span data-ttu-id="0b8c1-105">Приостанавливает скачивание.</span><span class="sxs-lookup"><span data-stu-id="0b8c1-105">Pauses the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b8c1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b8c1-106">Syntax</span></span>

```cpp
HRESULT Pause();
```

## <a name="return-value"></a><span data-ttu-id="0b8c1-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0b8c1-107">Return Value</span></span>

<span data-ttu-id="0b8c1-108">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="0b8c1-108">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="0b8c1-109">В противном случае возвращается [](/windows/desktop/com/structure-of-com-error-codes) [код ошибки](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="0b8c1-109">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b8c1-110">Требования</span><span class="sxs-lookup"><span data-stu-id="0b8c1-110">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="0b8c1-111">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="0b8c1-111">**Minimum supported client**</span></span> | <span data-ttu-id="0b8c1-112">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="0b8c1-112">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="0b8c1-113">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="0b8c1-113">**Minimum supported server**</span></span> | <span data-ttu-id="0b8c1-114">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="0b8c1-114">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="0b8c1-115">**Header**</span><span class="sxs-lookup"><span data-stu-id="0b8c1-115">**Header**</span></span> | <span data-ttu-id="0b8c1-116">Do. h</span><span class="sxs-lookup"><span data-stu-id="0b8c1-116">Do.h</span></span> |
