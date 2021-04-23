---
title: Ирдвтаскплугиннотифисинк Онтаскстатечанже, метод
description: Используется для уведомления агента активации о том, что состояние задачи изменилось.
ms.assetid: 3021ea7a-2627-48d1-8df5-c40e7a9b51c5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онтаскстатечанже
- Службы удаленных рабочих столов метода Онтаскстатечанже, интерфейс Ирдвтаскплугиннотифисинк
- Службы удаленных рабочих столов интерфейса Ирдвтаскплугиннотифисинк, метод Онтаскстатечанже
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTaskStateChange
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3e3acf1a2d47b1721ef90554f7a11714c02e6df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672863"
---
# <a name="irdvtaskpluginnotifysinkontaskstatechange-method"></a><span data-ttu-id="07716-106">Метод Ирдвтаскплугиннотифисинк:: Онтаскстатечанже</span><span class="sxs-lookup"><span data-stu-id="07716-106">IRDVTaskPluginNotifySink::OnTaskStateChange method</span></span>

<span data-ttu-id="07716-107">Используется для уведомления агента активации о том, что состояние задачи изменилось.</span><span class="sxs-lookup"><span data-stu-id="07716-107">Used to notify the trigger agent that the state of a task has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="07716-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07716-108">Syntax</span></span>


```C++
HRESULT OnTaskStateChange(
  [in] BSTR            bstrIdentifier,
  [in] RDV_TASK_STATUS status
);
```



## <a name="parameters"></a><span data-ttu-id="07716-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="07716-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07716-110">*bstrIdentifier* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="07716-110">*bstrIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07716-111">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="07716-111">Type: **BSTR**</span></span>

<span data-ttu-id="07716-112">Идентификатор задачи.</span><span class="sxs-lookup"><span data-stu-id="07716-112">The identifier of the task.</span></span> <span data-ttu-id="07716-113">Это идентификатор, передаваемый методу [**StartTask**](irdvtaskplugin-starttask.md) .</span><span class="sxs-lookup"><span data-stu-id="07716-113">This is the identifier passed to the [**StartTask**](irdvtaskplugin-starttask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="07716-114">*состояние* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="07716-114">*status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07716-115">Тип: **[ **RDV \_ задача \_ состояние**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**</span><span class="sxs-lookup"><span data-stu-id="07716-115">Type: **[**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**</span></span>

<span data-ttu-id="07716-116">Значение перечисления [**\_ \_ состояния задачи RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) , которое указывает новое состояние задачи.</span><span class="sxs-lookup"><span data-stu-id="07716-116">A value of the [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration that specifies the new state of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07716-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07716-117">Return value</span></span>

<span data-ttu-id="07716-118">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="07716-118">Type: **HRESULT**</span></span>

<span data-ttu-id="07716-119">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="07716-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="07716-120">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="07716-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="07716-121">Требования</span><span class="sxs-lookup"><span data-stu-id="07716-121">Requirements</span></span>



| <span data-ttu-id="07716-122">Требование</span><span class="sxs-lookup"><span data-stu-id="07716-122">Requirement</span></span> | <span data-ttu-id="07716-123">Значение</span><span class="sxs-lookup"><span data-stu-id="07716-123">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="07716-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07716-124">Minimum supported client</span></span><br/> | <span data-ttu-id="07716-125">Windows 7 Корпоративная</span><span class="sxs-lookup"><span data-stu-id="07716-125">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="07716-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07716-126">Minimum supported server</span></span><br/> | <span data-ttu-id="07716-127">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="07716-127">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="07716-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07716-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07716-129">**\_состояние задачи \_ RDV**</span><span class="sxs-lookup"><span data-stu-id="07716-129">**RDV\_TASK\_STATUS**</span></span>](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)
</dt> <dt>

[<span data-ttu-id="07716-130">**ирдвтаскплугиннотифисинк**</span><span class="sxs-lookup"><span data-stu-id="07716-130">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





