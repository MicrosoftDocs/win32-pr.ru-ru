---
description: Возвращает идентификатор GUID категории элемента для получения образа Windows (WIA) 2,0, с которым связан профиль.
ms.assetid: 2c816789-ad66-4b06-9160-7a86289ff373
title: Метод Исканпрофиле::-Item (Сканпрофиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 888a3bb5bcb6e6c4fc2fefff2d976eb7fc1c7f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650588"
---
# <a name="iscanprofilegetitem-method"></a><span data-ttu-id="fda93-103">Метод Исканпрофиле:: Item</span><span class="sxs-lookup"><span data-stu-id="fda93-103">IScanProfile::GetItem method</span></span>

<span data-ttu-id="fda93-104">Возвращает идентификатор GUID категории элемента для получения образа Windows (WIA) 2,0, с которым связан профиль.</span><span class="sxs-lookup"><span data-stu-id="fda93-104">Gets the GUID of the category of the Windows Image Acquisition (WIA) 2.0 item that the profile is associated with.</span></span>

## <a name="syntax"></a><span data-ttu-id="fda93-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fda93-105">Syntax</span></span>


```C++
HRESULT GetItem(
  [out] GUID *pguidCategory
);
```



## <a name="parameters"></a><span data-ttu-id="fda93-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fda93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fda93-107">*пгуидкатегори* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fda93-107">*pguidCategory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fda93-108">Тип: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="fda93-108">Type: \**GUID\** _</span></span>

<span data-ttu-id="fda93-109">Указатель на идентификатор GUID категории элемента WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="fda93-109">A pointer to the GUID of the category of the WIA 2.0 item.</span></span> <span data-ttu-id="fda93-110">Это всегда одна из \_ \_ констант категории элемента WIA IPA \_ .</span><span class="sxs-lookup"><span data-stu-id="fda93-110">This is always one of the WIA\_IPA\_ITEM\_CATEGORY constants.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fda93-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fda93-111">Return value</span></span>

<span data-ttu-id="fda93-112">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="fda93-112">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="fda93-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="fda93-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fda93-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fda93-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fda93-115">Требования</span><span class="sxs-lookup"><span data-stu-id="fda93-115">Requirements</span></span>



| <span data-ttu-id="fda93-116">Требование</span><span class="sxs-lookup"><span data-stu-id="fda93-116">Requirement</span></span> | <span data-ttu-id="fda93-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fda93-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fda93-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fda93-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fda93-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fda93-119">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="fda93-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fda93-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fda93-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fda93-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fda93-122">Header</span><span class="sxs-lookup"><span data-stu-id="fda93-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fda93-123"><dt>Сканпрофиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="fda93-123"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="fda93-124">IDL</span><span class="sxs-lookup"><span data-stu-id="fda93-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fda93-125"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fda93-125"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fda93-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fda93-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fda93-127">**исканпрофиле**</span><span class="sxs-lookup"><span data-stu-id="fda93-127">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="fda93-128">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="fda93-128">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




