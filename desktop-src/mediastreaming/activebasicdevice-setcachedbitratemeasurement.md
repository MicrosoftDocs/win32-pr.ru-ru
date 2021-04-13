---
title: Метод Активебасикдевице Сеткачедбитратемеасуремент (Плайтодевице. h)
description: Задает кэшированную скорость.
ms.assetid: 53530217-CFF7-4376-B155-E11044621E2D
keywords:
- API потоковой передачи мультимедиа метода Сеткачедбитратемеасуремент
- API потоковой передачи мультимедиа метода Сеткачедбитратемеасуремент, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, метод Сеткачедбитратемеасуремент
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c681776b00eb9d911a4fa75a9d360b39a3d2b8c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492867"
---
# <a name="activebasicdevicesetcachedbitratemeasurement-method"></a><span data-ttu-id="5e2c2-106">Метод Активебасикдевице:: Сеткачедбитратемеасуремент</span><span class="sxs-lookup"><span data-stu-id="5e2c2-106">ActiveBasicDevice::SetCachedBitrateMeasurement method</span></span>

<span data-ttu-id="5e2c2-107">Задает кэшированную скорость.</span><span class="sxs-lookup"><span data-stu-id="5e2c2-107">Sets the cached bitrate.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e2c2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e2c2-108">Syntax</span></span>


```C++
HRESULT SetCachedBitrateMeasurement(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a><span data-ttu-id="5e2c2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e2c2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e2c2-110">*фисикалнетворкинтерфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e2c2-110">*physicalNetworkInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e2c2-111">Указывает физический сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="5e2c2-111">Specifies the physical network interface.</span></span>

</dd> <dt>

<span data-ttu-id="5e2c2-112">*скорость* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e2c2-112">*bitrate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e2c2-113">Значение, для которого устанавливается скорость.</span><span class="sxs-lookup"><span data-stu-id="5e2c2-113">The value to set the bitrate to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e2c2-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e2c2-114">Return value</span></span>

<span data-ttu-id="5e2c2-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e2c2-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5e2c2-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5e2c2-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e2c2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="5e2c2-117">Requirements</span></span>



| <span data-ttu-id="5e2c2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="5e2c2-118">Requirement</span></span> | <span data-ttu-id="5e2c2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5e2c2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e2c2-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5e2c2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5e2c2-121">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5e2c2-121">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5e2c2-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5e2c2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5e2c2-123">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e2c2-123">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5e2c2-124">Header</span><span class="sxs-lookup"><span data-stu-id="5e2c2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e2c2-125"><dt>Плайтодевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e2c2-125"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e2c2-126">IDL</span><span class="sxs-lookup"><span data-stu-id="5e2c2-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5e2c2-127"><dt>Плайтодевице. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5e2c2-127"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="5e2c2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5e2c2-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e2c2-129"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e2c2-129"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e2c2-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e2c2-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="5e2c2-131">[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5e2c2-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

