---
description: Возвращает профиль сканирования по умолчанию.
ms.assetid: 0e5ca06a-78ca-4d24-8dda-26babc3124b5
title: 'Метод Исканпрофилемгр:: Жетдефаултпрофиле (Сканпрофилемгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetDefaultProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: e058094fc29510d6e073abc0b05374403a2b5cd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701688"
---
# <a name="iscanprofilemgrgetdefaultprofile-method"></a><span data-ttu-id="91f51-103">Метод Исканпрофилемгр:: Жетдефаултпрофиле</span><span class="sxs-lookup"><span data-stu-id="91f51-103">IScanProfileMgr::GetDefaultProfile method</span></span>

<span data-ttu-id="91f51-104">Возвращает профиль сканирования по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="91f51-104">Gets the default scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="91f51-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91f51-105">Syntax</span></span>


```C++
HRESULT GetDefaultProfile(
  [in]  BSTR         bstrDeviceID,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="91f51-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="91f51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91f51-107">*бстрдевицеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="91f51-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91f51-108">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="91f51-108">Type: **BSTR**</span></span>

<span data-ttu-id="91f51-109">ИДЕНТИФИКАТОР устройства.</span><span class="sxs-lookup"><span data-stu-id="91f51-109">The ID of the device.</span></span>

</dd> <dt>

<span data-ttu-id="91f51-110">*ппсканпрофиле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="91f51-110">*ppScanProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91f51-111">Тип: **[ **исканпрофиле**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="91f51-111">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="91f51-112">Адрес указателя на профиль по умолчанию для устройства.</span><span class="sxs-lookup"><span data-stu-id="91f51-112">The address of a pointer to the device's default profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91f51-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91f51-113">Return value</span></span>

<span data-ttu-id="91f51-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="91f51-114">Type: **HRESULT**</span></span>

<span data-ttu-id="91f51-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="91f51-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="91f51-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="91f51-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="91f51-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91f51-117">Remarks</span></span>

<span data-ttu-id="91f51-118">Профиль по умолчанию содержит `<Default>` элемент.</span><span class="sxs-lookup"><span data-stu-id="91f51-118">The default profile has a `<Default>` element.</span></span>

## <a name="requirements"></a><span data-ttu-id="91f51-119">Требования</span><span class="sxs-lookup"><span data-stu-id="91f51-119">Requirements</span></span>



| <span data-ttu-id="91f51-120">Требование</span><span class="sxs-lookup"><span data-stu-id="91f51-120">Requirement</span></span> | <span data-ttu-id="91f51-121">Значение</span><span class="sxs-lookup"><span data-stu-id="91f51-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="91f51-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91f51-122">Minimum supported client</span></span><br/> | <span data-ttu-id="91f51-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="91f51-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="91f51-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91f51-124">Minimum supported server</span></span><br/> | <span data-ttu-id="91f51-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="91f51-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91f51-126">Header</span><span class="sxs-lookup"><span data-stu-id="91f51-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="91f51-127"><dt>Сканпрофилемгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="91f51-127"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="91f51-128">IDL</span><span class="sxs-lookup"><span data-stu-id="91f51-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="91f51-129"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="91f51-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91f51-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91f51-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91f51-131">**исканпрофилемгр**</span><span class="sxs-lookup"><span data-stu-id="91f51-131">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="91f51-132">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="91f51-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




