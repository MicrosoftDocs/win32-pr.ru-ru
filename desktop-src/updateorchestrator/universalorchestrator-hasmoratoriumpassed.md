---
title: IUniversalOrchestrator::HasMoratoriumPassed
description: Запрашивает универсальную Orchestrator, чтобы определить, был ли превышен период после OOBE.
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 2ed354d365b795a0c959396e6b26d6bc73baad97
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "105719754"
---
# <a name="iuniversalorchestratorhasmoratoriumpassed-method"></a><span data-ttu-id="737d7-103">Метод Иуниверсалорчестратор:: Хасмораториумпассед</span><span class="sxs-lookup"><span data-stu-id="737d7-103">IUniversalOrchestrator::HasMoratoriumPassed method</span></span>

> [!NOTE] 
> <span data-ttu-id="737d7-104">Этот API принадлежит к универсальному API Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="737d7-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="737d7-105">Позволяет клиентам определить, работает ли Универсальная схема Orchestrator сразу же после завершения работы нового устройства, что ограничивает количество попыток, позволяющих уменьшить число прерываний работы пользователей.</span><span class="sxs-lookup"><span data-stu-id="737d7-105">Allows clients to determine if Universal Orchestrator is operating immediately after the new device Out of Box Experience, which limits work attempts to minimize user interruption.</span></span> 

## <a name="syntax"></a><span data-ttu-id="737d7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="737d7-106">Syntax</span></span>

```C++
HRESULT HasMoratoriumPassed(
  LPCWSTR callerIdentifier,
  BOOL*   moratoriumPassed);
```

## <a name="parameters"></a><span data-ttu-id="737d7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="737d7-107">Parameters</span></span>

`callerIdentifier`

<span data-ttu-id="737d7-108">Уникальная строка, идентифицирующая все вызовы от этого конкретного клиента.</span><span class="sxs-lookup"><span data-stu-id="737d7-108">A unique string that identifies all calls from this specific client.</span></span>

`hasMoratoriumPassed`

<span data-ttu-id="737d7-109">Выходной параметр, хранящий результат запроса.</span><span class="sxs-lookup"><span data-stu-id="737d7-109">Output parameter that stores the result of the query.</span></span>

## <a name="return-value"></a><span data-ttu-id="737d7-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="737d7-110">Return value</span></span>
<span data-ttu-id="737d7-111">Если этот метод завершается с ошибкой, возвращается **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="737d7-111">If this method succeeds, it returns **S_OK**.</span></span>  <span data-ttu-id="737d7-112">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="737d7-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="737d7-113">Требования</span><span class="sxs-lookup"><span data-stu-id="737d7-113">Requirements</span></span>

| <span data-ttu-id="737d7-114">Требование</span><span class="sxs-lookup"><span data-stu-id="737d7-114">Requirement</span></span> | <span data-ttu-id="737d7-115">Версия</span><span class="sxs-lookup"><span data-stu-id="737d7-115">Version</span></span> |
|---|---|
| <span data-ttu-id="737d7-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="737d7-116">Minimum supported client</span></span> | <span data-ttu-id="737d7-117">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="737d7-117">Windows 10 1903</span></span> |
|   |   |



 

 



