---
title: Метод Активебасикдевице Жеткачедсинкпротоколинфо (Плайтодевице. h)
description: Возвращает сведения о кэшированном протоколе приемника для устройства. | Метод Активебасикдевице Жеткачедсинкпротоколинфо (Плайтодевице. h)
ms.assetid: C6A3C4B5-1883-4E71-83D2-11E378A4FBCA
keywords:
- API потоковой передачи мультимедиа метода Жеткачедсинкпротоколинфо
- API потоковой передачи мультимедиа метода Жеткачедсинкпротоколинфо, интерфейс Активебасикдевице
- API потоковой передачи мультимедиа интерфейса Активебасикдевице, метод Жеткачедсинкпротоколинфо
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056cc351a1ecd1c8eef07d4e994da8e895aa85f8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694040"
---
# <a name="activebasicdevicegetcachedsinkprotocolinfo-method"></a><span data-ttu-id="493c8-107">Метод Активебасикдевице:: Жеткачедсинкпротоколинфо</span><span class="sxs-lookup"><span data-stu-id="493c8-107">ActiveBasicDevice::GetCachedSinkProtocolInfo method</span></span>

<span data-ttu-id="493c8-108">Возвращает сведения о кэшированном протоколе приемника для устройства.</span><span class="sxs-lookup"><span data-stu-id="493c8-108">Gets the cached sink protocol info for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="493c8-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="493c8-109">Syntax</span></span>


```C++
HRESULT GetCachedSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="493c8-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="493c8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="493c8-111">*значение* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="493c8-111">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="493c8-112">Сведения о кэшированном протоколе приемника для устройства.</span><span class="sxs-lookup"><span data-stu-id="493c8-112">The cached sink protocol info for the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="493c8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="493c8-113">Return value</span></span>

<span data-ttu-id="493c8-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="493c8-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="493c8-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="493c8-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="493c8-116">Требования</span><span class="sxs-lookup"><span data-stu-id="493c8-116">Requirements</span></span>



| <span data-ttu-id="493c8-117">Требование</span><span class="sxs-lookup"><span data-stu-id="493c8-117">Requirement</span></span> | <span data-ttu-id="493c8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="493c8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="493c8-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="493c8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="493c8-120">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="493c8-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="493c8-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="493c8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="493c8-122">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="493c8-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="493c8-123">Header</span><span class="sxs-lookup"><span data-stu-id="493c8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="493c8-124"><dt>Плайтодевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="493c8-124"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="493c8-125">IDL</span><span class="sxs-lookup"><span data-stu-id="493c8-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="493c8-126"><dt>Плайтодевице. idl</dt></span><span class="sxs-lookup"><span data-stu-id="493c8-126"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="493c8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="493c8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="493c8-128"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="493c8-128"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="493c8-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="493c8-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="493c8-130">[**активебасикдевице**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="493c8-130">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

