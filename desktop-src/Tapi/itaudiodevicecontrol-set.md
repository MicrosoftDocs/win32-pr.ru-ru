---
description: Метод Set задает значение заданного свойства звукового устройства.
ms.assetid: 701cdfd4-9241-408c-8497-3983018e7da0
title: 'Метод Итаудиодевицеконтрол:: Set (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25aa3a6013ce79bdcea5345dcc00f52c96c8a8fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675060"
---
# <a name="itaudiodevicecontrolset-method"></a><span data-ttu-id="e5ebd-103">Метод Итаудиодевицеконтрол:: Set</span><span class="sxs-lookup"><span data-stu-id="e5ebd-103">ITAudioDeviceControl::Set method</span></span>

<span data-ttu-id="e5ebd-104">\[ Этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e5ebd-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e5ebd-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="e5ebd-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e5ebd-106">Метод **Set** задает значение заданного [**Свойства звукового устройства**](audiodeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="e5ebd-106">The **Set** method sets the value of a given [**audio device property**](audiodeviceproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e5ebd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5ebd-107">Syntax</span></span>


```C++
HRESULT get_Error(
  [out] HRESULT *phrErrorCode
);
```



## <a name="parameters"></a><span data-ttu-id="e5ebd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5ebd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5ebd-109">*Свойство* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5ebd-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ebd-110">Член перечисления [**аудиодевицепроперти**](audiodeviceproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="e5ebd-110">Member of the [**AudioDeviceProperty**](audiodeviceproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="e5ebd-111">*lvalue* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5ebd-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ebd-112">Требуемое значение для свойства.</span><span class="sxs-lookup"><span data-stu-id="e5ebd-112">Desired value for the property.</span></span>

</dd> <dt>

<span data-ttu-id="e5ebd-113">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5ebd-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ebd-114">Значение перечисления [**тапиконтролфлагс**](tapicontrolflags.md) , указывающее, как должно контролироваться значение *свойства* .</span><span class="sxs-lookup"><span data-stu-id="e5ebd-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5ebd-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5ebd-115">Return value</span></span>

<span data-ttu-id="e5ebd-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="e5ebd-116">This method can return one of these values.</span></span>



| <span data-ttu-id="e5ebd-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e5ebd-117">Return code</span></span>                                                                                   | <span data-ttu-id="e5ebd-118">Описание</span><span class="sxs-lookup"><span data-stu-id="e5ebd-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e5ebd-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e5ebd-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e5ebd-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="e5ebd-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e5ebd-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e5ebd-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e5ebd-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="e5ebd-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e5ebd-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e5ebd-123">Requirements</span></span>



| <span data-ttu-id="e5ebd-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e5ebd-124">Requirement</span></span> | <span data-ttu-id="e5ebd-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e5ebd-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e5ebd-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="e5ebd-126">TAPI version</span></span><br/> | <span data-ttu-id="e5ebd-127">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="e5ebd-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="e5ebd-128">Header</span><span class="sxs-lookup"><span data-stu-id="e5ebd-128">Header</span></span><br/>       | <dl> <span data-ttu-id="e5ebd-129"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5ebd-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e5ebd-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e5ebd-130">Library</span></span><br/>      | <dl> <span data-ttu-id="e5ebd-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5ebd-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="e5ebd-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e5ebd-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="e5ebd-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5ebd-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5ebd-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5ebd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5ebd-135">**итаудиодевицеконтрол**</span><span class="sxs-lookup"><span data-stu-id="e5ebd-135">**ITAudioDeviceControl**</span></span>](itaudiodevicecontrol.md)
</dt> <dt>

[<span data-ttu-id="e5ebd-136">**тапиконтролфлагс**</span><span class="sxs-lookup"><span data-stu-id="e5ebd-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="e5ebd-137">**аудиодевицепроперти**</span><span class="sxs-lookup"><span data-stu-id="e5ebd-137">**AudioDeviceProperty**</span></span>](audiodeviceproperty.md)
</dt> </dl>

 

 




