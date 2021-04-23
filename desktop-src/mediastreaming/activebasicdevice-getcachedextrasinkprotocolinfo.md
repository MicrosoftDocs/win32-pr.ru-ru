---
title: Метод Активебасикдевице Жеткачедекстрасинкпротоколинфо (Плайтодевице. h)
description: Возвращает дополнительные кэшированные сведения о протоколе приемника для устройства.
ms.assetid: 97112921-1C1D-4FC9-8FE6-1381F3773351
keywords:
- API потоковой передачи мультимедиа метода Жеткачедекстрасинкпротоколинфо
- API потоковой передачи мультимедиа метода Жеткачедекстрасинкпротоколинфо, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, метод Жеткачедекстрасинкпротоколинфо
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedExtraSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5bb013d1356d5ff02e709a92f01eceff6c2e0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415725"
---
# <a name="activebasicdevicegetcachedextrasinkprotocolinfo-method"></a><span data-ttu-id="2dc9a-106">Метод Активебасикдевице:: Жеткачедекстрасинкпротоколинфо</span><span class="sxs-lookup"><span data-stu-id="2dc9a-106">ActiveBasicDevice::GetCachedExtraSinkProtocolInfo method</span></span>

<span data-ttu-id="2dc9a-107">Возвращает дополнительные кэшированные сведения о протоколе приемника для устройства.</span><span class="sxs-lookup"><span data-stu-id="2dc9a-107">Gets additional cached sink protocol info for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dc9a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2dc9a-108">Syntax</span></span>


```C++
HRESULT GetCachedExtraSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="2dc9a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2dc9a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dc9a-110">*значение* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2dc9a-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2dc9a-111">Дополнительные кэшированные сведения о протоколе приемника для устройства.</span><span class="sxs-lookup"><span data-stu-id="2dc9a-111">The extra cached sink protocol info for the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dc9a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2dc9a-112">Return value</span></span>

<span data-ttu-id="2dc9a-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="2dc9a-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2dc9a-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2dc9a-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dc9a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2dc9a-115">Requirements</span></span>



| <span data-ttu-id="2dc9a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2dc9a-116">Requirement</span></span> | <span data-ttu-id="2dc9a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2dc9a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dc9a-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2dc9a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2dc9a-119">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2dc9a-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2dc9a-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2dc9a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2dc9a-121">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2dc9a-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2dc9a-122">Header</span><span class="sxs-lookup"><span data-stu-id="2dc9a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dc9a-123"><dt>Плайтодевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dc9a-123"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="2dc9a-124">IDL</span><span class="sxs-lookup"><span data-stu-id="2dc9a-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2dc9a-125"><dt>Плайтодевице. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2dc9a-125"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="2dc9a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2dc9a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2dc9a-127"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2dc9a-127"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dc9a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2dc9a-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="2dc9a-129">[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2dc9a-129">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

