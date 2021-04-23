---
title: Ирдвтаскплугиннотифисинк DeleteSchedule, метод
description: Вызывается агентом задачи для удаления запланированной задачи.
ms.assetid: 67a9493e-367a-48c9-8f94-276d696406b7
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода DeleteSchedule
- Службы удаленных рабочих столов метода DeleteSchedule, интерфейс Ирдвтаскплугиннотифисинк
- Службы удаленных рабочих столов интерфейса Ирдвтаскплугиннотифисинк, метод DeleteSchedule
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.DeleteSchedule
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f00bcc740f87acb7f051decd5f2fc9b55ffbf642
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137558"
---
# <a name="irdvtaskpluginnotifysinkdeleteschedule-method"></a><span data-ttu-id="9dd0c-106">Ирдвтаскплугиннотифисинк: метод:D Елетесчедуле</span><span class="sxs-lookup"><span data-stu-id="9dd0c-106">IRDVTaskPluginNotifySink::DeleteSchedule method</span></span>

<span data-ttu-id="9dd0c-107">Вызывается агентом задачи для удаления запланированной задачи.</span><span class="sxs-lookup"><span data-stu-id="9dd0c-107">Called by the task agent to delete a scheduled task.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dd0c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9dd0c-108">Syntax</span></span>


```C++
HRESULT DeleteSchedule(
  [in] BSTR bstrIdentifier
);
```



## <a name="parameters"></a><span data-ttu-id="9dd0c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9dd0c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dd0c-110">*bstrIdentifier* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9dd0c-110">*bstrIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dd0c-111">Идентификатор запланированной задачи.</span><span class="sxs-lookup"><span data-stu-id="9dd0c-111">The identifier of the scheduled task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dd0c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9dd0c-112">Return value</span></span>

<span data-ttu-id="9dd0c-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="9dd0c-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9dd0c-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9dd0c-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dd0c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="9dd0c-115">Requirements</span></span>



| <span data-ttu-id="9dd0c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="9dd0c-116">Requirement</span></span> | <span data-ttu-id="9dd0c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9dd0c-117">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="9dd0c-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9dd0c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9dd0c-119">Windows 7 Корпоративная</span><span class="sxs-lookup"><span data-stu-id="9dd0c-119">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="9dd0c-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9dd0c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9dd0c-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9dd0c-121">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9dd0c-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9dd0c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dd0c-123">**ирдвтаскплугиннотифисинк**</span><span class="sxs-lookup"><span data-stu-id="9dd0c-123">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





