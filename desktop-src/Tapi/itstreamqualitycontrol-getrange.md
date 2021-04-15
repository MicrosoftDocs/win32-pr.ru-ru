---
description: Метод дальнего действия возвращает диапазон допустимых значений для заданного свойства качества потока.
ms.assetid: 8c5e4652-1a40-4d7d-aa89-606e979dc03d
title: Метод Итстреамкуалитиконтрол::-Range (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea8b20c2617eb0fe54ccc4603997464fca25f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688895"
---
# <a name="itstreamqualitycontrolgetrange-method"></a><span data-ttu-id="e13c7-103">Метод Итстреамкуалитиконтрол:: Range</span><span class="sxs-lookup"><span data-stu-id="e13c7-103">ITStreamQualityControl::GetRange method</span></span>

<span data-ttu-id="e13c7-104">\[ Этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e13c7-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e13c7-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="e13c7-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e13c7-106">Метод **дальнего действия** возвращает диапазон допустимых значений для заданного [**свойства качества потока**](streamqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="e13c7-106">The **GetRange** method gets the range of valid values for a given [**stream quality property**](streamqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e13c7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e13c7-107">Syntax</span></span>


```C++
HRESULT GetRange(
  [in]  StreamQualityProperty Property,
  [out] long                  *plMin,
  [out] long                  *plMax,
  [out] long                  *plSteppingDelta,
  [out] long                  *plDefault,
  [out] TAPIControlFlags      *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e13c7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e13c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e13c7-109">*Свойство* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e13c7-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e13c7-110">Член перечисления [**стреамкуалитипроперти**](streamqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="e13c7-110">Member of the [**StreamQualityProperty**](streamqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="e13c7-111">*плмин* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e13c7-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e13c7-112">Минимальное допустимое значение для входного свойства.</span><span class="sxs-lookup"><span data-stu-id="e13c7-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="e13c7-113">*плмакс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e13c7-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e13c7-114">Максимальное допустимое значение для входного свойства.</span><span class="sxs-lookup"><span data-stu-id="e13c7-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="e13c7-115">*плстеппингделта* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e13c7-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e13c7-116">Шаг приращения, на который может увеличиться или уменьшиться значение свойства.</span><span class="sxs-lookup"><span data-stu-id="e13c7-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="e13c7-117">*плдефаулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e13c7-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e13c7-118">Значение по умолчанию для параметра *Property* .</span><span class="sxs-lookup"><span data-stu-id="e13c7-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e13c7-119">*плфлагс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e13c7-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e13c7-120">Значение перечисления [**тапиконтролфлагс**](tapicontrolflags.md) , указывающее, как управляется значение *свойства* .</span><span class="sxs-lookup"><span data-stu-id="e13c7-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e13c7-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e13c7-121">Return value</span></span>

<span data-ttu-id="e13c7-122">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="e13c7-122">This method can return one of these values.</span></span>



| <span data-ttu-id="e13c7-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e13c7-123">Return code</span></span>                                                                                   | <span data-ttu-id="e13c7-124">Описание</span><span class="sxs-lookup"><span data-stu-id="e13c7-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e13c7-125"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e13c7-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e13c7-126">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="e13c7-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e13c7-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e13c7-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e13c7-128">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="e13c7-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e13c7-129">Требования</span><span class="sxs-lookup"><span data-stu-id="e13c7-129">Requirements</span></span>



| <span data-ttu-id="e13c7-130">Требование</span><span class="sxs-lookup"><span data-stu-id="e13c7-130">Requirement</span></span> | <span data-ttu-id="e13c7-131">Значение</span><span class="sxs-lookup"><span data-stu-id="e13c7-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e13c7-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="e13c7-132">TAPI version</span></span><br/> | <span data-ttu-id="e13c7-133">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="e13c7-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="e13c7-134">Header</span><span class="sxs-lookup"><span data-stu-id="e13c7-134">Header</span></span><br/>       | <dl> <span data-ttu-id="e13c7-135"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="e13c7-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e13c7-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e13c7-136">Library</span></span><br/>      | <dl> <span data-ttu-id="e13c7-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e13c7-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="e13c7-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e13c7-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="e13c7-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e13c7-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e13c7-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e13c7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e13c7-141">**итстреамкуалитиконтрол**</span><span class="sxs-lookup"><span data-stu-id="e13c7-141">**ITStreamQualityControl**</span></span>](itstreamqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="e13c7-142">**тапиконтролфлагс**</span><span class="sxs-lookup"><span data-stu-id="e13c7-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="e13c7-143">**стреамкуалитипроперти**</span><span class="sxs-lookup"><span data-stu-id="e13c7-143">**StreamQualityProperty**</span></span>](streamqualityproperty.md)
</dt> </dl>

 

 




