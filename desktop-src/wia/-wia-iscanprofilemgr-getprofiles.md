---
description: Получает все профили сканирования, доступные для пользователя в системе, в которой выполняется приложение.
ms.assetid: 9787079e-283c-4f6d-b97c-cfc1349ada30
title: 'Метод Исканпрофилемгр:: (Сканпрофилемгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 13949fe08dd547ecb5319e18ecc84139ccd310bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813881"
---
# <a name="iscanprofilemgrgetprofiles-method"></a><span data-ttu-id="cbcf6-103">Метод Исканпрофилемгр::</span><span class="sxs-lookup"><span data-stu-id="cbcf6-103">IScanProfileMgr::GetProfiles method</span></span>

<span data-ttu-id="cbcf6-104">Получает все профили сканирования, доступные для пользователя в системе, в которой выполняется приложение.</span><span class="sxs-lookup"><span data-stu-id="cbcf6-104">Gets all the scan profiles available for the user in the system that your application is running under.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbcf6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cbcf6-105">Syntax</span></span>


```C++
HRESULT GetProfiles(
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="cbcf6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cbcf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbcf6-107">*пулнумпрофилес* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="cbcf6-107">*pulNumProfiles* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbcf6-108">Тип: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="cbcf6-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="cbcf6-109">При передаче указатель на максимальное число возвращаемых профилей.</span><span class="sxs-lookup"><span data-stu-id="cbcf6-109">When passed, a pointer to the maximum number of profiles to be returned.</span></span> <span data-ttu-id="cbcf6-110">При возвращении — указатель на число возвращенных профилей.</span><span class="sxs-lookup"><span data-stu-id="cbcf6-110">When returned, a pointer to the number of profiles returned.</span></span>

</dd> <dt>

<span data-ttu-id="cbcf6-111">_ppScanProfile \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cbcf6-111">_ppScanProfile\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbcf6-112">Тип: **[ **исканпрофиле**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="cbcf6-112">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="cbcf6-113">Адрес массива указателей на профили.</span><span class="sxs-lookup"><span data-stu-id="cbcf6-113">The address of an array of pointers to profiles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbcf6-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cbcf6-114">Return value</span></span>

<span data-ttu-id="cbcf6-115">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cbcf6-115">Type: **HRESULT**</span></span>

<span data-ttu-id="cbcf6-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="cbcf6-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cbcf6-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cbcf6-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbcf6-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cbcf6-118">Remarks</span></span>

<span data-ttu-id="cbcf6-119">Если общее число профилей, доступных для пользователя, меньше значения, переданного в *пулнумпрофилес*, то *пулнумпрофилес* возвращает этот итог.</span><span class="sxs-lookup"><span data-stu-id="cbcf6-119">If the total number of profiles available for the user is smaller than the value passed to *pulNumProfiles*, then *pulNumProfiles* returns that total.</span></span> <span data-ttu-id="cbcf6-120">В противном случае возвращается то же значение, которое было передано в него.</span><span class="sxs-lookup"><span data-stu-id="cbcf6-120">Otherwise, it returns the same value that was passed to it.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbcf6-121">Требования</span><span class="sxs-lookup"><span data-stu-id="cbcf6-121">Requirements</span></span>



| <span data-ttu-id="cbcf6-122">Требование</span><span class="sxs-lookup"><span data-stu-id="cbcf6-122">Requirement</span></span> | <span data-ttu-id="cbcf6-123">Значение</span><span class="sxs-lookup"><span data-stu-id="cbcf6-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbcf6-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cbcf6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cbcf6-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cbcf6-125">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="cbcf6-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cbcf6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cbcf6-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cbcf6-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cbcf6-128">Header</span><span class="sxs-lookup"><span data-stu-id="cbcf6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbcf6-129"><dt>Сканпрофилемгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbcf6-129"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="cbcf6-130">IDL</span><span class="sxs-lookup"><span data-stu-id="cbcf6-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cbcf6-131"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cbcf6-131"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbcf6-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbcf6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbcf6-133">**исканпрофилемгр**</span><span class="sxs-lookup"><span data-stu-id="cbcf6-133">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="cbcf6-134">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="cbcf6-134">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




