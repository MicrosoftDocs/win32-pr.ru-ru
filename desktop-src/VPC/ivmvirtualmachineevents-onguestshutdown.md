---
title: Метод Ивмвиртуалмачинивентс Онгуестшутдовн (Впккоминтерфацес. h)
description: Получает уведомление о том, что гостевая операционная система завершает работу.
ms.assetid: a70c746a-f1ce-4f93-b41b-b03dc83f3da2
keywords:
- Метод Онгуестшутдовн Virtual PC
- Метод Онгуестшутдовн Virtual PC, интерфейс Ивмвиртуалмачинивентс
- Ивмвиртуалмачинивентс интерфейс Virtual PC, метод Онгуестшутдовн
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnGuestShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481b6dd6e13dc17d7f9a22ef366e984c2663279c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534952"
---
# <a name="ivmvirtualmachineeventsonguestshutdown-method"></a><span data-ttu-id="7f0e4-106">Метод Ивмвиртуалмачинивентс:: Онгуестшутдовн</span><span class="sxs-lookup"><span data-stu-id="7f0e4-106">IVMVirtualMachineEvents::OnGuestShutdown method</span></span>

<span data-ttu-id="7f0e4-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7f0e4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7f0e4-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7f0e4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7f0e4-109">Получает уведомление о том, что гостевая операционная система завершает работу.</span><span class="sxs-lookup"><span data-stu-id="7f0e4-109">Receives notification that guest operating system shuts down.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f0e4-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f0e4-110">Syntax</span></span>


```C++
HRESULT OnGuestShutdown();
```



## <a name="parameters"></a><span data-ttu-id="7f0e4-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f0e4-111">Parameters</span></span>

<span data-ttu-id="7f0e4-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7f0e4-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7f0e4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f0e4-113">Return value</span></span>

<span data-ttu-id="7f0e4-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7f0e4-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7f0e4-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7f0e4-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f0e4-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7f0e4-116">Requirements</span></span>



| <span data-ttu-id="7f0e4-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7f0e4-117">Requirement</span></span> | <span data-ttu-id="7f0e4-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7f0e4-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f0e4-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f0e4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7f0e4-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7f0e4-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7f0e4-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f0e4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7f0e4-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7f0e4-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7f0e4-123">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7f0e4-123">End of client support</span></span><br/>    | <span data-ttu-id="7f0e4-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7f0e4-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7f0e4-125">Продукт</span><span class="sxs-lookup"><span data-stu-id="7f0e4-125">Product</span></span><br/>                  | <span data-ttu-id="7f0e4-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7f0e4-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7f0e4-127">Header</span><span class="sxs-lookup"><span data-stu-id="7f0e4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f0e4-128"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f0e4-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7f0e4-129">IID</span><span class="sxs-lookup"><span data-stu-id="7f0e4-129">IID</span></span><br/>                      | <span data-ttu-id="7f0e4-130">ДИИД \_ ивмвиртуалмачинивентс определяется как 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="7f0e4-130">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="7f0e4-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f0e4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f0e4-132">**ивмвиртуалмачинивентс**</span><span class="sxs-lookup"><span data-stu-id="7f0e4-132">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

