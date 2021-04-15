---
description: Метод дальнего действия возвращает диапазон допустимых значений для заданного свойства качества вызова.
ms.assetid: 974033cf-59ce-4593-93d7-290094c20a7c
title: Метод Иткаллкуалитиконтрол::-Range (Ипмсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd3941ee8d7d0605cc6fefc61963065e4e5ba57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688826"
---
# <a name="itcallqualitycontrolgetrange-method"></a><span data-ttu-id="f4f12-103">Метод Иткаллкуалитиконтрол:: Range</span><span class="sxs-lookup"><span data-stu-id="f4f12-103">ITCallQualityControl::GetRange method</span></span>

<span data-ttu-id="f4f12-104">\[ Этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f4f12-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f4f12-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="f4f12-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f4f12-106">Метод **дальнего действия** возвращает диапазон допустимых значений для заданного [свойства качества вызова](callqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="f4f12-106">The **GetRange** method gets the range of valid values for a given [call quality property](callqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f4f12-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4f12-107">Syntax</span></span>


```C++
HRESULT GetRange(
  [in]  CallQualityProperty Property,
  [out] long                *plMin,
  [out] long                *plMax,
  [out] long                *plSteppingDelta,
  [out] long                *plDefault,
  [out] TAPIControlFlags    *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f4f12-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4f12-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4f12-109">*Свойство* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f4f12-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4f12-110">Член перечисления [**каллкуалитипроперти**](callqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="f4f12-110">Member of the [**CallQualityProperty**](callqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="f4f12-111">*плмин* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f4f12-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4f12-112">Минимальное допустимое значение для входного свойства.</span><span class="sxs-lookup"><span data-stu-id="f4f12-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="f4f12-113">*плмакс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f4f12-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4f12-114">Максимальное допустимое значение для входного свойства.</span><span class="sxs-lookup"><span data-stu-id="f4f12-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="f4f12-115">*плстеппингделта* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f4f12-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4f12-116">Шаг приращения, на который может увеличиться или уменьшиться значение свойства.</span><span class="sxs-lookup"><span data-stu-id="f4f12-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="f4f12-117">*плдефаулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f4f12-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4f12-118">Значение по умолчанию для параметра *Property* .</span><span class="sxs-lookup"><span data-stu-id="f4f12-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f4f12-119">*плфлагс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f4f12-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4f12-120">Значение перечисления [**тапиконтролфлагс**](tapicontrolflags.md) , указывающее, как управляется значение *свойства* .</span><span class="sxs-lookup"><span data-stu-id="f4f12-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4f12-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f4f12-121">Return value</span></span>

<span data-ttu-id="f4f12-122">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="f4f12-122">This method can return one of these values.</span></span>



| <span data-ttu-id="f4f12-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f4f12-123">Return code</span></span>                                                                                   | <span data-ttu-id="f4f12-124">Описание</span><span class="sxs-lookup"><span data-stu-id="f4f12-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f4f12-125"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f4f12-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f4f12-126">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="f4f12-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f4f12-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f4f12-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f4f12-128">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="f4f12-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f4f12-129">Требования</span><span class="sxs-lookup"><span data-stu-id="f4f12-129">Requirements</span></span>



| <span data-ttu-id="f4f12-130">Требование</span><span class="sxs-lookup"><span data-stu-id="f4f12-130">Requirement</span></span> | <span data-ttu-id="f4f12-131">Значение</span><span class="sxs-lookup"><span data-stu-id="f4f12-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f12-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="f4f12-132">TAPI version</span></span><br/> | <span data-ttu-id="f4f12-133">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="f4f12-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="f4f12-134">Header</span><span class="sxs-lookup"><span data-stu-id="f4f12-134">Header</span></span><br/>       | <dl> <span data-ttu-id="f4f12-135"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4f12-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f4f12-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f4f12-136">Library</span></span><br/>      | <dl> <span data-ttu-id="f4f12-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4f12-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="f4f12-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f4f12-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="f4f12-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4f12-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4f12-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4f12-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4f12-141">**иткаллкуалитиконтрол**</span><span class="sxs-lookup"><span data-stu-id="f4f12-141">**ITCallQualityControl**</span></span>](itcallqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="f4f12-142">**тапиконтролфлагс**</span><span class="sxs-lookup"><span data-stu-id="f4f12-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="f4f12-143">**каллкуалитипроперти**</span><span class="sxs-lookup"><span data-stu-id="f4f12-143">**CallQualityProperty**</span></span>](callqualityproperty.md)
</dt> </dl>

 

 




