---
title: IUniversalOrchestrator::ScheduleWork
description: Вызывает универсальную Orchestrator для планирования работы
ms.topic: method
ms.date: 01/14/2021
ms.openlocfilehash: 456df8f975114f7bdf750a0449f3bd98efcc3b2e
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/21/2021
ms.locfileid: "105719756"
---
# <a name="iuniversalorchestratorschedulework-method"></a><span data-ttu-id="00cd4-103">Метод Иуниверсалорчестратор:: Счедулеворк</span><span class="sxs-lookup"><span data-stu-id="00cd4-103">IUniversalOrchestrator::ScheduleWork method</span></span>

> [!NOTE] 
> <span data-ttu-id="00cd4-104">Этот API принадлежит к универсальному API Orchestrator.</span><span class="sxs-lookup"><span data-stu-id="00cd4-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="00cd4-105">Позволяет клиентам сообщать о неработающем универсальном Orchestrator Management и предоставить двоичный файл, который будет вызываться универсальной Orchestrator для выполнения обновления позже.</span><span class="sxs-lookup"><span data-stu-id="00cd4-105">Allows clients to inform Universal Orchestrator that work is pending and provide a binary that will be called by Universal Orchestrator to perform the update work at a later time.</span></span>

<span data-ttu-id="00cd4-106">Двоичный ответ обратного вызова должен быть подписан действительным сертификатом Майкрософт, а вызывающий должен вызывать вызов Счедулеворк из контекста системы.</span><span class="sxs-lookup"><span data-stu-id="00cd4-106">The callback binary must be signed with a valid Microsoft certificate, and the caller must be invoking the ScheduleWork call from SYSTEM context.</span></span>

## <a name="syntax"></a><span data-ttu-id="00cd4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00cd4-107">Syntax</span></span>

```C++
HRESULT ScheduleWork(
  LPCWSTR callerIdentifier,
  LPCWSTR cmdLine
  LPCWSTR startArg,
  LPCWSTR pauseArg);
```

## <a name="parameters"></a><span data-ttu-id="00cd4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="00cd4-108">Parameters</span></span>

`callerIdentifier`

<span data-ttu-id="00cd4-109">Уникальная строка, идентифицирующая все вызовы от этого конкретного клиента.</span><span class="sxs-lookup"><span data-stu-id="00cd4-109">A unique string that identifies all calls from this specific client.</span></span>

`cmdLine`

<span data-ttu-id="00cd4-110">Полный путь к двоичному файлу обратного вызова, который будет вызываться универсальной Orchestrator для выполнения работы.</span><span class="sxs-lookup"><span data-stu-id="00cd4-110">The full path to the callback binary that will be invoked by Universal Orchestrator to perform work.</span></span>

`startArg`

<span data-ttu-id="00cd4-111">Параметры для передачи в двоичный файл обратного вызова, указывающие на запрос Start.</span><span class="sxs-lookup"><span data-stu-id="00cd4-111">Parameters to pass to the callback binary to indicate Start is requested.</span></span>

`pauseArg`

<span data-ttu-id="00cd4-112">*(необязательно)* Параметры для передачи в двоичный файл обратного вызова для указания запрошения приостановки.</span><span class="sxs-lookup"><span data-stu-id="00cd4-112">*(optional)* Parameters to pass to the callback binary to indicate Pause is requested.</span></span>

## <a name="return-value"></a><span data-ttu-id="00cd4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00cd4-113">Return value</span></span>
<span data-ttu-id="00cd4-114">Если этот метод завершается с ошибкой, возвращается **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="00cd4-114">If this method succeeds, it returns **S_OK**.</span></span>  <span data-ttu-id="00cd4-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="00cd4-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="00cd4-116">Требования</span><span class="sxs-lookup"><span data-stu-id="00cd4-116">Requirements</span></span>

| <span data-ttu-id="00cd4-117">Требование</span><span class="sxs-lookup"><span data-stu-id="00cd4-117">Requirement</span></span> | <span data-ttu-id="00cd4-118">Версия</span><span class="sxs-lookup"><span data-stu-id="00cd4-118">Version</span></span> |
|---|---|
| <span data-ttu-id="00cd4-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00cd4-119">Minimum supported client</span></span> | <span data-ttu-id="00cd4-120">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="00cd4-120">Windows 10 1903</span></span> |
|   |   |



 

 



