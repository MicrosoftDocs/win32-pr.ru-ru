---
description: Удаляет указанный профиль сканирования.
ms.assetid: 31020528-3a96-492f-a3a1-e9075d4ffd14
title: 'Исканпрофилемгр: метод:D Елетепрофиле (Сканпрофилемгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: f45dfa3ef96fee194348192c2898a44df5f34be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998582"
---
# <a name="iscanprofilemgrdeleteprofile-method"></a><span data-ttu-id="f4165-103">Исканпрофилемгр: метод:D Елетепрофиле</span><span class="sxs-lookup"><span data-stu-id="f4165-103">IScanProfileMgr::DeleteProfile method</span></span>

<span data-ttu-id="f4165-104">Удаляет указанный профиль сканирования.</span><span class="sxs-lookup"><span data-stu-id="f4165-104">Deletes the specified scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4165-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4165-105">Syntax</span></span>


```C++
HRESULT DeleteProfile(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="f4165-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4165-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4165-107">*псканпрофиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f4165-107">*pScanProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4165-108">Тип: \**[**исканпрофиле**](-wia-iscanprofile.md) \** _</span><span class="sxs-lookup"><span data-stu-id="f4165-108">Type: \**[**IScanProfile**](-wia-iscanprofile.md)\** _</span></span>

<span data-ttu-id="f4165-109">Указатель на профиль.</span><span class="sxs-lookup"><span data-stu-id="f4165-109">A pointer to the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4165-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f4165-110">Return value</span></span>

<span data-ttu-id="f4165-111">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f4165-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f4165-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f4165-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f4165-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f4165-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4165-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f4165-114">Remarks</span></span>

<span data-ttu-id="f4165-115">**Исканпрофилемгр::D елетепрофиле** удаляет профиль с диска и уничтожает объект профиля в памяти.</span><span class="sxs-lookup"><span data-stu-id="f4165-115">**IScanProfileMgr::DeleteProfile** deletes the profile from disk and destroys the profile object in memory.</span></span>

<span data-ttu-id="f4165-116">Используйте метод [**исканпрофилемгр:: Refresh**](-wia-iscanprofilemgr-refresh.md) , если несколько объектов [**исканпрофилемгр**](-wia-iscanprofilemgr.md) могут создавать или удалять профили одновременно.</span><span class="sxs-lookup"><span data-stu-id="f4165-116">Use the [**IScanProfileMgr::Refresh**](-wia-iscanprofilemgr-refresh.md) method when more than one [**IScanProfileMgr**](-wia-iscanprofilemgr.md) object might be creating or deleting profiles at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4165-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f4165-117">Requirements</span></span>



| <span data-ttu-id="f4165-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f4165-118">Requirement</span></span> | <span data-ttu-id="f4165-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f4165-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4165-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f4165-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f4165-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4165-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="f4165-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f4165-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f4165-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f4165-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f4165-124">Header</span><span class="sxs-lookup"><span data-stu-id="f4165-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4165-125"><dt>Сканпрофилемгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4165-125"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="f4165-126">IDL</span><span class="sxs-lookup"><span data-stu-id="f4165-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f4165-127"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f4165-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4165-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4165-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4165-129">**исканпрофилемгр**</span><span class="sxs-lookup"><span data-stu-id="f4165-129">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="f4165-130">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="f4165-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




