---
description: Возвращает идентификатор GUID профиля.
ms.assetid: 184456dd-515d-4744-91f3-0ef8b4d2114d
title: Метод Исканпрофиле::-GUID (Сканпрофиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetGUID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: e3c39815e1bc88830f64f632689028c4c527a710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344012"
---
# <a name="iscanprofilegetguid-method"></a><span data-ttu-id="8d1c0-103">Метод Исканпрофиле::</span><span class="sxs-lookup"><span data-stu-id="8d1c0-103">IScanProfile::GetGUID method</span></span>

<span data-ttu-id="8d1c0-104">Возвращает идентификатор GUID профиля.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-104">Returns the GUID of the profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d1c0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d1c0-105">Syntax</span></span>


```C++
HRESULT GetGUID(
  [out] GUID *retVal
);
```



## <a name="parameters"></a><span data-ttu-id="8d1c0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d1c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d1c0-107">*retval* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8d1c0-107">*retVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d1c0-108">Тип: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="8d1c0-108">Type: \**GUID\** _</span></span>

<span data-ttu-id="8d1c0-109">Указатель на идентификатор GUID профиля.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-109">A pointer to the GUID of the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d1c0-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d1c0-110">Return value</span></span>

<span data-ttu-id="8d1c0-111">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="8d1c0-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="8d1c0-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="8d1c0-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8d1c0-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8d1c0-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d1c0-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d1c0-114">Remarks</span></span>

<span data-ttu-id="8d1c0-115">Идентификатор GUID для профиля создается автоматически при создании профиля с помощью [**креатепрофиле**](-wia-iscanprofilemgr-createprofile.md).</span><span class="sxs-lookup"><span data-stu-id="8d1c0-115">The GUID for a profile is automatically generated when the profile is created with [**CreateProfile**](-wia-iscanprofilemgr-createprofile.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d1c0-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8d1c0-116">Requirements</span></span>



| <span data-ttu-id="8d1c0-117">Требование</span><span class="sxs-lookup"><span data-stu-id="8d1c0-117">Requirement</span></span> | <span data-ttu-id="8d1c0-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8d1c0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d1c0-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d1c0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8d1c0-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8d1c0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="8d1c0-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d1c0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8d1c0-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8d1c0-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8d1c0-123">Header</span><span class="sxs-lookup"><span data-stu-id="8d1c0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d1c0-124"><dt>Сканпрофиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d1c0-124"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="8d1c0-125">IDL</span><span class="sxs-lookup"><span data-stu-id="8d1c0-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8d1c0-126"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8d1c0-126"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d1c0-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d1c0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d1c0-128">**исканпрофиле**</span><span class="sxs-lookup"><span data-stu-id="8d1c0-128">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="8d1c0-129">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="8d1c0-129">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




