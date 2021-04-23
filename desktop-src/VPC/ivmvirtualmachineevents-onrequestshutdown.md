---
title: Метод Ивмвиртуалмачинивентс Онрекуестшутдовн (Впккоминтерфацес. h)
description: Получает уведомление о том, что был выполнен запрос на завершение работы.
ms.assetid: e04131fd-5ca7-4392-9725-ba62b905324a
keywords:
- Метод Онрекуестшутдовн Virtual PC
- Метод Онрекуестшутдовн Virtual PC, интерфейс Ивмвиртуалмачинивентс
- Ивмвиртуалмачинивентс интерфейс Virtual PC, метод Онрекуестшутдовн
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnRequestShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94dce60a7dfdb5ed5dce714e8b8eafcbd9558b95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491295"
---
# <a name="ivmvirtualmachineeventsonrequestshutdown-method"></a><span data-ttu-id="4b055-106">Метод Ивмвиртуалмачинивентс:: Онрекуестшутдовн</span><span class="sxs-lookup"><span data-stu-id="4b055-106">IVMVirtualMachineEvents::OnRequestShutdown method</span></span>

<span data-ttu-id="4b055-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4b055-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4b055-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4b055-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4b055-109">Получает уведомление о том, что был выполнен запрос на завершение работы.</span><span class="sxs-lookup"><span data-stu-id="4b055-109">Receives notification that a shutdown request has been made.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b055-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b055-110">Syntax</span></span>


```C++
HRESULT OnRequestShutdown();
```



## <a name="parameters"></a><span data-ttu-id="4b055-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b055-111">Parameters</span></span>

<span data-ttu-id="4b055-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4b055-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b055-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b055-113">Return value</span></span>

<span data-ttu-id="4b055-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4b055-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4b055-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4b055-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b055-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b055-116">Remarks</span></span>

<span data-ttu-id="4b055-117">Этот метод вызывается при каждом завершении сеанса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4b055-117">This method is called whenever the virtual machine session is about to shut down.</span></span> <span data-ttu-id="4b055-118">Клиентская программа должна реализовать этот метод интерфейса для получения уведомления о событии **вмвиртуалмачинивент \_ рекуестшутдовн** , исходящем от [**ивмвиртуалмачине**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="4b055-118">The client program must implement this interface method to receive notification of the **vmVirtualMachineEvent\_RequestShutdown** event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

<span data-ttu-id="4b055-119">Это уведомление о событии отправляется только в том случае, если сеанс работы с виртуальными машинами скоро завершит работу.</span><span class="sxs-lookup"><span data-stu-id="4b055-119">This event notification is sent only when the virtual machines session is about to shut down.</span></span> <span data-ttu-id="4b055-120">Подпрограммы завершения работы операционной системы, такие как [**ивмгуестос:: Shutdown**](ivmguestos-shutdown.md), не вызывают это событие напрямую, кроме случаев, когда они также пытаются выполнить программное выключение виртуального оборудования.</span><span class="sxs-lookup"><span data-stu-id="4b055-120">Operating system shutdown routines, such as [**IVMGuestOS::Shutdown**](ivmguestos-shutdown.md), do not fire this event directly unless they also attempt to perform a software power off of the virtual hardware.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b055-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4b055-121">Requirements</span></span>



| <span data-ttu-id="4b055-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4b055-122">Requirement</span></span> | <span data-ttu-id="4b055-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4b055-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b055-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b055-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4b055-125">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4b055-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4b055-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b055-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4b055-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4b055-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4b055-128">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4b055-128">End of client support</span></span><br/>    | <span data-ttu-id="4b055-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4b055-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4b055-130">Продукт</span><span class="sxs-lookup"><span data-stu-id="4b055-130">Product</span></span><br/>                  | <span data-ttu-id="4b055-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4b055-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4b055-132">Header</span><span class="sxs-lookup"><span data-stu-id="4b055-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b055-133"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b055-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4b055-134">IID</span><span class="sxs-lookup"><span data-stu-id="4b055-134">IID</span></span><br/>                      | <span data-ttu-id="4b055-135">ДИИД \_ ивмвиртуалмачинивентс определяется как 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="4b055-135">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="4b055-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b055-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b055-137">**ивмвиртуалмачинивентс**</span><span class="sxs-lookup"><span data-stu-id="4b055-137">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

