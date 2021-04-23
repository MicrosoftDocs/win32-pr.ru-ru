---
title: Метод Активебасикдевице Сеткачедсинкпротоколинфо (Плайтодевице. h)
description: Возвращает сведения о кэшированном протоколе приемника для устройства. | Метод Активебасикдевице Сеткачедсинкпротоколинфо (Плайтодевице. h)
ms.assetid: C4856B97-89F9-43EC-B778-9E0CDAAF2C47
keywords:
- API потоковой передачи мультимедиа метода Сеткачедсинкпротоколинфо
- API потоковой передачи мультимедиа метода Сеткачедсинкпротоколинфо, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, метод Сеткачедсинкпротоколинфо
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9100cb8faeb685a0cc7a8b7b73deb11afca29a3e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105703613"
---
# <a name="activebasicdevicesetcachedsinkprotocolinfo-method"></a><span data-ttu-id="f29b7-107">Метод Активебасикдевице:: Сеткачедсинкпротоколинфо</span><span class="sxs-lookup"><span data-stu-id="f29b7-107">ActiveBasicDevice::SetCachedSinkProtocolInfo method</span></span>

<span data-ttu-id="f29b7-108">Возвращает сведения о кэшированном протоколе приемника для устройства.</span><span class="sxs-lookup"><span data-stu-id="f29b7-108">Gets the cached sink protocol info for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="f29b7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f29b7-109">Syntax</span></span>


```C++
HRESULT SetCachedSinkProtocolInfo(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a><span data-ttu-id="f29b7-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f29b7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f29b7-111">*фисикалнетворкинтерфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f29b7-111">*physicalNetworkInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f29b7-112">Указывает физический сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="f29b7-112">Specifies the physical network interface.</span></span>

</dd> <dt>

<span data-ttu-id="f29b7-113">*скорость* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f29b7-113">*bitrate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f29b7-114">Значение скорости.</span><span class="sxs-lookup"><span data-stu-id="f29b7-114">The bitrate value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f29b7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f29b7-115">Return value</span></span>

<span data-ttu-id="f29b7-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f29b7-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f29b7-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f29b7-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f29b7-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f29b7-118">Requirements</span></span>



| <span data-ttu-id="f29b7-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f29b7-119">Requirement</span></span> | <span data-ttu-id="f29b7-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f29b7-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f29b7-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f29b7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f29b7-122">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f29b7-122">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f29b7-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f29b7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f29b7-124">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f29b7-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f29b7-125">Header</span><span class="sxs-lookup"><span data-stu-id="f29b7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f29b7-126"><dt>Плайтодевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="f29b7-126"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="f29b7-127">IDL</span><span class="sxs-lookup"><span data-stu-id="f29b7-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f29b7-128"><dt>Плайтодевице. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f29b7-128"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="f29b7-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f29b7-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f29b7-130"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f29b7-130"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f29b7-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f29b7-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="f29b7-132">[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f29b7-132">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

