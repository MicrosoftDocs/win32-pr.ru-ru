---
title: Метод Ирдвтаскплугиннотифисинк с преждевременным завершением (Сбтсв. h)
description: Вызывается агентом задачи для запроса завершения работы агента задачи.
ms.assetid: 163e0ce5-f4ee-4242-bdbb-977c5ede3451
ms.tgt_platform: multiple
keywords:
- Метод onTerminate службы удаленных рабочих столов
- Метод onTerminate службы удаленных рабочих столов, интерфейс Ирдвтаскплугиннотифисинк
- Интерфейс Ирдвтаскплугиннотифисинк службы удаленных рабочих столов, метод onTerminate
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTerminated
api_location:
- sbtsv.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b261437425b0b4dce4b2c2e17c52b6e24ea3e0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535321"
---
# <a name="irdvtaskpluginnotifysinkonterminated-method"></a><span data-ttu-id="03425-106">Метод Ирдвтаскплугиннотифисинк:: onTerminate</span><span class="sxs-lookup"><span data-stu-id="03425-106">IRDVTaskPluginNotifySink::OnTerminated method</span></span>

<span data-ttu-id="03425-107">Вызывается агентом задачи для запроса завершения работы агента задачи.</span><span class="sxs-lookup"><span data-stu-id="03425-107">Called by the task agent to request that the task agent be shut down.</span></span>

## <a name="syntax"></a><span data-ttu-id="03425-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03425-108">Syntax</span></span>


```C++
HRESULT OnTerminated(
  [in] HRESULT hr
);
```



## <a name="parameters"></a><span data-ttu-id="03425-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="03425-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03425-110">*HR* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03425-110">*hr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03425-111">Указывает, что завершение работы вызвано нормальным завершением работы или сбоем.</span><span class="sxs-lookup"><span data-stu-id="03425-111">Indicates if the shut down is due to a normal shut down or a failure.</span></span> <span data-ttu-id="03425-112">Если завершение работы является нормальным, оно содержит **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="03425-112">If the shut down is normal, this contains **S\_OK**.</span></span> <span data-ttu-id="03425-113">В противном случае он содержит код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="03425-113">Otherwise, it contains an **HRESULT** error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03425-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03425-114">Return value</span></span>

<span data-ttu-id="03425-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="03425-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="03425-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="03425-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="03425-117">Требования</span><span class="sxs-lookup"><span data-stu-id="03425-117">Requirements</span></span>



| <span data-ttu-id="03425-118">Требование</span><span class="sxs-lookup"><span data-stu-id="03425-118">Requirement</span></span> | <span data-ttu-id="03425-119">Значение</span><span class="sxs-lookup"><span data-stu-id="03425-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="03425-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="03425-120">Minimum supported client</span></span><br/> | <span data-ttu-id="03425-121">Windows 7 Корпоративная</span><span class="sxs-lookup"><span data-stu-id="03425-121">Windows 7 Enterprise</span></span><br/>                                                    |
| <span data-ttu-id="03425-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="03425-122">Minimum supported server</span></span><br/> | <span data-ttu-id="03425-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="03425-123">Windows Server 2008 R2</span></span><br/>                                                  |
| <span data-ttu-id="03425-124">Header</span><span class="sxs-lookup"><span data-stu-id="03425-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="03425-125"><dt>Сбтсв. h</dt></span><span class="sxs-lookup"><span data-stu-id="03425-125"><dt>Sbtsv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03425-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03425-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03425-127">**ирдвтаскплугиннотифисинк**</span><span class="sxs-lookup"><span data-stu-id="03425-127">**IRDVTaskPluginNotifySink**</span></span>](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





