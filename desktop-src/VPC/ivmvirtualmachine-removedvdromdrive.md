---
title: Метод Ивмвиртуалмачине Ремоведвдромдриве (Впккоминтерфацес. h)
description: Удаляет указанный дисковод компакт-или DVD-дисков из виртуальной машины.
ms.assetid: 1c45c271-bead-41f6-8371-448d385a1288
keywords:
- Метод Ремоведвдромдриве Virtual PC
- Метод Ремоведвдромдриве Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Ремоведвдромдриве
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf0962b388c318d5abebdbd7a021a4466e644a28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136178"
---
# <a name="ivmvirtualmachineremovedvdromdrive-method"></a><span data-ttu-id="cc635-106">Метод Ивмвиртуалмачине:: Ремоведвдромдриве</span><span class="sxs-lookup"><span data-stu-id="cc635-106">IVMVirtualMachine::RemoveDVDROMDrive method</span></span>

<span data-ttu-id="cc635-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cc635-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cc635-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cc635-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cc635-109">Удаляет указанный дисковод компакт-или DVD-дисков из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cc635-109">Removes the specified CD or DVD drive from the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc635-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc635-110">Syntax</span></span>


```C++
HRESULT RemoveDVDROMDrive(
  [in] IVMDVDDrive *dvdDrive
);
```



## <a name="parameters"></a><span data-ttu-id="cc635-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc635-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc635-112">*двддриве* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc635-112">*dvdDrive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc635-113">Удаляемый диск.</span><span class="sxs-lookup"><span data-stu-id="cc635-113">The drive to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc635-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc635-114">Return value</span></span>

<span data-ttu-id="cc635-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="cc635-115">This method can return one of these values.</span></span>



| <span data-ttu-id="cc635-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="cc635-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="cc635-117">Описание</span><span class="sxs-lookup"><span data-stu-id="cc635-117">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="cc635-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cc635-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="cc635-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="cc635-119">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="cc635-120"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="cc635-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="cc635-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="cc635-121">The parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="cc635-122"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cc635-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="cc635-123">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="cc635-123">The configuration is unknown.</span></span><br/>                              |
| <dl> <span data-ttu-id="cc635-124"><dt>**Виртуальная машина \_ \_Виртуальная машина \_ с установленным \_ или \_ сохраненным**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="cc635-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="cc635-125">Виртуальная машина находится в работающем или сохраненном состоянии.</span><span class="sxs-lookup"><span data-stu-id="cc635-125">The virtual machine is in a running or saved state.</span></span><br/>        |
| <dl> <span data-ttu-id="cc635-126"><dt>**Виртуальная машина \_ \_Диск E \_ Недопустимый**</dt> <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="cc635-126"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>         | <span data-ttu-id="cc635-127">Указанный диск не подключен к этому расположению шины.</span><span class="sxs-lookup"><span data-stu-id="cc635-127">The drive specified is not connected to this bus location.</span></span><br/> |
| <dl> <span data-ttu-id="cc635-128"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="cc635-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="cc635-129">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="cc635-129">An unexpected error has occurred.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="cc635-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc635-130">Remarks</span></span>

<span data-ttu-id="cc635-131">Можно удалить только существующий компакт-диск или DVD-дисковод с остановленной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cc635-131">You can only remove an existing CD or DVD drive from a stopped virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc635-132">Требования</span><span class="sxs-lookup"><span data-stu-id="cc635-132">Requirements</span></span>



| <span data-ttu-id="cc635-133">Требование</span><span class="sxs-lookup"><span data-stu-id="cc635-133">Requirement</span></span> | <span data-ttu-id="cc635-134">Значение</span><span class="sxs-lookup"><span data-stu-id="cc635-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc635-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc635-135">Minimum supported client</span></span><br/> | <span data-ttu-id="cc635-136">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cc635-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cc635-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc635-137">Minimum supported server</span></span><br/> | <span data-ttu-id="cc635-138">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cc635-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cc635-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="cc635-139">End of client support</span></span><br/>    | <span data-ttu-id="cc635-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cc635-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cc635-141">Продукт</span><span class="sxs-lookup"><span data-stu-id="cc635-141">Product</span></span><br/>                  | <span data-ttu-id="cc635-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cc635-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cc635-143">Header</span><span class="sxs-lookup"><span data-stu-id="cc635-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc635-144"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc635-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cc635-145">IID</span><span class="sxs-lookup"><span data-stu-id="cc635-145">IID</span></span><br/>                      | <span data-ttu-id="cc635-146">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="cc635-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="cc635-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc635-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc635-148">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="cc635-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

