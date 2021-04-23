---
title: Метод Ивмдвддрививентс Онмедиаинсерт (Впккоминтерфацес. h)
description: Получает уведомление о том, что носитель вставлен в диск. | Метод Ивмдвддрививентс Онмедиаинсерт (Впккоминтерфацес. h)
ms.assetid: a246e2dd-638e-4d2f-9089-74771cd8bb2b
keywords:
- Метод Онмедиаинсерт Virtual PC
- Метод Онмедиаинсерт Virtual PC, интерфейс Ивмдвддрививентс
- Ивмдвддрививентс интерфейс Virtual PC, метод Онмедиаинсерт
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 883f7990de17a9d1dbb21db9651e0f5ad4ec74aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000070"
---
# <a name="ivmdvddriveeventsonmediainsert-method"></a><span data-ttu-id="3a91c-107">Метод Ивмдвддрививентс:: Онмедиаинсерт</span><span class="sxs-lookup"><span data-stu-id="3a91c-107">IVMDVDDriveEvents::OnMediaInsert method</span></span>

<span data-ttu-id="3a91c-108">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3a91c-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3a91c-109">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3a91c-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3a91c-110">Получает уведомление о том, что носитель вставлен в диск.</span><span class="sxs-lookup"><span data-stu-id="3a91c-110">Receives notification that media has been inserted into the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a91c-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a91c-111">Syntax</span></span>


```C++
HRESULT OnMediaInsert(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a><span data-ttu-id="3a91c-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a91c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a91c-113">*mediaPath* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a91c-113">*mediaPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a91c-114">Буква диска узла или путь к ISO-образу.</span><span class="sxs-lookup"><span data-stu-id="3a91c-114">The host drive letter, or path, to the ISO image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a91c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a91c-115">Return value</span></span>

<span data-ttu-id="3a91c-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3a91c-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3a91c-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3a91c-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a91c-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a91c-118">Remarks</span></span>

<span data-ttu-id="3a91c-119">Этот метод вызывается при вставке носителя (ISO-образ или диск на диске узла).</span><span class="sxs-lookup"><span data-stu-id="3a91c-119">This method is called when media (an ISO image or a disc in a host drive) is inserted.</span></span> <span data-ttu-id="3a91c-120">Клиентская программа должна реализовать этот метод интерфейса, чтобы получить уведомление о \_ событии Вмдвддрививент INSERT, созданном из [**ивмдвддриве**](ivmdvddrive.md).</span><span class="sxs-lookup"><span data-stu-id="3a91c-120">The client program must implement this interface method to receive notification of the vmDVDDriveEvent\_OnInsert event originating from [**IVMDVDDrive**](ivmdvddrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a91c-121">Требования</span><span class="sxs-lookup"><span data-stu-id="3a91c-121">Requirements</span></span>



| <span data-ttu-id="3a91c-122">Требование</span><span class="sxs-lookup"><span data-stu-id="3a91c-122">Requirement</span></span> | <span data-ttu-id="3a91c-123">Значение</span><span class="sxs-lookup"><span data-stu-id="3a91c-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a91c-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a91c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3a91c-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3a91c-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a91c-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a91c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3a91c-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3a91c-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3a91c-128">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="3a91c-128">End of client support</span></span><br/>    | <span data-ttu-id="3a91c-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3a91c-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3a91c-130">Продукт</span><span class="sxs-lookup"><span data-stu-id="3a91c-130">Product</span></span><br/>                  | <span data-ttu-id="3a91c-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3a91c-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3a91c-132">Header</span><span class="sxs-lookup"><span data-stu-id="3a91c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a91c-133"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a91c-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3a91c-134">IID</span><span class="sxs-lookup"><span data-stu-id="3a91c-134">IID</span></span><br/>                      | <span data-ttu-id="3a91c-135">ДИИД \_ ивмдвддрививентс определяется как c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span><span class="sxs-lookup"><span data-stu-id="3a91c-135">DIID\_IVMDVDDriveEvents is defined as c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="3a91c-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a91c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a91c-137">**ивмдвддрививентс**</span><span class="sxs-lookup"><span data-stu-id="3a91c-137">**IVMDVDDriveEvents**</span></span>](ivmdvddriveevents.md)
</dt> </dl>

 

