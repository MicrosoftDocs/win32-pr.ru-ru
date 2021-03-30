---
title: Метод Ивмвиртуалпк Финдвиртуалмачине (Впккоминтерфацес. h)
description: Извлекает объект виртуальной машины, соответствующий запрошенной конфигурации.
ms.assetid: 1c73d6f7-5662-485e-a864-e8e48197f8e4
keywords:
- Метод Финдвиртуалмачине Virtual PC
- Метод Финдвиртуалмачине Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, метод Финдвиртуалмачине
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e5702738e16fa7b4f4a263264b0574966d1fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136914"
---
# <a name="ivmvirtualpcfindvirtualmachine-method"></a><span data-ttu-id="e0aa6-106">Метод Ивмвиртуалпк:: Финдвиртуалмачине</span><span class="sxs-lookup"><span data-stu-id="e0aa6-106">IVMVirtualPC::FindVirtualMachine method</span></span>

<span data-ttu-id="e0aa6-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e0aa6-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e0aa6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e0aa6-109">Извлекает объект виртуальной машины, соответствующий запрошенной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-109">Retrieves a virtual machine object that matches the requested configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0aa6-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0aa6-110">Syntax</span></span>


```C++
HRESULT FindVirtualMachine(
  [in]          BSTR              configurationName,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="e0aa6-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="e0aa6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0aa6-112">*configurationName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e0aa6-112">*configurationName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0aa6-113">Имя виртуальной машины, которую нужно найти.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-113">The name of the virtual machine to be found.</span></span>

</dd> <dt>

<span data-ttu-id="e0aa6-114">*virtualMachine* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e0aa6-114">*virtualMachine* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e0aa6-115">Указатель на новый объект [**ивмвиртуалмачине**](ivmvirtualmachine.md) , представляющий эту виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-115">A pointer to a new [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents this virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0aa6-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e0aa6-116">Return value</span></span>

<span data-ttu-id="e0aa6-117">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-117">This method can return one of these values.</span></span>



| <span data-ttu-id="e0aa6-118">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="e0aa6-118">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="e0aa6-119">Описание</span><span class="sxs-lookup"><span data-stu-id="e0aa6-119">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e0aa6-120"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e0aa6-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="e0aa6-121">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-121">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e0aa6-122"><dt>**С \_ ЛОЖЬ**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e0aa6-122"><dt>**S\_FALSE**</dt> <dt>1</dt></span></span> </dl>                                           | <span data-ttu-id="e0aa6-123">Не удалось найти указанную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-123">The specified configuration could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="e0aa6-124"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="e0aa6-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="e0aa6-125">Параметр *configurationName* недопустим, или *VirtualMachine* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-125">The *configurationName* parameter is invalid, or *virtualMachine* is **NULL**.</span></span><br/>       |
| <dl> <span data-ttu-id="e0aa6-126"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e0aa6-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="e0aa6-127">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-127">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="e0aa6-128"><dt>**Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="e0aa6-128"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="e0aa6-129">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="e0aa6-129">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e0aa6-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0aa6-130">Remarks</span></span>

<span data-ttu-id="e0aa6-131">В именах виртуальных машин не учитывается регистр, например "MyVM" и "MyVM" ссылаются на одну и ту же виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-131">Virtual machine names are case-insensitive, for example, "MyVM" and "myvm" refer to the same virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0aa6-132">Требования</span><span class="sxs-lookup"><span data-stu-id="e0aa6-132">Requirements</span></span>



| <span data-ttu-id="e0aa6-133">Требование</span><span class="sxs-lookup"><span data-stu-id="e0aa6-133">Requirement</span></span> | <span data-ttu-id="e0aa6-134">Значение</span><span class="sxs-lookup"><span data-stu-id="e0aa6-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0aa6-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e0aa6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e0aa6-136">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e0aa6-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e0aa6-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e0aa6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e0aa6-138">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e0aa6-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e0aa6-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e0aa6-139">End of client support</span></span><br/>    | <span data-ttu-id="e0aa6-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e0aa6-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e0aa6-141">Продукт</span><span class="sxs-lookup"><span data-stu-id="e0aa6-141">Product</span></span><br/>                  | <span data-ttu-id="e0aa6-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e0aa6-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e0aa6-143">Header</span><span class="sxs-lookup"><span data-stu-id="e0aa6-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0aa6-144"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0aa6-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e0aa6-145">IID</span><span class="sxs-lookup"><span data-stu-id="e0aa6-145">IID</span></span><br/>                      | <span data-ttu-id="e0aa6-146">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="e0aa6-146">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e0aa6-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0aa6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0aa6-148">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="e0aa6-148">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

