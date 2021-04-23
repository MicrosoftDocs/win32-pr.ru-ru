---
description: Настраивает параметры возможностей по умолчанию.
ms.assetid: 0afcb25a-2499-4baa-82ad-0706164e2e72
title: 'Метод IH323LineEx:: Сетдефаулткапабилитипреферренце (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5604348eb80a3f423f6902f0a9a6e57204280c83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675137"
---
# <a name="ih323lineexsetdefaultcapabilitypreferrence-method"></a><span data-ttu-id="0544a-103">Метод IH323LineEx:: Сетдефаулткапабилитипреферренце</span><span class="sxs-lookup"><span data-stu-id="0544a-103">IH323LineEx::SetDefaultCapabilityPreferrence method</span></span>

<span data-ttu-id="0544a-104">\[**Сетдефаулткапабилитипреферренце** недоступен для использования в Windows Vista, windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0544a-104">\[**SetDefaultCapabilityPreferrence** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0544a-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="0544a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0544a-106">Метод **сетдефаулткапабилитипреферренце** настраивает предпочтения возможностей по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0544a-106">The **SetDefaultCapabilityPreferrence** method configures the preference of the default capabilities.</span></span> <span data-ttu-id="0544a-107">Вес по умолчанию — 100.</span><span class="sxs-lookup"><span data-stu-id="0544a-107">Capabilities have a default weight of 100.</span></span> <span data-ttu-id="0544a-108">Если приложение задает более высокий вес для возможности, оно будет иметь более высокий приоритет при согласовании H. 245.</span><span class="sxs-lookup"><span data-stu-id="0544a-108">If the application specifies a higher weight for a capability, it will have a higher priority during the H.245 negotiation.</span></span> <span data-ttu-id="0544a-109">Если приложение устанавливает весовой коэффициент возможности равным 0, оно не будет использоваться в согласовании H. 245.</span><span class="sxs-lookup"><span data-stu-id="0544a-109">If the application sets the weight of a capability to 0, it will not be used in the H.245 negotiation.</span></span>

<span data-ttu-id="0544a-110">Этот метод является кумулятивным.</span><span class="sxs-lookup"><span data-stu-id="0544a-110">This method is cumulative.</span></span> <span data-ttu-id="0544a-111">Например, если этот метод вызывается первым для отключения возможности и вызывается снова для отключения другого, обе возможности будут отключены в результате этих двух вызовов.</span><span class="sxs-lookup"><span data-stu-id="0544a-111">For example, if this method is called first to disable a capability and is called again to disable another, both capabilities will be disabled as the result of these two calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="0544a-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0544a-112">Syntax</span></span>


```C++
HRESULT SetDefaultCapabilityPreferrence(
  [in] DWORD           dwNumCaps,
  [in] H245_CAPABILITY *pCapabilities,
  [in] DWORD           *pWeights
);
```



## <a name="parameters"></a><span data-ttu-id="0544a-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="0544a-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0544a-114">*двнумкапс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0544a-114">*dwNumCaps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0544a-115">Значение **типа DWORD** , содержащее количество возможностей, заданных с помощью этого метода.</span><span class="sxs-lookup"><span data-stu-id="0544a-115">A **DWORD** value that contains the number of capabilities set with this method.</span></span>

</dd> <dt>

<span data-ttu-id="0544a-116">*пкапабилитиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0544a-116">*pCapabilities* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0544a-117">Массив возможностей.</span><span class="sxs-lookup"><span data-stu-id="0544a-117">An array of capabilities.</span></span> <span data-ttu-id="0544a-118">Каждый элемент массива является [**H245 значением \_ возможности**](h245-capability.md) .</span><span class="sxs-lookup"><span data-stu-id="0544a-118">Each element of the array is an [**H245\_CAPABILITY**](h245-capability.md) value.</span></span>

</dd> <dt>

<span data-ttu-id="0544a-119">*пвеигхтс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0544a-119">*pWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0544a-120">Массив весов, связанный с возможностями.</span><span class="sxs-lookup"><span data-stu-id="0544a-120">An array of weights associated with the capabilities.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0544a-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0544a-121">Return value</span></span>

<span data-ttu-id="0544a-122">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="0544a-122">This method can return one of these values.</span></span>



| <span data-ttu-id="0544a-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="0544a-123">Return code</span></span>                                                                                   | <span data-ttu-id="0544a-124">Описание</span><span class="sxs-lookup"><span data-stu-id="0544a-124">Description</span></span>                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0544a-125"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="0544a-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0544a-126">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="0544a-126">Method succeeded.</span></span><br/>                                                                                                                                                                                                |
| <dl> <span data-ttu-id="0544a-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0544a-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0544a-128">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="0544a-128">Insufficient memory exists to perform the operation.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="0544a-129"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0544a-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0544a-130">Параметр *пкапабилитиес* имеет **значение NULL**, либо параметр *пвеигхтс* имеет значение **null**, либо оба *Пкапабилитиес* и *пвеигхтс* имеют **значение NULL**, либо массив пкапабилитиес содержит недопустимый объект возможности H. 245.</span><span class="sxs-lookup"><span data-stu-id="0544a-130">The *pCapabilities* parameter is **NULL**, or the *pWeights* parameter is **NULL**, or both *pCapabilities* and *pWeights* are **NULL**, or the pCapabilities array contains an invalid H.245 capability object.</span></span><br/> |
| <dl> <span data-ttu-id="0544a-131"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="0544a-131"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0544a-132">Не удалось считать элемент массива *пвеигхтс* или элемента массива *пкапабилитиес* .</span><span class="sxs-lookup"><span data-stu-id="0544a-132">Unable to read an element of the *pWeights* array or an element of the *pCapabilities* array.</span></span><br/>                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="0544a-133">Требования</span><span class="sxs-lookup"><span data-stu-id="0544a-133">Requirements</span></span>



| <span data-ttu-id="0544a-134">Требование</span><span class="sxs-lookup"><span data-stu-id="0544a-134">Requirement</span></span> | <span data-ttu-id="0544a-135">Значение</span><span class="sxs-lookup"><span data-stu-id="0544a-135">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0544a-136">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="0544a-136">TAPI version</span></span><br/> | <span data-ttu-id="0544a-137">Требуется TAPI 3,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="0544a-137">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0544a-138">Header</span><span class="sxs-lookup"><span data-stu-id="0544a-138">Header</span></span><br/>       | <dl> <span data-ttu-id="0544a-139"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="0544a-139"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="0544a-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0544a-140">Library</span></span><br/>      | <dl> <span data-ttu-id="0544a-141"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0544a-141"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0544a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0544a-142">DLL</span></span><br/>          | <dl> <span data-ttu-id="0544a-143"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0544a-143"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

 




