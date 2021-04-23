---
title: Метод Ивмвиртуалмачине Адднетворкадаптер (Впккоминтерфацес. h)
description: Добавляет сетевой интерфейс к виртуальной машине.
ms.assetid: 1fa39d2c-4a5a-42cb-afa4-520bf19b8cc8
keywords:
- Метод Адднетворкадаптер Virtual PC
- Метод Адднетворкадаптер Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Адднетворкадаптер
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d24351e5f5a32aff08e755329ac12baaaaf546
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691891"
---
# <a name="ivmvirtualmachineaddnetworkadapter-method"></a><span data-ttu-id="370e2-106">Метод Ивмвиртуалмачине:: Адднетворкадаптер</span><span class="sxs-lookup"><span data-stu-id="370e2-106">IVMVirtualMachine::AddNetworkAdapter method</span></span>

<span data-ttu-id="370e2-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="370e2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="370e2-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="370e2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="370e2-109">Добавляет сетевой интерфейс к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="370e2-109">Adds a network interface to the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="370e2-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="370e2-110">Syntax</span></span>


```C++
HRESULT AddNetworkAdapter(
  [out, retval] IVMNetworkAdapter **networkAdapter
);
```



## <a name="parameters"></a><span data-ttu-id="370e2-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="370e2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="370e2-112">*сетевого адаптера* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="370e2-112">*networkAdapter* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="370e2-113">Объект [**ивмнетворкадаптер**](ivmnetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="370e2-113">An [**IVMNetworkAdapter**](ivmnetworkadapter.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="370e2-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="370e2-114">Return value</span></span>

<span data-ttu-id="370e2-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="370e2-115">This method can return one of these values.</span></span>



| <span data-ttu-id="370e2-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="370e2-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="370e2-117">Описание</span><span class="sxs-lookup"><span data-stu-id="370e2-117">Description</span></span>                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="370e2-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="370e2-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="370e2-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="370e2-119">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="370e2-120"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="370e2-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="370e2-121">Параметр *сетевого адаптера* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="370e2-121">The *networkAdapter* parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="370e2-122"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="370e2-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="370e2-123">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="370e2-123">The configuration is unknown.</span></span><br/>                        |
| <dl> <span data-ttu-id="370e2-124"><dt>**Виртуальная машина \_ E \_ преф \_ недопустимое \_ значение**</dt> <dt>0xA0040301</dt></span><span class="sxs-lookup"><span data-stu-id="370e2-124"><dt>**VM\_E\_PREF\_ILLEGAL\_VALUE**</dt> <dt>0xA0040301</dt></span></span> </dl>   | <span data-ttu-id="370e2-125">Можно добавить не более четырех (4) сетевых адаптеров.</span><span class="sxs-lookup"><span data-stu-id="370e2-125">No more than four (4) network adapters can be added.</span></span><br/> |
| <dl> <span data-ttu-id="370e2-126"><dt>**Виртуальная машина \_ \_Виртуальная машина \_ с установленным \_ или \_ сохраненным**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="370e2-126"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="370e2-127">Виртуальная машина находится в работающем или сохраненном состоянии.</span><span class="sxs-lookup"><span data-stu-id="370e2-127">The virtual machine is in a running or saved state.</span></span><br/>  |
| <dl> <span data-ttu-id="370e2-128"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="370e2-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="370e2-129">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="370e2-129">An unexpected error has occurred.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="370e2-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="370e2-130">Remarks</span></span>

<span data-ttu-id="370e2-131">В остановленную виртуальную машину можно добавить только новый сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="370e2-131">You can only add a new network interface to a stopped virtual machine.</span></span> <span data-ttu-id="370e2-132">Созданный сетевой адаптер не подключен к виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="370e2-132">The newly created network adapter is not connected to a virtual network.</span></span>

## <a name="requirements"></a><span data-ttu-id="370e2-133">Требования</span><span class="sxs-lookup"><span data-stu-id="370e2-133">Requirements</span></span>



| <span data-ttu-id="370e2-134">Требование</span><span class="sxs-lookup"><span data-stu-id="370e2-134">Requirement</span></span> | <span data-ttu-id="370e2-135">Значение</span><span class="sxs-lookup"><span data-stu-id="370e2-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="370e2-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="370e2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="370e2-137">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="370e2-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="370e2-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="370e2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="370e2-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="370e2-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="370e2-140">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="370e2-140">End of client support</span></span><br/>    | <span data-ttu-id="370e2-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="370e2-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="370e2-142">Продукт</span><span class="sxs-lookup"><span data-stu-id="370e2-142">Product</span></span><br/>                  | <span data-ttu-id="370e2-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="370e2-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="370e2-144">Header</span><span class="sxs-lookup"><span data-stu-id="370e2-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="370e2-145"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="370e2-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="370e2-146">IID</span><span class="sxs-lookup"><span data-stu-id="370e2-146">IID</span></span><br/>                      | <span data-ttu-id="370e2-147">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="370e2-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="370e2-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="370e2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="370e2-149">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="370e2-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

