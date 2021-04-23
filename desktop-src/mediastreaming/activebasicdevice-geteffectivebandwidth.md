---
title: Метод Активебасикдевице Жетеффективебандвидс (Плайтодевице. h)
description: Возвращает текущую эффективную пропускную способность для устройства.
ms.assetid: 88CE03AB-6F87-4E43-B673-2C693D351F10
keywords:
- API потоковой передачи мультимедиа метода Жетеффективебандвидс
- API потоковой передачи мультимедиа метода Жетеффективебандвидс, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, метод Жетеффективебандвидс
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetEffectiveBandwidth
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a97e9f1dc77040d4f55bc8997e553e0cdc5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071975"
---
# <a name="activebasicdevicegeteffectivebandwidth-method"></a><span data-ttu-id="3abb7-106">Метод Активебасикдевице:: Жетеффективебандвидс</span><span class="sxs-lookup"><span data-stu-id="3abb7-106">ActiveBasicDevice::GetEffectiveBandwidth method</span></span>

<span data-ttu-id="3abb7-107">Возвращает текущую эффективную пропускную способность для устройства.</span><span class="sxs-lookup"><span data-stu-id="3abb7-107">Gets the current effective bandwidth for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="3abb7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3abb7-108">Syntax</span></span>


```C++
HRESULT GetEffectiveBandwidth(
  [in, retval] boolean transmitSpeed,
  [out]        ULONG64 *currentSpeed
);
```



## <a name="parameters"></a><span data-ttu-id="3abb7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3abb7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3abb7-110">*трансмитспид* \[ в, retval\]</span><span class="sxs-lookup"><span data-stu-id="3abb7-110">*transmitSpeed* \[in, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3abb7-111">Указывает, получается ли скорость передачи или получается скорость приема.</span><span class="sxs-lookup"><span data-stu-id="3abb7-111">Specifies whether the transmit speed is retrieved or the receive speed is retrieved.</span></span>

<span data-ttu-id="3abb7-112">**значение true** , чтобы получить скорость передачи.</span><span class="sxs-lookup"><span data-stu-id="3abb7-112">**true** to retrieve the transmit speed.</span></span> <span data-ttu-id="3abb7-113">**значение false** , чтобы получить скорость приема.</span><span class="sxs-lookup"><span data-stu-id="3abb7-113">**false** to retrieve the receive speed.</span></span>

</dd> <dt>

<span data-ttu-id="3abb7-114">*куррентспид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3abb7-114">*currentSpeed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3abb7-115">Получает текущую эффективную пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="3abb7-115">Receives the current effective bandwidth.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3abb7-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3abb7-116">Return value</span></span>

<span data-ttu-id="3abb7-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3abb7-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3abb7-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3abb7-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3abb7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3abb7-119">Requirements</span></span>



| <span data-ttu-id="3abb7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3abb7-120">Requirement</span></span> | <span data-ttu-id="3abb7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3abb7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3abb7-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3abb7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3abb7-123">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3abb7-123">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3abb7-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3abb7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3abb7-125">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3abb7-125">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3abb7-126">Header</span><span class="sxs-lookup"><span data-stu-id="3abb7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3abb7-127"><dt>Плайтодевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="3abb7-127"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="3abb7-128">IDL</span><span class="sxs-lookup"><span data-stu-id="3abb7-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3abb7-129"><dt>Плайтодевице. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3abb7-129"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="3abb7-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3abb7-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3abb7-131"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3abb7-131"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3abb7-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3abb7-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="3abb7-133">[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3abb7-133">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

