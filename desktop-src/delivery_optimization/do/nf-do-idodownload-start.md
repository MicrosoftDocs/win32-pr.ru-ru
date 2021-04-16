---
title: 'Метод Идодовнлоад:: Start'
description: Запускает или возобновляет загрузку.
keywords:
- 'Метод Идодовнлоад:: Start'
topic_type:
- apiref
api_name:
- IDODownload.Start
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0d05b0660008ae65350c6331428f641bc2126c18
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105720837"
---
# <a name="idodownloadstart-method"></a><span data-ttu-id="e0917-104">Метод Идодовнлоад:: Start</span><span class="sxs-lookup"><span data-stu-id="e0917-104">IDODownload::Start method</span></span>

<span data-ttu-id="e0917-105">Запускает или возобновляет загрузку, передавая необязательные диапазоны в виде указателя на структуру [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) .</span><span class="sxs-lookup"><span data-stu-id="e0917-105">Starts or resumes a download, passing optional ranges as a pointer to [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0917-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0917-106">Syntax</span></span>

```cpp
HRESULT Start(
  DO_DOWNLOAD_RANGES_INFO *ranges
);
```

## <a name="parameters"></a><span data-ttu-id="e0917-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0917-107">Parameters</span></span>

`ranges`

<span data-ttu-id="e0917-108">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="e0917-108">Optional.</span></span> <span data-ttu-id="e0917-109">Указатель на структуру [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) (чтобы скачать только определенные диапазоны файла).</span><span class="sxs-lookup"><span data-stu-id="e0917-109">A pointer to a [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) structure (to download only specific ranges of the file).</span></span> <span data-ttu-id="e0917-110">Передайте `nullptr` скачивание всего файла.</span><span class="sxs-lookup"><span data-stu-id="e0917-110">Pass `nullptr` to download the entire file.</span></span>

## <a name="return-value"></a><span data-ttu-id="e0917-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0917-111">Return Value</span></span>

<span data-ttu-id="e0917-112">Если функция завершается с ошибкой, она возвращает **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="e0917-112">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="e0917-113">В противном случае возвращается [](/windows/desktop/com/structure-of-com-error-codes) [код ошибки](/windows/desktop/com/com-error-codes-10)HRESULT.</span><span class="sxs-lookup"><span data-stu-id="e0917-113">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0917-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e0917-114">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e0917-115">**Минимальная версия клиента**</span><span class="sxs-lookup"><span data-stu-id="e0917-115">**Minimum supported client**</span></span> | <span data-ttu-id="e0917-116">Windows 10, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="e0917-116">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="e0917-117">**Минимальная версия сервера**</span><span class="sxs-lookup"><span data-stu-id="e0917-117">**Minimum supported server**</span></span> | <span data-ttu-id="e0917-118">Windows Server, \[ только приложения Win32 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="e0917-118">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="e0917-119">**Header**</span><span class="sxs-lookup"><span data-stu-id="e0917-119">**Header**</span></span> | <span data-ttu-id="e0917-120">Do. h</span><span class="sxs-lookup"><span data-stu-id="e0917-120">Do.h</span></span> |
