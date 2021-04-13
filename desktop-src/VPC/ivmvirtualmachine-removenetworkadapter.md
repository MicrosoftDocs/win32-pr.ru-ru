---
title: Метод Ивмвиртуалмачине Ремовенетворкадаптер (Впккоминтерфацес. h)
description: Удаляет сетевой интерфейс из виртуальной машины.
ms.assetid: 25a5b172-55b8-4cbe-98aa-630148cf6b6d
keywords:
- Метод Ремовенетворкадаптер Virtual PC
- Метод Ремовенетворкадаптер Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Ремовенетворкадаптер
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27424f7a3dc5445f56d960393aa12345fcf5f1cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492240"
---
# <a name="ivmvirtualmachineremovenetworkadapter-method"></a><span data-ttu-id="4e2d7-106">Метод Ивмвиртуалмачине:: Ремовенетворкадаптер</span><span class="sxs-lookup"><span data-stu-id="4e2d7-106">IVMVirtualMachine::RemoveNetworkAdapter method</span></span>

<span data-ttu-id="4e2d7-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4e2d7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4e2d7-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4e2d7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4e2d7-109">Удаляет сетевой интерфейс из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4e2d7-109">Removes a network interface from the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e2d7-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e2d7-110">Syntax</span></span>


```C++
HRESULT RemoveNetworkAdapter(
  [in] IVMNetworkAdapter *networkAdapter
);
```



## <a name="parameters"></a><span data-ttu-id="4e2d7-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e2d7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e2d7-112">*сетевого адаптера* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4e2d7-112">*networkAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e2d7-113">Объект [**ивмнетворкадаптер**](ivmnetworkadapter.md) , представляющий удаляемый сетевой адаптер.</span><span class="sxs-lookup"><span data-stu-id="4e2d7-113">An [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that represents the network adapter to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e2d7-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e2d7-114">Return value</span></span>

<span data-ttu-id="4e2d7-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="4e2d7-115">This method can return one of these values.</span></span>



| <span data-ttu-id="4e2d7-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="4e2d7-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="4e2d7-117">Описание</span><span class="sxs-lookup"><span data-stu-id="4e2d7-117">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="4e2d7-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4e2d7-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="4e2d7-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4e2d7-119">The operation was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="4e2d7-120"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="4e2d7-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="4e2d7-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="4e2d7-121">The parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="4e2d7-122"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4e2d7-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="4e2d7-123">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="4e2d7-123">The configuration is unknown.</span></span><br/>                       |
| <dl> <span data-ttu-id="4e2d7-124"><dt>**Виртуальная машина \_ \_Виртуальная машина \_ с установленным \_ или \_ сохраненным**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="4e2d7-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="4e2d7-125">Виртуальная машина находится в работающем или сохраненном состоянии.</span><span class="sxs-lookup"><span data-stu-id="4e2d7-125">The virtual machine is in a running or saved state.</span></span><br/> |
| <dl> <span data-ttu-id="4e2d7-126"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="4e2d7-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="4e2d7-127">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="4e2d7-127">An unexpected error has occurred.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="4e2d7-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e2d7-128">Remarks</span></span>

<span data-ttu-id="4e2d7-129">Удалить существующий сетевой интерфейс можно только с остановленной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4e2d7-129">You can only remove an existing network interface from a virtual machine that is stopped.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e2d7-130">Требования</span><span class="sxs-lookup"><span data-stu-id="4e2d7-130">Requirements</span></span>



| <span data-ttu-id="4e2d7-131">Требование</span><span class="sxs-lookup"><span data-stu-id="4e2d7-131">Requirement</span></span> | <span data-ttu-id="4e2d7-132">Значение</span><span class="sxs-lookup"><span data-stu-id="4e2d7-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e2d7-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e2d7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4e2d7-134">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4e2d7-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4e2d7-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e2d7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4e2d7-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4e2d7-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4e2d7-137">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4e2d7-137">End of client support</span></span><br/>    | <span data-ttu-id="4e2d7-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4e2d7-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4e2d7-139">Продукт</span><span class="sxs-lookup"><span data-stu-id="4e2d7-139">Product</span></span><br/>                  | <span data-ttu-id="4e2d7-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4e2d7-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4e2d7-141">Header</span><span class="sxs-lookup"><span data-stu-id="4e2d7-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e2d7-142"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e2d7-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4e2d7-143">IID</span><span class="sxs-lookup"><span data-stu-id="4e2d7-143">IID</span></span><br/>                      | <span data-ttu-id="4e2d7-144">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="4e2d7-144">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="4e2d7-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e2d7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e2d7-146">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="4e2d7-146">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

