---
description: Метод Set задает значение заданного свойства качества потока.
ms.assetid: 57029d1c-ac63-45c0-9d07-43c7b46a27b1
title: 'Метод Итстреамкуалитиконтрол:: Set (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61deed4d6edc9b08d7c11fcc8d44d8cf91e11f99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675609"
---
# <a name="itstreamqualitycontrolset-method"></a><span data-ttu-id="1fa56-103">Метод Итстреамкуалитиконтрол:: Set</span><span class="sxs-lookup"><span data-stu-id="1fa56-103">ITStreamQualityControl::Set method</span></span>

<span data-ttu-id="1fa56-104">\[ Этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="1fa56-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1fa56-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="1fa56-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1fa56-106">Метод **Set** задает значение заданного [**свойства качества потока**](streamqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="1fa56-106">The **Set** method sets the value of a given [**stream quality property**](streamqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1fa56-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1fa56-107">Syntax</span></span>


```C++
HRESULT Set(
  [in] StreamQualityProperty Property,
  [in] long                  lValue,
  [in] TAPIControlFlags      lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="1fa56-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1fa56-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fa56-109">*Свойство* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1fa56-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fa56-110">Член перечисления [**стреамкуалитипроперти**](streamqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="1fa56-110">Member of the [**StreamQualityProperty**](streamqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="1fa56-111">*lvalue* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1fa56-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fa56-112">Требуемое значение для входного *Свойства*.</span><span class="sxs-lookup"><span data-stu-id="1fa56-112">Desired value for the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="1fa56-113">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1fa56-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fa56-114">Значение перечисления [**тапиконтролфлагс**](tapicontrolflags.md) , указывающее, как должно контролироваться значение *свойства* .</span><span class="sxs-lookup"><span data-stu-id="1fa56-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fa56-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1fa56-115">Return value</span></span>

<span data-ttu-id="1fa56-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="1fa56-116">This method can return one of these values.</span></span>



| <span data-ttu-id="1fa56-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1fa56-117">Value</span></span>                                                                                         | <span data-ttu-id="1fa56-118">Значение</span><span class="sxs-lookup"><span data-stu-id="1fa56-118">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="1fa56-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="1fa56-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1fa56-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="1fa56-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1fa56-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1fa56-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1fa56-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="1fa56-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1fa56-123">Требования</span><span class="sxs-lookup"><span data-stu-id="1fa56-123">Requirements</span></span>



| <span data-ttu-id="1fa56-124">Требование</span><span class="sxs-lookup"><span data-stu-id="1fa56-124">Requirement</span></span> | <span data-ttu-id="1fa56-125">Значение</span><span class="sxs-lookup"><span data-stu-id="1fa56-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa56-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="1fa56-126">TAPI version</span></span><br/> | <span data-ttu-id="1fa56-127">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="1fa56-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="1fa56-128">Header</span><span class="sxs-lookup"><span data-stu-id="1fa56-128">Header</span></span><br/>       | <dl> <span data-ttu-id="1fa56-129"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fa56-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1fa56-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1fa56-130">Library</span></span><br/>      | <dl> <span data-ttu-id="1fa56-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fa56-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="1fa56-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1fa56-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="1fa56-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fa56-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fa56-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1fa56-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fa56-135">**итстреамкуалитиконтрол**</span><span class="sxs-lookup"><span data-stu-id="1fa56-135">**ITStreamQualityControl**</span></span>](itstreamqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="1fa56-136">**тапиконтролфлагс**</span><span class="sxs-lookup"><span data-stu-id="1fa56-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="1fa56-137">**стреамкуалитипроперти**</span><span class="sxs-lookup"><span data-stu-id="1fa56-137">**StreamQualityProperty**</span></span>](streamqualityproperty.md)
</dt> </dl>

 

 




