---
title: Метод Ивмвиртуалмачине AddHardDiskConnection (Впккоминтерфацес. h)
description: Добавляет новое подключение жесткого диска к виртуальной машине.
ms.assetid: 0f4e0666-2cfd-4c73-884d-6f8b43186c05
keywords:
- Метод AddHardDiskConnection Virtual PC
- Метод AddHardDiskConnection Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод AddHardDiskConnection
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0111577fd5cab614988e7295f3b8cdd59b8805c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650378"
---
# <a name="ivmvirtualmachineaddharddiskconnection-method"></a><span data-ttu-id="657dc-106">Метод Ивмвиртуалмачине:: AddHardDiskConnection</span><span class="sxs-lookup"><span data-stu-id="657dc-106">IVMVirtualMachine::AddHardDiskConnection method</span></span>

<span data-ttu-id="657dc-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="657dc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="657dc-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="657dc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="657dc-109">Добавляет новое подключение жесткого диска к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="657dc-109">Adds a new hard disk connection to the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="657dc-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="657dc-110">Syntax</span></span>


```C++
HRESULT AddHardDiskConnection(
  [in]          BSTR                  hardDiskPath,
  [in]          long                  busNumber,
  [in]          long                  deviceNumber,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="parameters"></a><span data-ttu-id="657dc-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="657dc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="657dc-112">*харддискпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="657dc-112">*hardDiskPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="657dc-113">Полный путь к файлу виртуального жесткого диска (VHD) для подключения.</span><span class="sxs-lookup"><span data-stu-id="657dc-113">The full path of the virtual hard disk (VHD) file to connect.</span></span>

</dd> <dt>

<span data-ttu-id="657dc-114">*буснумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="657dc-114">*busNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="657dc-115">Шина, к которой будет подключен диск.</span><span class="sxs-lookup"><span data-stu-id="657dc-115">The bus to which the drive will be attached.</span></span>



| <span data-ttu-id="657dc-116">Значение</span><span class="sxs-lookup"><span data-stu-id="657dc-116">Value</span></span>                                                                        | <span data-ttu-id="657dc-117">Значение</span><span class="sxs-lookup"><span data-stu-id="657dc-117">Meaning</span></span>                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="657dc-118"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="657dc-118"><dt>0</dt></span></span> </dl> | <span data-ttu-id="657dc-119">Диск будет подключен к первой шине.</span><span class="sxs-lookup"><span data-stu-id="657dc-119">The drive will be attached to the first bus.</span></span><br/>  |
| <dl> <span data-ttu-id="657dc-120"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="657dc-120"><dt>1</dt></span></span> </dl> | <span data-ttu-id="657dc-121">Диск будет подключен к второй шине.</span><span class="sxs-lookup"><span data-stu-id="657dc-121">The drive will be attached to the second bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="657dc-122">*девиценумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="657dc-122">*deviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="657dc-123">Устройство, к которому будет подключен диск.</span><span class="sxs-lookup"><span data-stu-id="657dc-123">The device to which the drive will be attached.</span></span>



| <span data-ttu-id="657dc-124">Значение</span><span class="sxs-lookup"><span data-stu-id="657dc-124">Value</span></span>                                                                        | <span data-ttu-id="657dc-125">Значение</span><span class="sxs-lookup"><span data-stu-id="657dc-125">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="657dc-126"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="657dc-126"><dt>0</dt></span></span> </dl> | <span data-ttu-id="657dc-127">Диск будет подключен к первому устройству на шине.</span><span class="sxs-lookup"><span data-stu-id="657dc-127">The drive will be attached to the first device on the bus.</span></span><br/>  |
| <dl> <span data-ttu-id="657dc-128"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="657dc-128"><dt>1</dt></span></span> </dl> | <span data-ttu-id="657dc-129">Диск будет подключен ко второму устройству на шине.</span><span class="sxs-lookup"><span data-stu-id="657dc-129">The drive will be attached to the second device on the bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="657dc-130">*харддискконнектион* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="657dc-130">*hardDiskConnection* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="657dc-131">Объект [**ивмхарддискконнектион**](ivmharddiskconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="657dc-131">An [**IVMHardDiskConnection**](ivmharddiskconnection.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="657dc-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="657dc-132">Return value</span></span>

<span data-ttu-id="657dc-133">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="657dc-133">This method can return one of these values.</span></span>



| <span data-ttu-id="657dc-134">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="657dc-134">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="657dc-135">Описание</span><span class="sxs-lookup"><span data-stu-id="657dc-135">Description</span></span>                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="657dc-136"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="657dc-136"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="657dc-137">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="657dc-137">The operation was successful.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="657dc-138"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="657dc-138"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="657dc-139">Параметр *харддискконнектион* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="657dc-139">The *hardDiskConnection* parameter is **NULL**.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="657dc-140"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="657dc-140"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                   | <span data-ttu-id="657dc-141">Параметр *харддискпас* имеет **значение NULL** , или параметр *буснумбер* или *девиценумбер* является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="657dc-141">A *hardDiskPath* parameter is **NULL** or the *busNumber* or *deviceNumber* parameter is not valid.</span></span><br/>                                            |
| <dl> <span data-ttu-id="657dc-142"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ файл ошибки \_ не \_ найден)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="657dc-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl>   | <span data-ttu-id="657dc-143">Системе не удается найти файл, указанный параметром *харддискпас* .</span><span class="sxs-lookup"><span data-stu-id="657dc-143">The system cannot find the file specified by the *hardDiskPath* parameter.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="657dc-144"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ путь ошибки \_ не \_ найден)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="657dc-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl>   | <span data-ttu-id="657dc-145">Системе не удается найти путь, указанный параметром *харддискпас* .</span><span class="sxs-lookup"><span data-stu-id="657dc-145">The system cannot find the path specified by the *hardDiskPath* parameter.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="657dc-146"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ недопустимое \_ имя)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="657dc-146"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>      | <span data-ttu-id="657dc-147">Параметр *харддискпас* содержит недопустимый символ (один из " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="657dc-147">The *hardDiskPath* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                                        |
| <dl> <span data-ttu-id="657dc-148"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ Bad \_ PATHNAME)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="657dc-148"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>      | <span data-ttu-id="657dc-149">Параметр *харддискпас* указывает пустой или относительный путь.</span><span class="sxs-lookup"><span data-stu-id="657dc-149">The *hardDiskPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="657dc-150">Требуется абсолютный путь.</span><span class="sxs-lookup"><span data-stu-id="657dc-150">An absolute path is required.</span></span><br/>                                                |
| <dl> <span data-ttu-id="657dc-151"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ \_ переполнение буфера ошибки)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="657dc-151"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl>   | <span data-ttu-id="657dc-152">Путь, указанный в параметре *харддискпас* , слишком длинный.</span><span class="sxs-lookup"><span data-stu-id="657dc-152">The path specified by the *hardDiskPath* parameter is too long.</span></span> <span data-ttu-id="657dc-153">Длина пути должна быть меньше 260 символов.</span><span class="sxs-lookup"><span data-stu-id="657dc-153">The path must be less than 260 characters.</span></span><br/>                                     |
| <dl> <span data-ttu-id="657dc-154"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="657dc-154"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                              | <span data-ttu-id="657dc-155">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="657dc-155">The configuration is unknown.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="657dc-156"><dt>**Виртуальная машина \_ \_Виртуальная машина \_ с установленным \_ или \_ сохраненным**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="657dc-156"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl>                   | <span data-ttu-id="657dc-157">Виртуальная машина находится в работающем или сохраненном состоянии.</span><span class="sxs-lookup"><span data-stu-id="657dc-157">The VM is in a running or saved state.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="657dc-158"><dt>**Виртуальная машина \_ \_Шина диска \_ E \_ \_ с \_ помощью**</dt> <dt>0xA00400503</dt></span><span class="sxs-lookup"><span data-stu-id="657dc-158"><dt>**VM\_E\_DRIVE\_BUS\_LOC\_IN\_USE**</dt> <dt>0xA00400503</dt></span></span> </dl>                | <span data-ttu-id="657dc-159">Указанное расположение шины используется.</span><span class="sxs-lookup"><span data-stu-id="657dc-159">The specified bus location is in use.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="657dc-160"><dt>**Виртуальная машина \_ E \_ Недопустимый \_ \_ файл HD**</dt> <dt>0xA0040682</dt></span><span class="sxs-lookup"><span data-stu-id="657dc-160"><dt>**VM\_E\_INVALID\_HD\_FILE**</dt> <dt>0xA0040682</dt></span></span> </dl>                        | <span data-ttu-id="657dc-161">Размер VHD превышает 127 Гб и не может быть подключен к шине IDE.</span><span class="sxs-lookup"><span data-stu-id="657dc-161">The VHD is greater than 127 GB and cannot be connected to the IDE bus.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="657dc-162"><dt>**Виртуальная машина \_ E \_ НЕподдерживаемый \_ \_ \_ Тип HD**</dt> <dt>0xA00400686</dt></span><span class="sxs-lookup"><span data-stu-id="657dc-162"><dt>**VM\_E\_UNSUPPORTED\_HD\_DISK\_TYPE**</dt> <dt>0xA00400686</dt></span></span> </dl>             | <span data-ttu-id="657dc-163">Параметр *харддискпас* относится к связанному виртуальному жесткому диску или разностному виртуальному жесткому диску с связанным VHD.</span><span class="sxs-lookup"><span data-stu-id="657dc-163">The *hardDiskPath* parameter refers to a linked VHD or a differencing VHD to a linked VHD.</span></span> <span data-ttu-id="657dc-164">Связанные VHD не могут быть подключены к виртуальным машинам.</span><span class="sxs-lookup"><span data-stu-id="657dc-164">Linked VHDs cannot be attached to virtual machines.</span></span><br/> |
| <dl> <span data-ttu-id="657dc-165"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ \_ нарушение общего доступа к ошибкам)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="657dc-165"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="657dc-166">Указанный виртуальный жесткий диск уже подключен к другому расположению шины для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="657dc-166">The specified VHD is already connected to another bus location for this VM.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="657dc-167"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="657dc-167"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="657dc-168">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="657dc-168">An unexpected error has occurred.</span></span><br/>                                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="657dc-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="657dc-169">Remarks</span></span>

<span data-ttu-id="657dc-170">Можно добавить только новое подключение жесткого диска к остановленной виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="657dc-170">You can only add a new hard disk connection to a stopped virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="657dc-171">Требования</span><span class="sxs-lookup"><span data-stu-id="657dc-171">Requirements</span></span>



| <span data-ttu-id="657dc-172">Требование</span><span class="sxs-lookup"><span data-stu-id="657dc-172">Requirement</span></span> | <span data-ttu-id="657dc-173">Значение</span><span class="sxs-lookup"><span data-stu-id="657dc-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="657dc-174">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="657dc-174">Minimum supported client</span></span><br/> | <span data-ttu-id="657dc-175">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="657dc-175">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="657dc-176">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="657dc-176">Minimum supported server</span></span><br/> | <span data-ttu-id="657dc-177">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="657dc-177">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="657dc-178">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="657dc-178">End of client support</span></span><br/>    | <span data-ttu-id="657dc-179">Windows 7</span><span class="sxs-lookup"><span data-stu-id="657dc-179">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="657dc-180">Продукт</span><span class="sxs-lookup"><span data-stu-id="657dc-180">Product</span></span><br/>                  | <span data-ttu-id="657dc-181">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="657dc-181">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="657dc-182">Header</span><span class="sxs-lookup"><span data-stu-id="657dc-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="657dc-183"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="657dc-183"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="657dc-184">IID</span><span class="sxs-lookup"><span data-stu-id="657dc-184">IID</span></span><br/>                      | <span data-ttu-id="657dc-185">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="657dc-185">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="657dc-186">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="657dc-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="657dc-187">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="657dc-187">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

