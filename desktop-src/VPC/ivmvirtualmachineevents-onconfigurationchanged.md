---
title: Метод Ивмвиртуалмачинивентс Онконфигуратиончанжед (Впккоминтерфацес. h)
description: Получает уведомление о том, что значение в конфигурации этой виртуальной машины изменилось.
ms.assetid: 1955f23e-b318-41aa-b82e-81283be81608
keywords:
- Метод Онконфигуратиончанжед Virtual PC
- Метод Онконфигуратиончанжед Virtual PC, интерфейс Ивмвиртуалмачинивентс
- Ивмвиртуалмачинивентс интерфейс Virtual PC, метод Онконфигуратиончанжед
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnConfigurationChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10459562da2d87b8c883217e003cd822ef923fad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988156"
---
# <a name="ivmvirtualmachineeventsonconfigurationchanged-method"></a><span data-ttu-id="3ffe5-106">Метод Ивмвиртуалмачинивентс:: Онконфигуратиончанжед</span><span class="sxs-lookup"><span data-stu-id="3ffe5-106">IVMVirtualMachineEvents::OnConfigurationChanged method</span></span>

<span data-ttu-id="3ffe5-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3ffe5-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3ffe5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3ffe5-109">Получает уведомление о том, что значение в конфигурации этой виртуальной машины изменилось.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-109">Receives notification that a value in the configuration for this virtual machine has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ffe5-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ffe5-110">Syntax</span></span>


```C++
HRESULT OnConfigurationChanged(
  [in] BSTR    configKey,
  [in] VARIANT configData
);
```



## <a name="parameters"></a><span data-ttu-id="3ffe5-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ffe5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ffe5-112">*configKey* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ffe5-112">*configKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ffe5-113">Значение в изменяемой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-113">The value inside the configuration that has changed.</span></span>

</dd> <dt>

<span data-ttu-id="3ffe5-114">*конфигдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ffe5-114">*configData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ffe5-115">Новое значение для конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-115">The new value for the configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ffe5-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ffe5-116">Return value</span></span>

<span data-ttu-id="3ffe5-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3ffe5-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3ffe5-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ffe5-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ffe5-119">Remarks</span></span>

<span data-ttu-id="3ffe5-120">Этот метод вызывается при изменении конфигурации для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-120">This method is called when the configuration changes for this virtual machine.</span></span> <span data-ttu-id="3ffe5-121">Клиентская программа должна реализовать этот метод интерфейса для получения уведомления о \_ событии вмвиртуалмачинивент конфигуратиончанжед, исходящем от [**ивмвиртуалмачине**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="3ffe5-121">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_ConfigurationChanged event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ffe5-122">Требования</span><span class="sxs-lookup"><span data-stu-id="3ffe5-122">Requirements</span></span>



| <span data-ttu-id="3ffe5-123">Требование</span><span class="sxs-lookup"><span data-stu-id="3ffe5-123">Requirement</span></span> | <span data-ttu-id="3ffe5-124">Значение</span><span class="sxs-lookup"><span data-stu-id="3ffe5-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ffe5-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ffe5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3ffe5-126">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3ffe5-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3ffe5-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ffe5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3ffe5-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3ffe5-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3ffe5-129">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="3ffe5-129">End of client support</span></span><br/>    | <span data-ttu-id="3ffe5-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3ffe5-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3ffe5-131">Продукт</span><span class="sxs-lookup"><span data-stu-id="3ffe5-131">Product</span></span><br/>                  | <span data-ttu-id="3ffe5-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3ffe5-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3ffe5-133">Header</span><span class="sxs-lookup"><span data-stu-id="3ffe5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ffe5-134"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ffe5-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3ffe5-135">IID</span><span class="sxs-lookup"><span data-stu-id="3ffe5-135">IID</span></span><br/>                      | <span data-ttu-id="3ffe5-136">ДИИД \_ ивмвиртуалмачинивентс определяется как 9d84f560-bb67-4961-bd12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="3ffe5-136">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="3ffe5-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ffe5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ffe5-138">**ивмвиртуалмачинивентс**</span><span class="sxs-lookup"><span data-stu-id="3ffe5-138">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

