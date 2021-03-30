---
description: Возвращает число профилей сканирования для устройства.
ms.assetid: fb1f8884-28ef-460e-a8c4-b9608cc89dc6
title: 'Метод Исканпрофилемгр:: Жетнумпрофилесфордевицеид (Сканпрофилемгр. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 1a65e1f6571f4ec12a9bd91749c7419f9f9641c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263309"
---
# <a name="iscanprofilemgrgetnumprofilesfordeviceid-method"></a><span data-ttu-id="50df9-103">Метод Исканпрофилемгр:: Жетнумпрофилесфордевицеид</span><span class="sxs-lookup"><span data-stu-id="50df9-103">IScanProfileMgr::GetNumProfilesforDeviceID method</span></span>

<span data-ttu-id="50df9-104">Возвращает число профилей сканирования для устройства.</span><span class="sxs-lookup"><span data-stu-id="50df9-104">Gets the number of scan profiles for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="50df9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50df9-105">Syntax</span></span>


```C++
HRESULT GetNumProfilesforDeviceID(
  [in]  BSTR  bstrDeviceID,
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a><span data-ttu-id="50df9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="50df9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50df9-107">*бстрдевицеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50df9-107">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50df9-108">Тип: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="50df9-108">Type: **BSTR**</span></span>

<span data-ttu-id="50df9-109">ИДЕНТИФИКАТОР устройства.</span><span class="sxs-lookup"><span data-stu-id="50df9-109">The ID of the device.</span></span>

</dd> <dt>

<span data-ttu-id="50df9-110">*пулнумпрофилес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="50df9-110">*pulNumProfiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50df9-111">Тип: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="50df9-111">Type: \**ULONG\** _</span></span>

<span data-ttu-id="50df9-112">Указатель на количество профилей, доступных для устройства.</span><span class="sxs-lookup"><span data-stu-id="50df9-112">A pointer to the number of profiles available for the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50df9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50df9-113">Return value</span></span>

<span data-ttu-id="50df9-114">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="50df9-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="50df9-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="50df9-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="50df9-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="50df9-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="50df9-117">Требования</span><span class="sxs-lookup"><span data-stu-id="50df9-117">Requirements</span></span>



| <span data-ttu-id="50df9-118">Требование</span><span class="sxs-lookup"><span data-stu-id="50df9-118">Requirement</span></span> | <span data-ttu-id="50df9-119">Значение</span><span class="sxs-lookup"><span data-stu-id="50df9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="50df9-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50df9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="50df9-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="50df9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="50df9-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50df9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="50df9-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="50df9-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="50df9-124">Header</span><span class="sxs-lookup"><span data-stu-id="50df9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="50df9-125"><dt>Сканпрофилемгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="50df9-125"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="50df9-126">IDL</span><span class="sxs-lookup"><span data-stu-id="50df9-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50df9-127"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="50df9-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50df9-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50df9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50df9-129">**исканпрофилемгр**</span><span class="sxs-lookup"><span data-stu-id="50df9-129">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="50df9-130">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="50df9-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




