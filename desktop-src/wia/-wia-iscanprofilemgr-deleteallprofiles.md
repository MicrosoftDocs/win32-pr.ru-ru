---
description: Удаляет все профили сканирования, связанные с указанным устройством.
ms.assetid: 5abf101b-0442-47fc-8159-95db63f0af78
title: 'Исканпрофилемгр: метод:D Елетеаллпрофилес (Сканпрофилемгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteAllProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: f21e9f562d008846b4ecf6ad46e86c2c371eb9f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080809"
---
# <a name="iscanprofilemgrdeleteallprofiles-method"></a><span data-ttu-id="fc49e-103">Исканпрофилемгр: метод:D Елетеаллпрофилес</span><span class="sxs-lookup"><span data-stu-id="fc49e-103">IScanProfileMgr::DeleteAllProfiles method</span></span>

<span data-ttu-id="fc49e-104">Удаляет все профили сканирования, связанные с указанным устройством.</span><span class="sxs-lookup"><span data-stu-id="fc49e-104">Deletes all the scan profiles associated with the specified device.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc49e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc49e-105">Syntax</span></span>


```C++
HRESULT DeleteAllProfiles(
  [in] BSTR bstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="fc49e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc49e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc49e-107">*бстрдевицеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc49e-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc49e-108">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="fc49e-108">Type: **BSTR**</span></span>

<span data-ttu-id="fc49e-109">ИДЕНТИФИКАТОР устройства.</span><span class="sxs-lookup"><span data-stu-id="fc49e-109">The ID of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc49e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc49e-110">Return value</span></span>

<span data-ttu-id="fc49e-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fc49e-111">Type: **HRESULT**</span></span>

<span data-ttu-id="fc49e-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="fc49e-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fc49e-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fc49e-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc49e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="fc49e-114">Requirements</span></span>



| <span data-ttu-id="fc49e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="fc49e-115">Requirement</span></span> | <span data-ttu-id="fc49e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fc49e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc49e-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc49e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fc49e-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fc49e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="fc49e-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc49e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fc49e-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fc49e-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fc49e-121">Header</span><span class="sxs-lookup"><span data-stu-id="fc49e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc49e-122"><dt>Сканпрофилемгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc49e-122"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="fc49e-123">IDL</span><span class="sxs-lookup"><span data-stu-id="fc49e-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fc49e-124"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fc49e-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc49e-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc49e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc49e-126">**исканпрофилемгр**</span><span class="sxs-lookup"><span data-stu-id="fc49e-126">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="fc49e-127">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="fc49e-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




