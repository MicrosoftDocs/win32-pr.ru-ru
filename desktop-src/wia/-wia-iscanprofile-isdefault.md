---
description: Возвращает значение, указывающее, является ли профиль профилем сканирования по умолчанию для связанного устройства IWiaItem2.
ms.assetid: 32ca3b9f-6235-4eec-aa94-bf20f15a9a16
title: 'Метод Исканпрофиле:: Default (Сканпрофиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.IsDefault
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 245d36d3f6c907260e3e4858a5873309d2638530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991276"
---
# <a name="iscanprofileisdefault-method"></a><span data-ttu-id="59bac-103">Метод Исканпрофиле:: Default</span><span class="sxs-lookup"><span data-stu-id="59bac-103">IScanProfile::IsDefault method</span></span>

<span data-ttu-id="59bac-104">Возвращает значение, указывающее, является ли профиль профилем сканирования по умолчанию для связанного устройства [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="59bac-104">Gets a value that indicates whether the profile is the default scan profile of an associated [**IWiaItem2**](-wia-iwiaitem2.md) device.</span></span>

## <a name="syntax"></a><span data-ttu-id="59bac-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59bac-105">Syntax</span></span>


```C++
HRESULT IsDefault(
  [out] BOOL *pbDefault
);
```



## <a name="parameters"></a><span data-ttu-id="59bac-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="59bac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59bac-107">*пбдефаулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="59bac-107">*pbDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59bac-108">Тип: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="59bac-108">Type: \**BOOL\** _</span></span>

<span data-ttu-id="59bac-109">Указатель на _ \* BOOL \* \*.</span><span class="sxs-lookup"><span data-stu-id="59bac-109">A pointer to a _\*BOOL\*\*.</span></span>

<dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="59bac-110"><span id="TRUE"></span><span id="true"></span>**УСЛОВИЯ**</span><span class="sxs-lookup"><span data-stu-id="59bac-110"><span id="TRUE"></span><span id="true"></span>**TRUE**</span></span>


</dt> <dd>

<span data-ttu-id="59bac-111">По умолчанию используется профиль.</span><span class="sxs-lookup"><span data-stu-id="59bac-111">The profile is the default.</span></span>

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="59bac-112"><span id="FALSE"></span><span id="false"></span>**ISFALSE**</span><span class="sxs-lookup"><span data-stu-id="59bac-112"><span id="FALSE"></span><span id="false"></span>**FALSE**</span></span>


</dt> <dd>

<span data-ttu-id="59bac-113">Профиль не является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="59bac-113">The profile is not the default.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59bac-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59bac-114">Return value</span></span>

<span data-ttu-id="59bac-115">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="59bac-115">Type: **HRESULT**</span></span>

<span data-ttu-id="59bac-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="59bac-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="59bac-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="59bac-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="59bac-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59bac-118">Remarks</span></span>

<span data-ttu-id="59bac-119">*пбдефаулт* имеет **значение true** , если профиль содержит `<Default>` элемент.</span><span class="sxs-lookup"><span data-stu-id="59bac-119">*pbDefault* is **TRUE** if the profile contains a `<Default>` element.</span></span> <span data-ttu-id="59bac-120">**Значение false** , если такой элемент отсутствует.</span><span class="sxs-lookup"><span data-stu-id="59bac-120">It is **FALSE** if no such element is present.</span></span> <span data-ttu-id="59bac-121">Элемент не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="59bac-121">The element has no value.</span></span>

## <a name="requirements"></a><span data-ttu-id="59bac-122">Требования</span><span class="sxs-lookup"><span data-stu-id="59bac-122">Requirements</span></span>



| <span data-ttu-id="59bac-123">Требование</span><span class="sxs-lookup"><span data-stu-id="59bac-123">Requirement</span></span> | <span data-ttu-id="59bac-124">Значение</span><span class="sxs-lookup"><span data-stu-id="59bac-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="59bac-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59bac-125">Minimum supported client</span></span><br/> | <span data-ttu-id="59bac-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59bac-126">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="59bac-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59bac-127">Minimum supported server</span></span><br/> | <span data-ttu-id="59bac-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="59bac-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59bac-129">Header</span><span class="sxs-lookup"><span data-stu-id="59bac-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="59bac-130"><dt>Сканпрофиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="59bac-130"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="59bac-131">IDL</span><span class="sxs-lookup"><span data-stu-id="59bac-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="59bac-132"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="59bac-132"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59bac-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59bac-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59bac-134">**исканпрофиле**</span><span class="sxs-lookup"><span data-stu-id="59bac-134">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="59bac-135">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="59bac-135">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




