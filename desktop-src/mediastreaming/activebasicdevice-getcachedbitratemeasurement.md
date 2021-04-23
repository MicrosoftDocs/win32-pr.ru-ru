---
title: Метод Активебасикдевице Жеткачедбитратемеасуремент (Плайтодевице. h)
description: Возвращает кэшированную скорость.
ms.assetid: 78C3C5D7-C46B-413D-BC18-C3861E5FDAA5
keywords:
- API потоковой передачи мультимедиа метода Жеткачедбитратемеасуремент
- API потоковой передачи мультимедиа метода Жеткачедбитратемеасуремент, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, метод Жеткачедбитратемеасуремент
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d15b38ba2730d2023b09c2fa0352ade1f1532724
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535087"
---
# <a name="activebasicdevicegetcachedbitratemeasurement-method"></a><span data-ttu-id="0f196-106">Метод Активебасикдевице:: Жеткачедбитратемеасуремент</span><span class="sxs-lookup"><span data-stu-id="0f196-106">ActiveBasicDevice::GetCachedBitrateMeasurement method</span></span>

<span data-ttu-id="0f196-107">Возвращает кэшированную скорость.</span><span class="sxs-lookup"><span data-stu-id="0f196-107">Gets the cached bitrate.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f196-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f196-108">Syntax</span></span>


```C++
HRESULT GetCachedBitrateMeasurement(
  [in]          GUID   physicalNetworkInterface,
  [out, retval] UINT64 *bitrate
);
```



## <a name="parameters"></a><span data-ttu-id="0f196-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f196-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f196-110">*фисикалнетворкинтерфаце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0f196-110">*physicalNetworkInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f196-111">Указывает физический сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="0f196-111">Specifies the physical network interface.</span></span>

</dd> <dt>

<span data-ttu-id="0f196-112">*скорость* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0f196-112">*bitrate* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0f196-113">Получает значение скорости.</span><span class="sxs-lookup"><span data-stu-id="0f196-113">Receives the bitrate value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f196-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f196-114">Return value</span></span>

<span data-ttu-id="0f196-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="0f196-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0f196-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0f196-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f196-117">Требования</span><span class="sxs-lookup"><span data-stu-id="0f196-117">Requirements</span></span>



| <span data-ttu-id="0f196-118">Требование</span><span class="sxs-lookup"><span data-stu-id="0f196-118">Requirement</span></span> | <span data-ttu-id="0f196-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0f196-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f196-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f196-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0f196-121">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0f196-121">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0f196-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f196-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0f196-123">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0f196-123">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0f196-124">Header</span><span class="sxs-lookup"><span data-stu-id="0f196-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f196-125"><dt>Плайтодевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f196-125"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f196-126">IDL</span><span class="sxs-lookup"><span data-stu-id="0f196-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0f196-127"><dt>Плайтодевице. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0f196-127"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="0f196-128">DLL</span><span class="sxs-lookup"><span data-stu-id="0f196-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f196-129"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f196-129"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f196-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f196-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="0f196-131">[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0f196-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

