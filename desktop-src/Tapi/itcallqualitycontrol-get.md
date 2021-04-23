---
description: Метод Get получает значение заданного свойства контроля качества вызова.
ms.assetid: 0fec408e-2751-4c99-afe1-4337d22eff83
title: 'Метод Иткаллкуалитиконтрол:: Get (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ea42768c173c0c073abe356e1ae6816a486a03c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679774"
---
# <a name="itcallqualitycontrolget-method"></a><span data-ttu-id="71d8e-103">Метод Иткаллкуалитиконтрол:: Get</span><span class="sxs-lookup"><span data-stu-id="71d8e-103">ITCallQualityControl::Get method</span></span>

<span data-ttu-id="71d8e-104">\[ Этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="71d8e-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="71d8e-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="71d8e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="71d8e-106">Метод **Get** получает значение заданного [Свойства контроля качества вызова](callqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="71d8e-106">The **Get** method gets the value of a given [call quality control property](callqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="71d8e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71d8e-107">Syntax</span></span>


```C++
HRESULT Get(
  [in]  CallQualityProperty Property,
  [out] long                *plValue,
  [out] TAPIControlFlags    *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="71d8e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="71d8e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71d8e-109">*Свойство* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="71d8e-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71d8e-110">Член перечисления [**каллкуалитипроперти**](callqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="71d8e-110">Member of the [**CallQualityProperty**](callqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="71d8e-111">*плвалуе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="71d8e-111">*plValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71d8e-112">Значение входного *Свойства*.</span><span class="sxs-lookup"><span data-stu-id="71d8e-112">Value of the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="71d8e-113">*плфлагс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="71d8e-113">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71d8e-114">Значение перечисления [**тапиконтролфлагс**](tapicontrolflags.md) , указывающее, как управляется значение *свойства* .</span><span class="sxs-lookup"><span data-stu-id="71d8e-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71d8e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71d8e-115">Return value</span></span>

<span data-ttu-id="71d8e-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="71d8e-116">This method can return one of these values.</span></span>



| <span data-ttu-id="71d8e-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="71d8e-117">Return code</span></span>                                                                                   | <span data-ttu-id="71d8e-118">Описание</span><span class="sxs-lookup"><span data-stu-id="71d8e-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="71d8e-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="71d8e-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="71d8e-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="71d8e-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="71d8e-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="71d8e-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="71d8e-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="71d8e-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="71d8e-123">Требования</span><span class="sxs-lookup"><span data-stu-id="71d8e-123">Requirements</span></span>



| <span data-ttu-id="71d8e-124">Требование</span><span class="sxs-lookup"><span data-stu-id="71d8e-124">Requirement</span></span> | <span data-ttu-id="71d8e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="71d8e-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="71d8e-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="71d8e-126">TAPI version</span></span><br/> | <span data-ttu-id="71d8e-127">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="71d8e-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="71d8e-128">Header</span><span class="sxs-lookup"><span data-stu-id="71d8e-128">Header</span></span><br/>       | <dl> <span data-ttu-id="71d8e-129"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="71d8e-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="71d8e-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="71d8e-130">Library</span></span><br/>      | <dl> <span data-ttu-id="71d8e-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71d8e-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="71d8e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="71d8e-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="71d8e-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71d8e-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71d8e-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71d8e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71d8e-135">**иткаллкуалитиконтрол**</span><span class="sxs-lookup"><span data-stu-id="71d8e-135">**ITCallQualityControl**</span></span>](itcallqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="71d8e-136">**тапиконтролфлагс**</span><span class="sxs-lookup"><span data-stu-id="71d8e-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="71d8e-137">**каллкуалитипроперти**</span><span class="sxs-lookup"><span data-stu-id="71d8e-137">**CallQualityProperty**</span></span>](callqualityproperty.md)
</dt> </dl>

 

 




