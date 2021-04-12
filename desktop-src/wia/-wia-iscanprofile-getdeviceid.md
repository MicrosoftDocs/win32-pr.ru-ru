---
description: Возвращает идентификатор устройства.
ms.assetid: 72a0843d-36f2-463f-8269-0e91233f1931
title: 'Метод Исканпрофиле:: GetDeviceID (Сканпрофиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetDeviceID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: fb0e2597164cb0a82c15cecf394ce7a9e0bec16d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344015"
---
# <a name="iscanprofilegetdeviceid-method"></a><span data-ttu-id="f6f44-103">Метод Исканпрофиле:: GetDeviceID</span><span class="sxs-lookup"><span data-stu-id="f6f44-103">IScanProfile::GetDeviceID method</span></span>

<span data-ttu-id="f6f44-104">Возвращает идентификатор устройства.</span><span class="sxs-lookup"><span data-stu-id="f6f44-104">Returns the ID of the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6f44-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6f44-105">Syntax</span></span>


```C++
HRESULT GetDeviceID(
  [out] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="f6f44-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6f44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6f44-107">*пбстрдевицеид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f6f44-107">*pbstrDeviceID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6f44-108">Тип: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="f6f44-108">Type: \**BSTR\** _</span></span>

<span data-ttu-id="f6f44-109">Указатель на идентификатор устройства.</span><span class="sxs-lookup"><span data-stu-id="f6f44-109">A pointer to the device ID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6f44-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6f44-110">Return value</span></span>

<span data-ttu-id="f6f44-111">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f6f44-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f6f44-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f6f44-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f6f44-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f6f44-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6f44-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f6f44-114">Requirements</span></span>



| <span data-ttu-id="f6f44-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f6f44-115">Requirement</span></span> | <span data-ttu-id="f6f44-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f6f44-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6f44-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6f44-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f6f44-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f6f44-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="f6f44-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6f44-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f6f44-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f6f44-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f6f44-121">Header</span><span class="sxs-lookup"><span data-stu-id="f6f44-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6f44-122"><dt>Сканпрофиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6f44-122"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="f6f44-123">IDL</span><span class="sxs-lookup"><span data-stu-id="f6f44-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f6f44-124"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f6f44-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6f44-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6f44-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6f44-126">**исканпрофиле**</span><span class="sxs-lookup"><span data-stu-id="f6f44-126">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="f6f44-127">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="f6f44-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




