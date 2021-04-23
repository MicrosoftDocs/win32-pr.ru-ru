---
title: Метод Ивмвиртуалмачинивентс Оненханцедвидеомодечанжед (Впккоминтерфацес. h)
description: Получает уведомление о том, что изменилась поддержка виртуальной машины для расширенного видеорежима.
ms.assetid: be22a859-4687-4647-9f53-f79ae8ad52a5
keywords:
- Метод Оненханцедвидеомодечанжед Virtual PC
- Метод Оненханцедвидеомодечанжед Virtual PC, интерфейс Ивмвиртуалмачинивентс
- Ивмвиртуалмачинивентс интерфейс Virtual PC, метод Оненханцедвидеомодечанжед
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnEnhancedVideoModeChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29bbc67fe298c1a47d853072d8c58ab5b3ce1988
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488919"
---
# <a name="ivmvirtualmachineeventsonenhancedvideomodechanged-method"></a><span data-ttu-id="45f8d-106">Метод Ивмвиртуалмачинивентс:: Оненханцедвидеомодечанжед</span><span class="sxs-lookup"><span data-stu-id="45f8d-106">IVMVirtualMachineEvents::OnEnhancedVideoModeChanged method</span></span>

<span data-ttu-id="45f8d-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="45f8d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="45f8d-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="45f8d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="45f8d-109">Получает уведомление о том, что изменилась поддержка виртуальной машины для расширенного видеорежима.</span><span class="sxs-lookup"><span data-stu-id="45f8d-109">Receives notification that a virtual machine's support for enhanced video mode has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="45f8d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45f8d-110">Syntax</span></span>


```C++
HRESULT OnEnhancedVideoModeChanged(
  [in] VARIANT_BOOL enhancedVideoMode
);
```



## <a name="parameters"></a><span data-ttu-id="45f8d-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="45f8d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45f8d-112">*енханцедвидеомоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="45f8d-112">*enhancedVideoMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45f8d-113">Указывает, доступен ли расширенный видеорежим.</span><span class="sxs-lookup"><span data-stu-id="45f8d-113">Indicates whether enhanced video mode is available.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45f8d-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45f8d-114">Return value</span></span>

<span data-ttu-id="45f8d-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="45f8d-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="45f8d-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="45f8d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="45f8d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="45f8d-117">Requirements</span></span>



| <span data-ttu-id="45f8d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="45f8d-118">Requirement</span></span> | <span data-ttu-id="45f8d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="45f8d-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="45f8d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45f8d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="45f8d-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="45f8d-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="45f8d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45f8d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="45f8d-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="45f8d-123">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="45f8d-124">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="45f8d-124">End of client support</span></span><br/>    | <span data-ttu-id="45f8d-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="45f8d-125">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="45f8d-126">Продукт</span><span class="sxs-lookup"><span data-stu-id="45f8d-126">Product</span></span><br/>                  | <span data-ttu-id="45f8d-127">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="45f8d-127">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="45f8d-128">Header</span><span class="sxs-lookup"><span data-stu-id="45f8d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="45f8d-129"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="45f8d-129"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="45f8d-130">IID</span><span class="sxs-lookup"><span data-stu-id="45f8d-130">IID</span></span><br/>                      | <span data-ttu-id="45f8d-131">ДИИД \_ ивмвиртуалмачинивентс определяется как 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="45f8d-131">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="45f8d-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45f8d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45f8d-133">**ивмвиртуалмачинивентс**</span><span class="sxs-lookup"><span data-stu-id="45f8d-133">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

