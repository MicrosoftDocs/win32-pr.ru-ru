---
title: Метод Ивмвиртуалмачинивентс Онхеартбеатстоппед (Впккоминтерфацес. h)
description: Получает уведомление о том, что пульс виртуальной машины остановлен.
ms.assetid: 58fc81a8-747c-47f9-98ec-38482694f533
keywords:
- Метод Онхеартбеатстоппед Virtual PC
- Метод Онхеартбеатстоппед Virtual PC, интерфейс Ивмвиртуалмачинивентс
- Ивмвиртуалмачинивентс интерфейс Virtual PC, метод Онхеартбеатстоппед
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnHeartbeatStopped
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ade783d2d182439d5c500dcc114c74c8278ba6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989138"
---
# <a name="ivmvirtualmachineeventsonheartbeatstopped-method"></a><span data-ttu-id="0ec1a-106">Метод Ивмвиртуалмачинивентс:: Онхеартбеатстоппед</span><span class="sxs-lookup"><span data-stu-id="0ec1a-106">IVMVirtualMachineEvents::OnHeartbeatStopped method</span></span>

<span data-ttu-id="0ec1a-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0ec1a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0ec1a-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0ec1a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0ec1a-109">Получает уведомление о том, что пульс виртуальной машины остановлен.</span><span class="sxs-lookup"><span data-stu-id="0ec1a-109">Receives notification that a virtual machine's heartbeat has stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ec1a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ec1a-110">Syntax</span></span>


```C++
HRESULT OnHeartbeatStopped();
```



## <a name="parameters"></a><span data-ttu-id="0ec1a-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ec1a-111">Parameters</span></span>

<span data-ttu-id="0ec1a-112">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0ec1a-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ec1a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ec1a-113">Return value</span></span>

<span data-ttu-id="0ec1a-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="0ec1a-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0ec1a-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0ec1a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ec1a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ec1a-116">Remarks</span></span>

<span data-ttu-id="0ec1a-117">Этот метод вызывается при внезапной остановке операционной системы на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="0ec1a-117">This method is called when the guest operating system for this virtual machine has stopped abruptly.</span></span> <span data-ttu-id="0ec1a-118">Клиентская программа должна реализовать этот метод интерфейса для получения уведомления о \_ событии вмвиртуалмачинивент хеартбеатстоппед, исходящем от [**ивмвиртуалмачине**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="0ec1a-118">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_HeartbeatStopped event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ec1a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0ec1a-119">Requirements</span></span>



| <span data-ttu-id="0ec1a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0ec1a-120">Requirement</span></span> | <span data-ttu-id="0ec1a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0ec1a-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ec1a-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0ec1a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0ec1a-123">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0ec1a-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0ec1a-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0ec1a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0ec1a-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0ec1a-125">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0ec1a-126">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="0ec1a-126">End of client support</span></span><br/>    | <span data-ttu-id="0ec1a-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0ec1a-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0ec1a-128">Продукт</span><span class="sxs-lookup"><span data-stu-id="0ec1a-128">Product</span></span><br/>                  | <span data-ttu-id="0ec1a-129">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0ec1a-129">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0ec1a-130">Header</span><span class="sxs-lookup"><span data-stu-id="0ec1a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ec1a-131"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ec1a-131"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0ec1a-132">IID</span><span class="sxs-lookup"><span data-stu-id="0ec1a-132">IID</span></span><br/>                      | <span data-ttu-id="0ec1a-133">ДИИД \_ ивмвиртуалмачинивентс определяется как 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="0ec1a-133">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="0ec1a-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ec1a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ec1a-135">**ивмвиртуалмачинивентс**</span><span class="sxs-lookup"><span data-stu-id="0ec1a-135">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

