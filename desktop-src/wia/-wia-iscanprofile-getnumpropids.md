---
description: Возвращает число идентификаторов свойств в профиле.
ms.assetid: fa587c8a-8d09-4dfc-938a-5ec8cc9265f5
title: 'Метод Исканпрофиле:: Жетнумпропидс (Сканпрофиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetNumPropIDS
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 13d8d276ca4b849fc1a2ae108369f84354d44361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154875"
---
# <a name="iscanprofilegetnumpropids-method"></a><span data-ttu-id="de06f-103">Метод Исканпрофиле:: Жетнумпропидс</span><span class="sxs-lookup"><span data-stu-id="de06f-103">IScanProfile::GetNumPropIDS method</span></span>

<span data-ttu-id="de06f-104">Возвращает число идентификаторов свойств в профиле.</span><span class="sxs-lookup"><span data-stu-id="de06f-104">Gets the number of property IDs in a profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="de06f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de06f-105">Syntax</span></span>


```C++
HRESULT GetNumPropIDS(
  [out] ULONG *num
);
```



## <a name="parameters"></a><span data-ttu-id="de06f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="de06f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de06f-107">*число* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="de06f-107">*num* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de06f-108">Тип: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="de06f-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="de06f-109">Число идентификаторов свойств в профиле.</span><span class="sxs-lookup"><span data-stu-id="de06f-109">The number of property IDs in the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de06f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de06f-110">Return value</span></span>

<span data-ttu-id="de06f-111">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="de06f-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="de06f-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="de06f-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="de06f-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="de06f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="de06f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="de06f-114">Requirements</span></span>



| <span data-ttu-id="de06f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="de06f-115">Requirement</span></span> | <span data-ttu-id="de06f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="de06f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="de06f-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="de06f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="de06f-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de06f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="de06f-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="de06f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="de06f-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="de06f-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="de06f-121">Header</span><span class="sxs-lookup"><span data-stu-id="de06f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="de06f-122"><dt>Сканпрофиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="de06f-122"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="de06f-123">IDL</span><span class="sxs-lookup"><span data-stu-id="de06f-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="de06f-124"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="de06f-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de06f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de06f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de06f-126">**исканпрофиле**</span><span class="sxs-lookup"><span data-stu-id="de06f-126">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="de06f-127">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="de06f-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




