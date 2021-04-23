---
title: Имстскаксевентс Оннетворкстатусчанжед, метод
description: Вызывается при изменении состояния сети. | Имстскаксевентс Оннетворкстатусчанжед, метод
ms.assetid: 177A410E-2449-4FC7-8DE5-21F83A6DD028
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Оннетворкстатусчанжед
- Службы удаленных рабочих столов метода Оннетворкстатусчанжед, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Оннетворкстатусчанжед
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b9bdcd7774493fcc54e1390ad199a6a56a7c51
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674581"
---
# <a name="imstscaxeventsonnetworkstatuschanged-method"></a><span data-ttu-id="bf55c-107">Метод Имстскаксевентс:: Оннетворкстатусчанжед</span><span class="sxs-lookup"><span data-stu-id="bf55c-107">IMsTscAxEvents::OnNetworkStatusChanged method</span></span>

<span data-ttu-id="bf55c-108">Вызывается при изменении состояния сети.</span><span class="sxs-lookup"><span data-stu-id="bf55c-108">Called when the network status has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf55c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf55c-109">Syntax</span></span>


```C++
void OnNetworkStatusChanged(
  [in] ULONG qualityLevel,
  [in] LONG  bandwidth,
  [in] LONG  rtt
);
```



## <a name="parameters"></a><span data-ttu-id="bf55c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf55c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf55c-111">*куалитилевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf55c-111">*qualityLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf55c-112">Указывает новую скорость подключения.</span><span class="sxs-lookup"><span data-stu-id="bf55c-112">Specifies the new connection speed.</span></span> <span data-ttu-id="bf55c-113">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="bf55c-113">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="bf55c-114">1</span><span class="sxs-lookup"><span data-stu-id="bf55c-114">1</span></span>
</dt> <dd>

<span data-ttu-id="bf55c-115">Менее 512 килобайт в секунду (кбит/с).</span><span class="sxs-lookup"><span data-stu-id="bf55c-115">Less than 512 kilobytes per second (KBps).</span></span>

</dd> <dt>

<span data-ttu-id="bf55c-116">2</span><span class="sxs-lookup"><span data-stu-id="bf55c-116">2</span></span>
</dt> <dd>

<span data-ttu-id="bf55c-117">512 – 1 999 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="bf55c-117">512 to 1,999 KBps.</span></span>

</dd> <dt>

<span data-ttu-id="bf55c-118">3</span><span class="sxs-lookup"><span data-stu-id="bf55c-118">3</span></span>
</dt> <dd>

<span data-ttu-id="bf55c-119">2 000 – 9 999 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="bf55c-119">2,000 to 9,999 KBps.</span></span>

</dd> <dt>

<span data-ttu-id="bf55c-120">4</span><span class="sxs-lookup"><span data-stu-id="bf55c-120">4</span></span>
</dt> <dd>

<span data-ttu-id="bf55c-121">Больше или равно 10 000 кбит/с.</span><span class="sxs-lookup"><span data-stu-id="bf55c-121">Greater than or equal to 10,000 KBps.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="bf55c-122">*пропускная способность* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf55c-122">*bandwidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf55c-123">Указывает пропускную способность подключения.</span><span class="sxs-lookup"><span data-stu-id="bf55c-123">Specifies the connection bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="bf55c-124">*RTT* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf55c-124">*rtt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf55c-125">Указывает задержку подключения.</span><span class="sxs-lookup"><span data-stu-id="bf55c-125">Specifies the connection latency.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf55c-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf55c-126">Return value</span></span>

<span data-ttu-id="bf55c-127">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bf55c-127">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf55c-128">Требования</span><span class="sxs-lookup"><span data-stu-id="bf55c-128">Requirements</span></span>



| <span data-ttu-id="bf55c-129">Требование</span><span class="sxs-lookup"><span data-stu-id="bf55c-129">Requirement</span></span> | <span data-ttu-id="bf55c-130">Значение</span><span class="sxs-lookup"><span data-stu-id="bf55c-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf55c-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bf55c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bf55c-132">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bf55c-132">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="bf55c-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bf55c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bf55c-134">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bf55c-134">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="bf55c-135">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="bf55c-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="bf55c-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf55c-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bf55c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="bf55c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf55c-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf55c-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="bf55c-139">IID</span><span class="sxs-lookup"><span data-stu-id="bf55c-139">IID</span></span><br/>                      | <span data-ttu-id="bf55c-140">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="bf55c-140">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="bf55c-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf55c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf55c-142">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="bf55c-142">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





