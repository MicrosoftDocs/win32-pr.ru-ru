---
title: Метод Ивмвиртуалмачине Адддвдромдриве (Впккоминтерфацес. h)
description: Добавляет новый компакт-диск или DVD-дисковод в виртуальную машину.
ms.assetid: d39f2728-6146-42ed-b67f-6586566a7209
keywords:
- Метод Адддвдромдриве Virtual PC
- Метод Адддвдромдриве Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Адддвдромдриве
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7acbe70f6b338b3490c12ab67bcdfdc997d90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691860"
---
# <a name="ivmvirtualmachineadddvdromdrive-method"></a><span data-ttu-id="188e2-106">Метод Ивмвиртуалмачине:: Адддвдромдриве</span><span class="sxs-lookup"><span data-stu-id="188e2-106">IVMVirtualMachine::AddDVDROMDrive method</span></span>

<span data-ttu-id="188e2-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="188e2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="188e2-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="188e2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="188e2-109">Добавляет новый компакт-диск или DVD-дисковод в виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="188e2-109">Adds a new CD or DVD drive to the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="188e2-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="188e2-110">Syntax</span></span>


```C++
HRESULT AddDVDROMDrive(
  [in]          long        busNumber,
  [in]          long        deviceNumber,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="parameters"></a><span data-ttu-id="188e2-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="188e2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="188e2-112">*буснумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="188e2-112">*busNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="188e2-113">Шина, к которой будет подключен диск.</span><span class="sxs-lookup"><span data-stu-id="188e2-113">The bus to which the drive will be attached.</span></span>



| <span data-ttu-id="188e2-114">Значение</span><span class="sxs-lookup"><span data-stu-id="188e2-114">Value</span></span>                                                                        | <span data-ttu-id="188e2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="188e2-115">Meaning</span></span>                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="188e2-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="188e2-116"><dt>0</dt></span></span> </dl> | <span data-ttu-id="188e2-117">Диск будет подключен к первой шине.</span><span class="sxs-lookup"><span data-stu-id="188e2-117">The drive will be attached to the first bus.</span></span><br/>  |
| <dl> <span data-ttu-id="188e2-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="188e2-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="188e2-119">Диск будет подключен к второй шине.</span><span class="sxs-lookup"><span data-stu-id="188e2-119">The drive will be attached to the second bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="188e2-120">*девиценумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="188e2-120">*deviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="188e2-121">Устройство, к которому будет подключен диск.</span><span class="sxs-lookup"><span data-stu-id="188e2-121">The device to which the drive will be attached.</span></span>



| <span data-ttu-id="188e2-122">Значение</span><span class="sxs-lookup"><span data-stu-id="188e2-122">Value</span></span>                                                                        | <span data-ttu-id="188e2-123">Значение</span><span class="sxs-lookup"><span data-stu-id="188e2-123">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="188e2-124"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="188e2-124"><dt>0</dt></span></span> </dl> | <span data-ttu-id="188e2-125">Диск будет подключен к первому устройству на шине.</span><span class="sxs-lookup"><span data-stu-id="188e2-125">The drive will be attached to the first device on the bus.</span></span><br/>  |
| <dl> <span data-ttu-id="188e2-126"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="188e2-126"><dt>1</dt></span></span> </dl> | <span data-ttu-id="188e2-127">Диск будет подключен ко второму устройству на шине.</span><span class="sxs-lookup"><span data-stu-id="188e2-127">The drive will be attached to the second device on the bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="188e2-128">*двддриве* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="188e2-128">*dvdDrive* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="188e2-129">Объект [**ивмдвддриве**](ivmdvddrive.md) .</span><span class="sxs-lookup"><span data-stu-id="188e2-129">An [**IVMDVDDrive**](ivmdvddrive.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="188e2-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="188e2-130">Return value</span></span>

<span data-ttu-id="188e2-131">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="188e2-131">This method can return one of these values.</span></span>



| <span data-ttu-id="188e2-132">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="188e2-132">Return code/value</span></span>                                                                                                                                                               | <span data-ttu-id="188e2-133">Описание</span><span class="sxs-lookup"><span data-stu-id="188e2-133">Description</span></span>                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="188e2-134"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="188e2-134"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                     | <span data-ttu-id="188e2-135">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="188e2-135">The operation was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="188e2-136"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="188e2-136"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                       | <span data-ttu-id="188e2-137">Параметр *двддриве* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="188e2-137">The *dvdDrive* parameter is **NULL**.</span></span><br/>               |
| <dl> <span data-ttu-id="188e2-138"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="188e2-138"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                    | <span data-ttu-id="188e2-139">Недействительный параметр.</span><span class="sxs-lookup"><span data-stu-id="188e2-139">A parameter is not valid.</span></span><br/>                           |
| <dl> <span data-ttu-id="188e2-140"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="188e2-140"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>               | <span data-ttu-id="188e2-141">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="188e2-141">The configuration is unknown.</span></span><br/>                       |
| <dl> <span data-ttu-id="188e2-142"><dt>**Виртуальная машина \_ \_Виртуальная машина \_ с установленным \_ или \_ сохраненным**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="188e2-142"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl>    | <span data-ttu-id="188e2-143">Виртуальная машина находится в работающем или сохраненном состоянии.</span><span class="sxs-lookup"><span data-stu-id="188e2-143">The virtual machine is in a running or saved state.</span></span><br/> |
| <dl> <span data-ttu-id="188e2-144"><dt>**Виртуальная машина \_ \_Шина диска \_ E \_ \_ с \_ помощью**</dt> <dt>0xA00400503</dt></span><span class="sxs-lookup"><span data-stu-id="188e2-144"><dt>**VM\_E\_DRIVE\_BUS\_LOC\_IN\_USE**</dt> <dt>0xA00400503</dt></span></span> </dl> | <span data-ttu-id="188e2-145">Указанное расположение шины используется.</span><span class="sxs-lookup"><span data-stu-id="188e2-145">The specified bus location is in use.</span></span><br/>               |
| <dl> <span data-ttu-id="188e2-146"><dt>**Виртуальная машина \_ \_Диск E \_ Недопустимый**</dt> <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="188e2-146"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>            | <span data-ttu-id="188e2-147">Указан недопустимый диск.</span><span class="sxs-lookup"><span data-stu-id="188e2-147">The drive specified is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="188e2-148"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="188e2-148"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>               | <span data-ttu-id="188e2-149">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="188e2-149">An unexpected error has occurred.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="188e2-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="188e2-150">Remarks</span></span>

<span data-ttu-id="188e2-151">В остановленную виртуальную машину можно добавить только новый компакт-диск или DVD-дисковод.</span><span class="sxs-lookup"><span data-stu-id="188e2-151">You can only add a new CD or DVD drive to a stopped virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="188e2-152">Требования</span><span class="sxs-lookup"><span data-stu-id="188e2-152">Requirements</span></span>



| <span data-ttu-id="188e2-153">Требование</span><span class="sxs-lookup"><span data-stu-id="188e2-153">Requirement</span></span> | <span data-ttu-id="188e2-154">Значение</span><span class="sxs-lookup"><span data-stu-id="188e2-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="188e2-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="188e2-155">Minimum supported client</span></span><br/> | <span data-ttu-id="188e2-156">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="188e2-156">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="188e2-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="188e2-157">Minimum supported server</span></span><br/> | <span data-ttu-id="188e2-158">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="188e2-158">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="188e2-159">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="188e2-159">End of client support</span></span><br/>    | <span data-ttu-id="188e2-160">Windows 7</span><span class="sxs-lookup"><span data-stu-id="188e2-160">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="188e2-161">Продукт</span><span class="sxs-lookup"><span data-stu-id="188e2-161">Product</span></span><br/>                  | <span data-ttu-id="188e2-162">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="188e2-162">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="188e2-163">Header</span><span class="sxs-lookup"><span data-stu-id="188e2-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="188e2-164"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="188e2-164"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="188e2-165">IID</span><span class="sxs-lookup"><span data-stu-id="188e2-165">IID</span></span><br/>                      | <span data-ttu-id="188e2-166">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="188e2-166">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="188e2-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="188e2-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="188e2-168">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="188e2-168">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

