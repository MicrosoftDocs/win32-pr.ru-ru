---
title: 'Метод Идоманажер:: Креатедовнлоад'
description: Создает новую загрузку.
keywords:
- 'Метод Идоманажер:: Креатедовнлоад'
topic_type:
- apiref
api_name:
- IDOManager.CreateDownload
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: b79bf0a1c5602fafea113585dfe6e8ca5b01057c
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104412291"
---
# <a name="idomanagercreatedownload-method"></a><span data-ttu-id="fb117-104">Метод Идоманажер:: Креатедовнлоад</span><span class="sxs-lookup"><span data-stu-id="fb117-104">IDOManager::CreateDownload method</span></span>

<span data-ttu-id="fb117-105">Создает новую загрузку.</span><span class="sxs-lookup"><span data-stu-id="fb117-105">Creates a new download.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb117-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb117-106">Syntax</span></span>

```cpp
HRESULT CreateDownload(
  IDODownload **download
);
```

## <a name="parameters"></a><span data-ttu-id="fb117-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb117-107">Parameters</span></span>

`download`

<span data-ttu-id="fb117-108">Адрес указателя интерфейса **идодовнлоад** .</span><span class="sxs-lookup"><span data-stu-id="fb117-108">The address of an **IDODownload** interface pointer.</span></span>

## <a name="return-value"></a><span data-ttu-id="fb117-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb117-109">Return Value</span></span>

<span data-ttu-id="fb117-110">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="fb117-110">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="fb117-111">В противном случае возвращается [](/windows/desktop/com/structure-of-com-error-codes) [код ошибки](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="fb117-111">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb117-112">Требования</span><span class="sxs-lookup"><span data-stu-id="fb117-112">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fb117-113">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="fb117-113">**Minimum supported client**</span></span> | <span data-ttu-id="fb117-114">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="fb117-114">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="fb117-115">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="fb117-115">**Minimum supported server**</span></span> | <span data-ttu-id="fb117-116">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="fb117-116">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="fb117-117">**Header**</span><span class="sxs-lookup"><span data-stu-id="fb117-117">**Header**</span></span> | <span data-ttu-id="fb117-118">Do. h</span><span class="sxs-lookup"><span data-stu-id="fb117-118">Do.h</span></span> |
