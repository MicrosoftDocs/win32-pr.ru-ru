---
description: Создает пустой профиль сканирования и связывает его с сканером или другим элементом для получения изображения Windows (WIA) 2,0.
ms.assetid: daa8cd66-184b-4559-a22a-c3e6d8209a3f
title: 'Метод Исканпрофилемгр:: Креатепрофиле (Сканпрофилемгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.CreateProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 657cfb339d439452f4a49f048aea50c02ab92ba6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497724"
---
# <a name="iscanprofilemgrcreateprofile-method"></a><span data-ttu-id="c7806-103">Метод Исканпрофилемгр:: Креатепрофиле</span><span class="sxs-lookup"><span data-stu-id="c7806-103">IScanProfileMgr::CreateProfile method</span></span>

<span data-ttu-id="c7806-104">Создает пустой профиль сканирования и связывает его с сканером или другим элементом для получения изображения Windows (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="c7806-104">Creates an empty scan profile and associates it with a scanner or other Windows Image Acquisition (WIA) 2.0 item.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7806-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7806-105">Syntax</span></span>


```C++
HRESULT CreateProfile(
  [in]  BSTR         bstrDeviceID,
  [in]  BSTR         bstrName,
  [in]  GUID         guidCategory,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="c7806-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7806-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7806-107">*бстрдевицеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7806-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7806-108">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c7806-108">Type: **BSTR**</span></span>

<span data-ttu-id="c7806-109">ИДЕНТИФИКАТОР устройства или элемента WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="c7806-109">The ID of the device or WIA 2.0 item.</span></span>

</dd> <dt>

<span data-ttu-id="c7806-110">*bstrName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7806-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7806-111">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c7806-111">Type: **BSTR**</span></span>

<span data-ttu-id="c7806-112">Понятное имя нового профиля.</span><span class="sxs-lookup"><span data-stu-id="c7806-112">The friendly name of the new profile.</span></span>

</dd> <dt>

<span data-ttu-id="c7806-113">*гуидкатегори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7806-113">*guidCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7806-114">Тип: **GUID**</span><span class="sxs-lookup"><span data-stu-id="c7806-114">Type: **GUID**</span></span>

<span data-ttu-id="c7806-115">Идентификатор GUID категории для устройства или элемента WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="c7806-115">The GUID of the category of the device or WIA 2.0 item.</span></span> <span data-ttu-id="c7806-116">Это должна быть одна из \_ \_ констант категории элемента WIA IPA \_ .</span><span class="sxs-lookup"><span data-stu-id="c7806-116">This must be one of the WIA\_IPA\_ITEM\_CATEGORY constants.</span></span>

</dd> <dt>

<span data-ttu-id="c7806-117">*ппсканпрофиле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c7806-117">*ppScanProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7806-118">Тип: **[ **исканпрофиле**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c7806-118">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="c7806-119">Адрес указателя на новый профиль.</span><span class="sxs-lookup"><span data-stu-id="c7806-119">The address of a pointer to the new profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7806-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7806-120">Return value</span></span>

<span data-ttu-id="c7806-121">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c7806-121">Type: **HRESULT**</span></span>

<span data-ttu-id="c7806-122">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c7806-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c7806-123">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c7806-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7806-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7806-124">Remarks</span></span>

<span data-ttu-id="c7806-125">**Исканпрофилемгр:: креатепрофиле** связывает указанное устройство с новым профилем сканирования.</span><span class="sxs-lookup"><span data-stu-id="c7806-125">**IScanProfileMgr::CreateProfile** associates the specified device with the new scan profile.</span></span>

<span data-ttu-id="c7806-126">**Исканпрофилемгр:: креатепрофиле** автоматически создает идентификатор GUID для нового профиля.</span><span class="sxs-lookup"><span data-stu-id="c7806-126">**IScanProfileMgr::CreateProfile** automatically generates a GUID for the new profile.</span></span> <span data-ttu-id="c7806-127">Получите [**GUID с помощью**](-wia-iscanprofile-getguid.md).</span><span class="sxs-lookup"><span data-stu-id="c7806-127">Get the GUID with [**GetGUID**](-wia-iscanprofile-getguid.md).</span></span>

<span data-ttu-id="c7806-128">Используйте метод [**исканпрофилемгр:: Refresh**](-wia-iscanprofilemgr-refresh.md) , если несколько объектов [**исканпрофилемгр**](-wia-iscanprofilemgr.md) могут создавать или удалять профили одновременно.</span><span class="sxs-lookup"><span data-stu-id="c7806-128">Use the [**IScanProfileMgr::Refresh**](-wia-iscanprofilemgr-refresh.md) method when more than one [**IScanProfileMgr**](-wia-iscanprofilemgr.md) object might be creating or deleting profiles at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7806-129">Требования</span><span class="sxs-lookup"><span data-stu-id="c7806-129">Requirements</span></span>



| <span data-ttu-id="c7806-130">Требование</span><span class="sxs-lookup"><span data-stu-id="c7806-130">Requirement</span></span> | <span data-ttu-id="c7806-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c7806-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7806-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7806-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c7806-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c7806-133">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="c7806-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7806-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c7806-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c7806-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c7806-136">Header</span><span class="sxs-lookup"><span data-stu-id="c7806-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7806-137"><dt>Сканпрофилемгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7806-137"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="c7806-138">IDL</span><span class="sxs-lookup"><span data-stu-id="c7806-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c7806-139"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7806-139"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7806-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7806-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7806-141">**исканпрофилемгр**</span><span class="sxs-lookup"><span data-stu-id="c7806-141">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="c7806-142">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="c7806-142">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




