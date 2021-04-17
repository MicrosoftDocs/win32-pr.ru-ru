---
description: Открывает профиль сканирования, сохраненный на диске в виде XML-файла.
ms.assetid: 2b45280e-a1b6-4db9-af8c-09faff34b067
title: 'Метод Исканпрофилемгр:: Опенпрофиле (Сканпрофилемгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.OpenProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 40d380a2b0405445cba72a0aac73c4b529114fcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711965"
---
# <a name="iscanprofilemgropenprofile-method"></a><span data-ttu-id="5e240-103">Метод Исканпрофилемгр:: Опенпрофиле</span><span class="sxs-lookup"><span data-stu-id="5e240-103">IScanProfileMgr::OpenProfile method</span></span>

<span data-ttu-id="5e240-104">Открывает профиль сканирования, сохраненный на диске в виде XML-файла.</span><span class="sxs-lookup"><span data-stu-id="5e240-104">Opens a scan profile that has been saved to disk as an XML file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e240-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e240-105">Syntax</span></span>


```C++
HRESULT OpenProfile(
  [in]  GUID         guid,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="5e240-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e240-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e240-107">*идентификатор GUID* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5e240-107">*guid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e240-108">Тип: **GUID**</span><span class="sxs-lookup"><span data-stu-id="5e240-108">Type: **GUID**</span></span>

<span data-ttu-id="5e240-109">Идентификатор GUID профиля.</span><span class="sxs-lookup"><span data-stu-id="5e240-109">The GUID of the profile.</span></span>

</dd> <dt>

<span data-ttu-id="5e240-110">*ппсканпрофиле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5e240-110">*ppScanProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e240-111">Тип: **[ **исканпрофиле**](-wia-iscanprofile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="5e240-111">Type: **[**IScanProfile**](-wia-iscanprofile.md)\*\***</span></span>

<span data-ttu-id="5e240-112">Адрес указателя на профиль.</span><span class="sxs-lookup"><span data-stu-id="5e240-112">The address of a pointer to the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e240-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e240-113">Return value</span></span>

<span data-ttu-id="5e240-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5e240-114">Type: **HRESULT**</span></span>

<span data-ttu-id="5e240-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5e240-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5e240-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5e240-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e240-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5e240-117">Remarks</span></span>

<span data-ttu-id="5e240-118">Если профиль сканирования сохранен с помощью метода [**Save**](-wia-iscanprofile-save.md) , он сохраняется в виде XML-файла в файле% UserProfile% \\ Application Data \\ \\ центра документов Microsoft \\ усерсканпрофилес.</span><span class="sxs-lookup"><span data-stu-id="5e240-118">If a scan profile is saved using the [**Save**](-wia-iscanprofile-save.md) method, it is stored as an XML file at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e240-119">Требования</span><span class="sxs-lookup"><span data-stu-id="5e240-119">Requirements</span></span>



| <span data-ttu-id="5e240-120">Требование</span><span class="sxs-lookup"><span data-stu-id="5e240-120">Requirement</span></span> | <span data-ttu-id="5e240-121">Значение</span><span class="sxs-lookup"><span data-stu-id="5e240-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e240-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5e240-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5e240-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e240-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="5e240-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5e240-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5e240-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5e240-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5e240-126">Header</span><span class="sxs-lookup"><span data-stu-id="5e240-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e240-127"><dt>Сканпрофилемгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e240-127"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="5e240-128">IDL</span><span class="sxs-lookup"><span data-stu-id="5e240-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5e240-129"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5e240-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e240-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e240-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e240-131">**исканпрофилемгр**</span><span class="sxs-lookup"><span data-stu-id="5e240-131">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="5e240-132">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="5e240-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




