---
description: Предоставляет систему со сведениями о состоянии после завершения операции скрытого буфера обмена.
title: Функция Длпнотифипостсташклипбоард (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostStashClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: e549593acab6d74edf838a0f82952d8f3034bfcc
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495858"
---
# <a name="dlpnotifypoststashclipboard-function"></a><span data-ttu-id="39b66-103">Функция Длпнотифипостсташклипбоард</span><span class="sxs-lookup"><span data-stu-id="39b66-103">DlpNotifyPostStashClipboard function</span></span>

<span data-ttu-id="39b66-104">Предоставляет систему со сведениями о состоянии после завершения операции скрытого буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="39b66-104">Provides the system with status information after a stash clipboard operation is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="39b66-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39b66-105">Syntax</span></span>


```C++
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a><span data-ttu-id="39b66-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="39b66-106">Parameters</span></span>


<dl> <dt>

<span data-ttu-id="39b66-107">*Опстатус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39b66-107">*OpStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39b66-108">Указатель на структуру [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) , содержащую сведения о состоянии операции скрытого буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="39b66-108">A pointer to a [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) structure containing status information about the stash clipboard operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="39b66-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39b66-109">Return value</span></span>

<span data-ttu-id="39b66-110">Возвращает значение void.</span><span class="sxs-lookup"><span data-stu-id="39b66-110">Return void.</span></span>

## <a name="remarks"></a><span data-ttu-id="39b66-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="39b66-111">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="39b66-112">Требования</span><span class="sxs-lookup"><span data-stu-id="39b66-112">Requirements</span></span>



| <span data-ttu-id="39b66-113">Требование</span><span class="sxs-lookup"><span data-stu-id="39b66-113">Requirement</span></span>          |    <span data-ttu-id="39b66-114">Значение</span><span class="sxs-lookup"><span data-stu-id="39b66-114">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39b66-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39b66-115">Minimum supported client</span></span><br/> | <span data-ttu-id="39b66-116">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="39b66-116">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="39b66-117">DLL</span><span class="sxs-lookup"><span data-stu-id="39b66-117">DLL</span></span><br/>                      | <span data-ttu-id="39b66-118">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="39b66-118">EndpointDlp.dll</span></span> |