---
description: Метод Get получает значение заданного свойства качества потока.
ms.assetid: a8b5b8c7-47c9-4561-be96-af8416d854dc
title: 'Метод Итстреамкуалитиконтрол:: Get (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6758678dfacc8e0fe169189beaa8e890e801c907
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688896"
---
# <a name="itstreamqualitycontrolget-method"></a><span data-ttu-id="7285f-103">Метод Итстреамкуалитиконтрол:: Get</span><span class="sxs-lookup"><span data-stu-id="7285f-103">ITStreamQualityControl::Get method</span></span>

<span data-ttu-id="7285f-104">\[ Этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7285f-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7285f-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="7285f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7285f-106">Метод **Get** получает значение заданного [**свойства качества потока**](streamqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="7285f-106">The **Get** method retrieves the value of a given [**stream quality property**](streamqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7285f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7285f-107">Syntax</span></span>


```C++
HRESULT Get(
  [in]  StreamQualityProperty Property,
  [out] long                  *plValue,
  [out] TAPIControlFlags      *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7285f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7285f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7285f-109">*Свойство* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7285f-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7285f-110">Член перечисления [**стреамкуалитипроперти**](streamqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="7285f-110">Member of the [**StreamQualityProperty**](streamqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="7285f-111">*плвалуе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7285f-111">*plValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7285f-112">Значение входного *Свойства*.</span><span class="sxs-lookup"><span data-stu-id="7285f-112">Value of the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="7285f-113">*плфлагс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7285f-113">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7285f-114">Значение перечисления [**тапиконтролфлагс**](tapicontrolflags.md) , указывающее, как управляется значение *свойства* .</span><span class="sxs-lookup"><span data-stu-id="7285f-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7285f-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7285f-115">Return value</span></span>

<span data-ttu-id="7285f-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="7285f-116">This method can return one of these values.</span></span>



| <span data-ttu-id="7285f-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7285f-117">Return code</span></span>                                                                                   | <span data-ttu-id="7285f-118">Описание</span><span class="sxs-lookup"><span data-stu-id="7285f-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="7285f-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7285f-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7285f-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="7285f-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7285f-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7285f-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7285f-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="7285f-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7285f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="7285f-123">Requirements</span></span>



| <span data-ttu-id="7285f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="7285f-124">Requirement</span></span> | <span data-ttu-id="7285f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7285f-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7285f-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="7285f-126">TAPI version</span></span><br/> | <span data-ttu-id="7285f-127">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="7285f-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="7285f-128">Header</span><span class="sxs-lookup"><span data-stu-id="7285f-128">Header</span></span><br/>       | <dl> <span data-ttu-id="7285f-129"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="7285f-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7285f-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7285f-130">Library</span></span><br/>      | <dl> <span data-ttu-id="7285f-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7285f-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="7285f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7285f-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="7285f-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7285f-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7285f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7285f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7285f-135">**итстреамкуалитиконтрол**</span><span class="sxs-lookup"><span data-stu-id="7285f-135">**ITStreamQualityControl**</span></span>](itstreamqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="7285f-136">**тапиконтролфлагс**</span><span class="sxs-lookup"><span data-stu-id="7285f-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="7285f-137">**стреамкуалитипроперти**</span><span class="sxs-lookup"><span data-stu-id="7285f-137">**StreamQualityProperty**</span></span>](streamqualityproperty.md)
</dt> </dl>

 

 




