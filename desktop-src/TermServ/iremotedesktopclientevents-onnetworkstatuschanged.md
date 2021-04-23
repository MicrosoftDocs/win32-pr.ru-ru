---
title: Иремотедесктопклиентевентс Оннетворкстатусчанжед, метод
description: Вызывается при изменении состояния сети. | Иремотедесктопклиентевентс Оннетворкстатусчанжед, метод
ms.assetid: B68D1AA0-6403-40CA-95C5-BBBF39CEFFD8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Оннетворкстатусчанжед
- Службы удаленных рабочих столов метода Оннетворкстатусчанжед, интерфейс Иремотедесктопклиентевентс
- Службы удаленных рабочих столов интерфейса Иремотедесктопклиентевентс, метод Оннетворкстатусчанжед
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de64d8b16ea9acf9defc976d4baa91afd64f8fa7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547575"
---
# <a name="iremotedesktopclienteventsonnetworkstatuschanged-method"></a><span data-ttu-id="c5be2-107">Метод Иремотедесктопклиентевентс:: Оннетворкстатусчанжед</span><span class="sxs-lookup"><span data-stu-id="c5be2-107">IRemoteDesktopClientEvents::OnNetworkStatusChanged method</span></span>

<span data-ttu-id="c5be2-108">Вызывается при изменении состояния сети.</span><span class="sxs-lookup"><span data-stu-id="c5be2-108">Called when the network status has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5be2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5be2-109">Syntax</span></span>


```C++
void OnNetworkStatusChanged(
  [in] unsigned long qualityLevel,
  [in] long          bandwidth,
  [in] long          rtt
);
```



## <a name="parameters"></a><span data-ttu-id="c5be2-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5be2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5be2-111">*куалитилевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c5be2-111">*qualityLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5be2-112">Новый уровень качества соединения.</span><span class="sxs-lookup"><span data-stu-id="c5be2-112">The new quality level of the connection.</span></span> <span data-ttu-id="c5be2-113">Уровень качества определяется на основе значений пропускной способности и времени приема-передачи (RTT).</span><span class="sxs-lookup"><span data-stu-id="c5be2-113">The quality level is determined from the bandwidth and round-trip time (rtt) values.</span></span>

<span data-ttu-id="c5be2-114">Одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c5be2-114">One of the following values.</span></span>



| <span data-ttu-id="c5be2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c5be2-115">Value</span></span>                                                                        | <span data-ttu-id="c5be2-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c5be2-116">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="c5be2-117"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c5be2-117"><dt>0</dt></span></span> </dl> | <span data-ttu-id="c5be2-118">Не удалось определить уровень качества.</span><span class="sxs-lookup"><span data-stu-id="c5be2-118">The quality level could not be determined.</span></span><br/>       |
| <dl> <span data-ttu-id="c5be2-119"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c5be2-119"><dt>1</dt></span></span> </dl> | <span data-ttu-id="c5be2-120">Низкое качество соединения (одна панель).</span><span class="sxs-lookup"><span data-stu-id="c5be2-120">The connection quality is poor (one bar).</span></span><br/>        |
| <dl> <span data-ttu-id="c5be2-121"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c5be2-121"><dt>2</dt></span></span> </dl> | <span data-ttu-id="c5be2-122">Качество соединения справедливо (две полосы).</span><span class="sxs-lookup"><span data-stu-id="c5be2-122">The connection quality is fair (two bars).</span></span><br/>       |
| <dl> <span data-ttu-id="c5be2-123"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c5be2-123"><dt>3</dt></span></span> </dl> | <span data-ttu-id="c5be2-124">Качество подключения хорошее (три полосы).</span><span class="sxs-lookup"><span data-stu-id="c5be2-124">The connection quality is good (three bars).</span></span><br/>     |
| <dl> <span data-ttu-id="c5be2-125"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c5be2-125"><dt>4</dt></span></span> </dl> | <span data-ttu-id="c5be2-126">Качество соединения отлично (четыре полосы).</span><span class="sxs-lookup"><span data-stu-id="c5be2-126">The connection quality is excellent (four bars).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c5be2-127">*пропускная способность* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c5be2-127">*bandwidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5be2-128">Указывает новую пропускную способность подключения в килобитах в секунду (кбит/с).</span><span class="sxs-lookup"><span data-stu-id="c5be2-128">Specifies the new connection bandwidth, in kilobits per second (Kbps).</span></span>

</dd> <dt>

<span data-ttu-id="c5be2-129">*RTT* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c5be2-129">*rtt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5be2-130">Указывает новое время обращения к соединению (задержка) в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="c5be2-130">Specifies the new connection roundtrip time (latency), in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5be2-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5be2-131">Return value</span></span>

<span data-ttu-id="c5be2-132">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c5be2-132">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5be2-133">Требования</span><span class="sxs-lookup"><span data-stu-id="c5be2-133">Requirements</span></span>



| <span data-ttu-id="c5be2-134">Требование</span><span class="sxs-lookup"><span data-stu-id="c5be2-134">Requirement</span></span> | <span data-ttu-id="c5be2-135">Значение</span><span class="sxs-lookup"><span data-stu-id="c5be2-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5be2-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c5be2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c5be2-137">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c5be2-137">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="c5be2-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c5be2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c5be2-139">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c5be2-139">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="c5be2-140">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="c5be2-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="c5be2-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5be2-141"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="c5be2-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c5be2-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5be2-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5be2-143"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="c5be2-144">IID</span><span class="sxs-lookup"><span data-stu-id="c5be2-144">IID</span></span><br/>                      | <span data-ttu-id="c5be2-145">ДИИД \_ иремотедесктопклиентевентс определяется как 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="c5be2-145">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c5be2-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5be2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5be2-147">**иремотедесктопклиентевентс**</span><span class="sxs-lookup"><span data-stu-id="c5be2-147">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





