---
title: 'Метод Идодовнлоадстатускаллбакк:: Онстатусчанже'
description: Вызывает реализацию этого метода при каждом изменении состояния загрузки.
keywords:
- 'Метод Идодовнлоадстатускаллбакк:: Онстатусчанже'
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback.OnStatusChange
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 9abf13969a6183f98102792b9bcf7a3329ca243d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/26/2019
ms.locfileid: "104069406"
---
# <a name="idodownloadstatuscallbackonstatuschange-method"></a><span data-ttu-id="11cf2-104">Метод Идодовнлоадстатускаллбакк:: Онстатусчанже</span><span class="sxs-lookup"><span data-stu-id="11cf2-104">IDODownloadStatusCallback::OnStatusChange method</span></span>

<span data-ttu-id="11cf2-105">Вызывает реализацию этого метода при каждом изменении состояния загрузки.</span><span class="sxs-lookup"><span data-stu-id="11cf2-105">DO calls your implementation of this method any time a download status has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="11cf2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11cf2-106">Syntax</span></span>

```cpp
HRESULT OnStatusChange(
  IDODownload *download,
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a><span data-ttu-id="11cf2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="11cf2-107">Parameters</span></span>

`download`

<span data-ttu-id="11cf2-108">Указатель на интерфейс **идодовнлоад** , состояние которого изменилось.</span><span class="sxs-lookup"><span data-stu-id="11cf2-108">An pointer to the **IDODownload** interface whose status changed.</span></span>

`status`

<span data-ttu-id="11cf2-109">Указатель на структуру **DO_DOWNLOAD_STATUS** , содержащую состояние загрузки.</span><span class="sxs-lookup"><span data-stu-id="11cf2-109">A pointer to a **DO_DOWNLOAD_STATUS** structure containing the download's status.</span></span>

## <a name="return-value"></a><span data-ttu-id="11cf2-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11cf2-110">Return Value</span></span>

<span data-ttu-id="11cf2-111">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="11cf2-111">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="11cf2-112">В противном случае возвращается [](/windows/desktop/com/structure-of-com-error-codes) [код ошибки](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="11cf2-112">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="11cf2-113">Требования</span><span class="sxs-lookup"><span data-stu-id="11cf2-113">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="11cf2-114">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="11cf2-114">**Minimum supported client**</span></span> | <span data-ttu-id="11cf2-115">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="11cf2-115">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="11cf2-116">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="11cf2-116">**Minimum supported server**</span></span> | <span data-ttu-id="11cf2-117">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="11cf2-117">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="11cf2-118">**Header**</span><span class="sxs-lookup"><span data-stu-id="11cf2-118">**Header**</span></span> | <span data-ttu-id="11cf2-119">Do. h</span><span class="sxs-lookup"><span data-stu-id="11cf2-119">Do.h</span></span> |
