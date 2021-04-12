---
title: Метод Terminate Ирдвтаскплугин
description: Вызывается при завершении работы агента задачи.
ms.assetid: b693a318-1da7-4207-8046-a62b7ccca471
ms.tgt_platform: multiple
keywords:
- Метод Terminate службы удаленных рабочих столов
- Метод Terminate службы удаленных рабочих столов, интерфейс Ирдвтаскплугин
- Интерфейс Ирдвтаскплугин службы удаленных рабочих столов, метод Terminate
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Terminate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 178f0a7c054169d972acb6b60a9cc80578fd13e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415748"
---
# <a name="irdvtaskpluginterminate-method"></a><span data-ttu-id="35fbe-106">Метод Ирдвтаскплугин:: Terminate</span><span class="sxs-lookup"><span data-stu-id="35fbe-106">IRDVTaskPlugin::Terminate method</span></span>

<span data-ttu-id="35fbe-107">Вызывается при завершении работы агента задачи.</span><span class="sxs-lookup"><span data-stu-id="35fbe-107">Called when the task agent is being shut down.</span></span>

## <a name="syntax"></a><span data-ttu-id="35fbe-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35fbe-108">Syntax</span></span>


```C++
HRESULT Terminate(
  [in] HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="35fbe-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="35fbe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35fbe-110">*HR* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="35fbe-110">*hr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35fbe-111">Указывает, находится ли завершение работы из-за нормального завершения работы или сбоя.</span><span class="sxs-lookup"><span data-stu-id="35fbe-111">Indicates whether the shut down is due to a normal shut down or a failure.</span></span> <span data-ttu-id="35fbe-112">Если завершение работы является нормальным, оно содержит **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="35fbe-112">If the shut down is normal, this contains **S\_OK**.</span></span> <span data-ttu-id="35fbe-113">В противном случае он содержит код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="35fbe-113">Otherwise, it contains an **HRESULT** error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35fbe-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35fbe-114">Return value</span></span>

<span data-ttu-id="35fbe-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="35fbe-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="35fbe-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="35fbe-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="35fbe-117">Требования</span><span class="sxs-lookup"><span data-stu-id="35fbe-117">Requirements</span></span>



| <span data-ttu-id="35fbe-118">Требование</span><span class="sxs-lookup"><span data-stu-id="35fbe-118">Requirement</span></span> | <span data-ttu-id="35fbe-119">Значение</span><span class="sxs-lookup"><span data-stu-id="35fbe-119">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="35fbe-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35fbe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="35fbe-121">Windows 7 Корпоративная</span><span class="sxs-lookup"><span data-stu-id="35fbe-121">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="35fbe-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35fbe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="35fbe-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="35fbe-123">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="35fbe-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35fbe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35fbe-125">**ирдвтаскплугин**</span><span class="sxs-lookup"><span data-stu-id="35fbe-125">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





