---
description: Возвращает понятное имя профиля.
ms.assetid: db2f8229-ce43-4608-af3f-a06011b4fac0
title: Метод Исканпрофиле::-Name (Сканпрофиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 81d1a0293802ea137f4e23b4571d32fd3d54ee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263311"
---
# <a name="iscanprofilegetname-method"></a><span data-ttu-id="89428-103">Метод Исканпрофиле:: Name</span><span class="sxs-lookup"><span data-stu-id="89428-103">IScanProfile::GetName method</span></span>

<span data-ttu-id="89428-104">Возвращает понятное имя профиля.</span><span class="sxs-lookup"><span data-stu-id="89428-104">Gets the friendly name of the profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="89428-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89428-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] BSTR *pbstrName
);
```



## <a name="parameters"></a><span data-ttu-id="89428-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="89428-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89428-107">*пбстрнаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="89428-107">*pbstrName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89428-108">Тип: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="89428-108">Type: \**BSTR\** _</span></span>

<span data-ttu-id="89428-109">Понятное имя профиля.</span><span class="sxs-lookup"><span data-stu-id="89428-109">The friendly name of the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89428-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89428-110">Return value</span></span>

<span data-ttu-id="89428-111">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="89428-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="89428-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="89428-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="89428-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="89428-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="89428-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89428-114">Remarks</span></span>

<span data-ttu-id="89428-115">Этот метод является обязательным, поскольку идентификатор GUID профиля не может использоваться для вывода профиля сканирования пользователю.</span><span class="sxs-lookup"><span data-stu-id="89428-115">This method is required because the GUID of a profile cannot be used to display the scan profile to a user.</span></span>

## <a name="requirements"></a><span data-ttu-id="89428-116">Требования</span><span class="sxs-lookup"><span data-stu-id="89428-116">Requirements</span></span>



| <span data-ttu-id="89428-117">Требование</span><span class="sxs-lookup"><span data-stu-id="89428-117">Requirement</span></span> | <span data-ttu-id="89428-118">Значение</span><span class="sxs-lookup"><span data-stu-id="89428-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="89428-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89428-119">Minimum supported client</span></span><br/> | <span data-ttu-id="89428-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="89428-120">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="89428-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89428-121">Minimum supported server</span></span><br/> | <span data-ttu-id="89428-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="89428-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89428-123">Header</span><span class="sxs-lookup"><span data-stu-id="89428-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="89428-124"><dt>Сканпрофиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="89428-124"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="89428-125">IDL</span><span class="sxs-lookup"><span data-stu-id="89428-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="89428-126"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="89428-126"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89428-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89428-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89428-128">**исканпрофиле**</span><span class="sxs-lookup"><span data-stu-id="89428-128">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="89428-129">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="89428-129">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




