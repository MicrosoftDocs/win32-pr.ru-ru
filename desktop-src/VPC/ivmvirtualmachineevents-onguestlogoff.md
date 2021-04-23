---
title: Метод Ивмвиртуалмачинивентс Онгуестлогофф (Впккоминтерфацес. h)
description: Получает уведомление о том, что пользователь вышел из операционной системы на виртуальной машине.
ms.assetid: 3771ba28-eea9-4c8b-9224-231b00d2f2f5
keywords:
- Метод Онгуестлогофф Virtual PC
- Метод Онгуестлогофф Virtual PC, интерфейс Ивмвиртуалмачинивентс
- Ивмвиртуалмачинивентс интерфейс Virtual PC, метод Онгуестлогофф
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnGuestLogoff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ce5100c3901b3de32a769b6bae0e16fcffe26a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988155"
---
# <a name="ivmvirtualmachineeventsonguestlogoff-method"></a><span data-ttu-id="f842e-106">Метод Ивмвиртуалмачинивентс:: Онгуестлогофф</span><span class="sxs-lookup"><span data-stu-id="f842e-106">IVMVirtualMachineEvents::OnGuestLogoff method</span></span>

<span data-ttu-id="f842e-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f842e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f842e-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f842e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f842e-109">Получает уведомление о том, что пользователь вышел из операционной системы на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="f842e-109">Receives notification that a user has logged off from the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="f842e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f842e-110">Syntax</span></span>


```C++
HRESULT OnGuestLogoff(
  [in] VMLogoffType logoffType
);
```



## <a name="parameters"></a><span data-ttu-id="f842e-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="f842e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f842e-112">*логоффтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f842e-112">*logoffType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f842e-113">Значение из перечисления [**вмлогоффтипе**](vmlogofftype.md) , описывающее тип выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="f842e-113">Value from the [**VMLogoffType**](vmlogofftype.md) enumeration that describes the type of logoff.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f842e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f842e-114">Return value</span></span>

<span data-ttu-id="f842e-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="f842e-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f842e-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f842e-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f842e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f842e-117">Requirements</span></span>



| <span data-ttu-id="f842e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f842e-118">Requirement</span></span> | <span data-ttu-id="f842e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f842e-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f842e-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f842e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f842e-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f842e-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f842e-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f842e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f842e-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f842e-123">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f842e-124">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f842e-124">End of client support</span></span><br/>    | <span data-ttu-id="f842e-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f842e-125">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f842e-126">Продукт</span><span class="sxs-lookup"><span data-stu-id="f842e-126">Product</span></span><br/>                  | <span data-ttu-id="f842e-127">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f842e-127">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f842e-128">Header</span><span class="sxs-lookup"><span data-stu-id="f842e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f842e-129"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="f842e-129"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f842e-130">IID</span><span class="sxs-lookup"><span data-stu-id="f842e-130">IID</span></span><br/>                      | <span data-ttu-id="f842e-131">ДИИД \_ ивмвиртуалмачинивентс определяется как 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="f842e-131">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="f842e-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f842e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f842e-133">**ивмвиртуалмачинивентс**</span><span class="sxs-lookup"><span data-stu-id="f842e-133">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> <dt>

[<span data-ttu-id="f842e-134">**вмлогоффтипе**</span><span class="sxs-lookup"><span data-stu-id="f842e-134">**VMLogoffType**</span></span>](vmlogofftype.md)
</dt> </dl>

 

