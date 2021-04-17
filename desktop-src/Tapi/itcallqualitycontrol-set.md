---
description: Метод Set задает значение заданного свойства контроля качества вызова.
ms.assetid: e83ed9d7-0a53-4555-ae44-737ab3dfb749
title: 'Метод Иткаллкуалитиконтрол:: Set (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c0a83702ba0dd4d04eb129eeed95c46d2a79a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675523"
---
# <a name="itcallqualitycontrolset-method"></a><span data-ttu-id="14ddd-103">Метод Иткаллкуалитиконтрол:: Set</span><span class="sxs-lookup"><span data-stu-id="14ddd-103">ITCallQualityControl::Set method</span></span>

<span data-ttu-id="14ddd-104">\[ Этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="14ddd-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="14ddd-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="14ddd-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="14ddd-106">Метод **Set** задает значение заданного [Свойства контроля качества вызова](callqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="14ddd-106">The **Set** method sets the value of a given [call quality control property](callqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="14ddd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14ddd-107">Syntax</span></span>


```C++
HRESULT Set(
  [in] CallQualityProperty Property,
  [in] long                lValue,
  [in] TAPIControlFlags    lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="14ddd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="14ddd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14ddd-109">*Свойство* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14ddd-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14ddd-110">Член перечисления [**каллкуалитипроперти**](callqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="14ddd-110">Member of the [**CallQualityProperty**](callqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="14ddd-111">*lvalue* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14ddd-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14ddd-112">Требуемое значение для свойства.</span><span class="sxs-lookup"><span data-stu-id="14ddd-112">Desired value for the property.</span></span>

</dd> <dt>

<span data-ttu-id="14ddd-113">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14ddd-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14ddd-114">Значение перечисления [**тапиконтролфлагс**](tapicontrolflags.md) , указывающее, как должно контролироваться значение *свойства* .</span><span class="sxs-lookup"><span data-stu-id="14ddd-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14ddd-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14ddd-115">Return value</span></span>

<span data-ttu-id="14ddd-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="14ddd-116">This method can return one of these values.</span></span>



| <span data-ttu-id="14ddd-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="14ddd-117">Return code</span></span>                                                                                   | <span data-ttu-id="14ddd-118">Описание</span><span class="sxs-lookup"><span data-stu-id="14ddd-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="14ddd-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="14ddd-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="14ddd-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="14ddd-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="14ddd-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="14ddd-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="14ddd-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="14ddd-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="14ddd-123">Требования</span><span class="sxs-lookup"><span data-stu-id="14ddd-123">Requirements</span></span>



| <span data-ttu-id="14ddd-124">Требование</span><span class="sxs-lookup"><span data-stu-id="14ddd-124">Requirement</span></span> | <span data-ttu-id="14ddd-125">Значение</span><span class="sxs-lookup"><span data-stu-id="14ddd-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="14ddd-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="14ddd-126">TAPI version</span></span><br/> | <span data-ttu-id="14ddd-127">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="14ddd-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="14ddd-128">Header</span><span class="sxs-lookup"><span data-stu-id="14ddd-128">Header</span></span><br/>       | <dl> <span data-ttu-id="14ddd-129"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="14ddd-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="14ddd-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="14ddd-130">Library</span></span><br/>      | <dl> <span data-ttu-id="14ddd-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14ddd-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="14ddd-132">DLL</span><span class="sxs-lookup"><span data-stu-id="14ddd-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="14ddd-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14ddd-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14ddd-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14ddd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14ddd-135">**иткаллкуалитиконтрол**</span><span class="sxs-lookup"><span data-stu-id="14ddd-135">**ITCallQualityControl**</span></span>](itcallqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="14ddd-136">**тапиконтролфлагс**</span><span class="sxs-lookup"><span data-stu-id="14ddd-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="14ddd-137">**каллкуалитипроперти**</span><span class="sxs-lookup"><span data-stu-id="14ddd-137">**CallQualityProperty**</span></span>](callqualityproperty.md)
</dt> </dl>

 

 




