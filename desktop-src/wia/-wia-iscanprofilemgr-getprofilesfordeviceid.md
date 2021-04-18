---
description: Возвращает все профили сканирования, связанные с устройством.
ms.assetid: 2e509f01-9c5e-4d17-8888-b08b6b4b9fa9
title: 'Метод Исканпрофилемгр:: Жетпрофилесфордевицеид (Сканпрофилемгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 10a7d891a114fc36de3f91341febf1616a06ed22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701686"
---
# <a name="iscanprofilemgrgetprofilesfordeviceid-method"></a><span data-ttu-id="184f6-103">Метод Исканпрофилемгр:: Жетпрофилесфордевицеид</span><span class="sxs-lookup"><span data-stu-id="184f6-103">IScanProfileMgr::GetProfilesforDeviceID method</span></span>

<span data-ttu-id="184f6-104">Возвращает все профили сканирования, связанные с устройством.</span><span class="sxs-lookup"><span data-stu-id="184f6-104">Gets all the scan profiles associated with a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="184f6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="184f6-105">Syntax</span></span>


```C++
HRESULT GetProfilesforDeviceID(
  [in]      BSTR         bstrDeviceID,
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="184f6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="184f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="184f6-107">*бстрдевицеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="184f6-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="184f6-108">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="184f6-108">Type: **BSTR**</span></span>

<span data-ttu-id="184f6-109">ИДЕНТИФИКАТОР устройства.</span><span class="sxs-lookup"><span data-stu-id="184f6-109">The ID of the device.</span></span>

</dd> <dt>

<span data-ttu-id="184f6-110">*пулнумпрофилес* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="184f6-110">*pulNumProfiles* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="184f6-111">Тип: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="184f6-111">Type: \**ULONG\** _</span></span>

<span data-ttu-id="184f6-112">При передаче указатель на максимальное число возвращаемых профилей.</span><span class="sxs-lookup"><span data-stu-id="184f6-112">When passed, a pointer to the maximum number of profiles to be returned.</span></span> <span data-ttu-id="184f6-113">При возвращении возвращается указатель на число возвращаемых профилей.</span><span class="sxs-lookup"><span data-stu-id="184f6-113">When returned, the a pointer to the number of profiles returned.</span></span>

</dd> <dt>

<span data-ttu-id="184f6-114">_ppScanProfile \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="184f6-114">_ppScanProfile\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="184f6-115">Тип: **[ **исканпрофиле**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="184f6-115">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="184f6-116">Адрес указателя на массив профилей.</span><span class="sxs-lookup"><span data-stu-id="184f6-116">The address of a pointer to an array of profiles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="184f6-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="184f6-117">Return value</span></span>

<span data-ttu-id="184f6-118">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="184f6-118">Type: **HRESULT**</span></span>

<span data-ttu-id="184f6-119">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="184f6-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="184f6-120">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="184f6-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="184f6-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="184f6-121">Remarks</span></span>

<span data-ttu-id="184f6-122">Если общее число профилей, связанных с устройством, меньше значения, переданного в *пулнумпрофилес*, то *пулнумпрофилес* возвращает этот итог.</span><span class="sxs-lookup"><span data-stu-id="184f6-122">If the total number of profiles associated with the device is smaller than the value passed to *pulNumProfiles*, then *pulNumProfiles* returns that total.</span></span> <span data-ttu-id="184f6-123">В противном случае возвращается то же значение, которое было передано в него.</span><span class="sxs-lookup"><span data-stu-id="184f6-123">Otherwise, it returns the same value that was passed to it.</span></span>

## <a name="requirements"></a><span data-ttu-id="184f6-124">Требования</span><span class="sxs-lookup"><span data-stu-id="184f6-124">Requirements</span></span>



| <span data-ttu-id="184f6-125">Требование</span><span class="sxs-lookup"><span data-stu-id="184f6-125">Requirement</span></span> | <span data-ttu-id="184f6-126">Значение</span><span class="sxs-lookup"><span data-stu-id="184f6-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="184f6-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="184f6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="184f6-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="184f6-128">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="184f6-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="184f6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="184f6-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="184f6-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="184f6-131">Header</span><span class="sxs-lookup"><span data-stu-id="184f6-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="184f6-132"><dt>Сканпрофилемгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="184f6-132"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="184f6-133">IDL</span><span class="sxs-lookup"><span data-stu-id="184f6-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="184f6-134"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="184f6-134"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="184f6-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="184f6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="184f6-136">**исканпрофилемгр**</span><span class="sxs-lookup"><span data-stu-id="184f6-136">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="184f6-137">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="184f6-137">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




