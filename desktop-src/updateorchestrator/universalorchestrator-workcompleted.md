---
title: IUniversalOrchestrator::WorkCompleted
description: Вызывает универсальную Orchestrator для обозначения завершения работы
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 8d4a08e7f021811e59a182a8b726397476b78433
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "105719757"
---
# <a name="iuniversalorchestratorworkcompleted-method"></a><span data-ttu-id="ffe04-103">Метод Иуниверсалорчестратор:: Ворккомплетед</span><span class="sxs-lookup"><span data-stu-id="ffe04-103">IUniversalOrchestrator::WorkCompleted method</span></span>

> [!NOTE] 
> <span data-ttu-id="ffe04-104">Этот API принадлежит к универсальному API Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="ffe04-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="ffe04-105">Позволяет клиентам информировать универсальную Orchestrator о том, что ранее запланированная работа была выполнена, и закончить обратные вызовы, чтобы выполнить работу до следующего успешного вызова Счедулеворк.</span><span class="sxs-lookup"><span data-stu-id="ffe04-105">Allows clients to inform Universal Orchestrator that the previously scheduled work has been completed and stop callbacks to perform work until the next successful ScheduleWork call.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffe04-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffe04-106">Syntax</span></span>

```C++
HRESULT WorkCompleted(
  LPCWSTR callerIdentifier,
  BOOL    workCompleted);
```

## <a name="parameters"></a><span data-ttu-id="ffe04-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ffe04-107">Parameters</span></span>

`callerIdentifier`

<span data-ttu-id="ffe04-108">Уникальная строка, идентифицирующая все вызовы от этого конкретного клиента.</span><span class="sxs-lookup"><span data-stu-id="ffe04-108">A unique string that identifies all calls from this specific client.</span></span>

`workCompleted`

<span data-ttu-id="ffe04-109">**Значение true** , если работа успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="ffe04-109">**TRUE** if the work successfully completed.</span></span> <span data-ttu-id="ffe04-110">В противном случае **значение false** , если попытка работы завершилась неудачей, и ее следует повторить в будущем.</span><span class="sxs-lookup"><span data-stu-id="ffe04-110">Otherwise, **FALSE** if the work attempt failed and should be retried in the future.</span></span> 

## <a name="return-value"></a><span data-ttu-id="ffe04-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ffe04-111">Return value</span></span>
<span data-ttu-id="ffe04-112">Если этот метод завершается с ошибкой, возвращается **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="ffe04-112">If this method succeeds, it returns **S_OK**.</span></span>  <span data-ttu-id="ffe04-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ffe04-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffe04-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ffe04-114">Requirements</span></span>

| <span data-ttu-id="ffe04-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ffe04-115">Requirement</span></span> | <span data-ttu-id="ffe04-116">Версия</span><span class="sxs-lookup"><span data-stu-id="ffe04-116">Version</span></span> |
|---|---|
| <span data-ttu-id="ffe04-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ffe04-117">Minimum supported client</span></span> | <span data-ttu-id="ffe04-118">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="ffe04-118">Windows 10 1903</span></span> |
|   |   |



 

 



