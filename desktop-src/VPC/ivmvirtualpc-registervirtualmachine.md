---
title: Метод Ивмвиртуалпк Регистервиртуалмачине (Впккоминтерфацес. h)
description: Регистрирует существующую конфигурацию виртуальной машины и извлекает объект виртуальной машины.
ms.assetid: d3b13f1b-7537-4e3f-9bcc-98a6fe855f78
keywords:
- Метод Регистервиртуалмачине Virtual PC
- Метод Регистервиртуалмачине Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, метод Регистервиртуалмачине
topic_type:
- apiref
api_name:
- IVMVirtualPC.RegisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cc1e27a657eaad70aeec81c0216d1e707fa36b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691919"
---
# <a name="ivmvirtualpcregistervirtualmachine-method"></a><span data-ttu-id="bbea4-106">Метод Ивмвиртуалпк:: Регистервиртуалмачине</span><span class="sxs-lookup"><span data-stu-id="bbea4-106">IVMVirtualPC::RegisterVirtualMachine method</span></span>

<span data-ttu-id="bbea4-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bbea4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bbea4-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bbea4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bbea4-109">Регистрирует существующую конфигурацию виртуальной машины и извлекает объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bbea4-109">Registers an existing virtual machine configuration and retrieves the virtual machine object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbea4-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bbea4-110">Syntax</span></span>


```C++
HRESULT RegisterVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="bbea4-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="bbea4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbea4-112">*configurationName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bbea4-112">*configurationName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbea4-113">Имя регистрируемой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bbea4-113">The name of the virtual machine to be registered.</span></span> <span data-ttu-id="bbea4-114">Длина имени не может превышать 80 символов, а общая длина имени и пути не может превышать **максимальный \_ путь** (260) символов.</span><span class="sxs-lookup"><span data-stu-id="bbea4-114">The length of the name cannot exceed 80 characters and the combined length of the name and path cannot exceed **MAX\_PATH** (260) characters.</span></span> <span data-ttu-id="bbea4-115">Указанное имя может содержать расширение VMC.</span><span class="sxs-lookup"><span data-stu-id="bbea4-115">The specified name may contain the .vmc extension.</span></span> <span data-ttu-id="bbea4-116">Если этот параметр имеет **значение NULL** или является пустой строкой, параметр *configurationPath* должен указывать полный путь к файлу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bbea4-116">If this parameter is **NULL** or an empty string, the *configurationPath* parameter must specify the full path to the configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="bbea4-117">*configurationPath* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bbea4-117">*configurationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbea4-118">Путь к папке, содержащей существующий файл конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bbea4-118">The path to the folder that contains the existing configuration file.</span></span> <span data-ttu-id="bbea4-119">Если параметр *configurationName* имеет **значение NULL** или является пустой строкой, он должен указывать полный путь к существующему файлу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bbea4-119">If the *configurationName* parameter is **NULL** or an empty string, this must specify the full path to the existing configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="bbea4-120">*virtualMachine* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="bbea4-120">*virtualMachine* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="bbea4-121">Указатель на новый объект [**ивмвиртуалмачине**](ivmvirtualmachine.md) , представляющий эту виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="bbea4-121">A pointer to a new [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents this virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbea4-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bbea4-122">Return value</span></span>

<span data-ttu-id="bbea4-123">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="bbea4-123">This method can return one of these values.</span></span>



| <span data-ttu-id="bbea4-124">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="bbea4-124">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="bbea4-125">Описание</span><span class="sxs-lookup"><span data-stu-id="bbea4-125">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bbea4-126"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bbea4-126"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="bbea4-127">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="bbea4-127">The operation was successful.</span></span><br/>                                                                                                                                                                          |
| <dl> <span data-ttu-id="bbea4-128"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="bbea4-128"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="bbea4-129">Недопустимый параметр *configurationName* или *ConfigurationPath* , или *virtualMachine* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="bbea4-129">The *configurationName* or *configurationPath* parameter is invalid, or *virtualMachine* is **NULL**.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="bbea4-130"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ путь ошибки \_ не \_ найден)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="bbea4-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="bbea4-131">Системе не удается найти путь, указанный параметрами *configurationName* и *configurationPath* .</span><span class="sxs-lookup"><span data-stu-id="bbea4-131">The system cannot find the path specified by the *configurationName* and *configurationPath* parameters.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="bbea4-132"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ файл ошибки \_ не \_ найден)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="bbea4-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="bbea4-133">Системе не удается найти файл, указанный параметрами *configurationName* и *configurationPath* .</span><span class="sxs-lookup"><span data-stu-id="bbea4-133">The system cannot find the file specified by the *configurationName* and *configurationPath* parameters.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="bbea4-134"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ недопустимое \_ имя)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="bbea4-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="bbea4-135">Параметр *configurationPath* содержит недопустимый символ (один из " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="bbea4-135">The *configurationPath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="bbea4-136"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ Bad \_ PATHNAME)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="bbea4-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="bbea4-137">Параметр *configurationPath* указывает пустой или относительный путь.</span><span class="sxs-lookup"><span data-stu-id="bbea4-137">The parameter *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="bbea4-138">Требуется абсолютный путь.</span><span class="sxs-lookup"><span data-stu-id="bbea4-138">An absolute path is required.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="bbea4-139"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ \_ переполнение буфера ошибки)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="bbea4-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="bbea4-140">Путь, указанный в параметрах *configurationName* и *configurationPath* , приводит к слишком длинному пути.</span><span class="sxs-lookup"><span data-stu-id="bbea4-140">The path specified by the *configurationName* and *configurationPath* parameters results in a path that is too long.</span></span> <span data-ttu-id="bbea4-141">Общая длина пути должна быть меньше **максимального \_ пути** (260) символов.</span><span class="sxs-lookup"><span data-stu-id="bbea4-141">The combined length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="bbea4-142"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ уже \_ существует)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="bbea4-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="bbea4-143">Файл конфигурации с таким именем уже существует в этом расположении.</span><span class="sxs-lookup"><span data-stu-id="bbea4-143">A configuration file with this name already exists at this location.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="bbea4-144"><dt>**Виртуальная машина \_ \_Имя конфигурации \_ E \_ слишком \_ длинное**</dt> <dt>0xA0040401</dt></span><span class="sxs-lookup"><span data-stu-id="bbea4-144"><dt>**VM\_E\_CONFIG\_NAME\_TOO\_LONG**</dt> <dt>0xA0040401</dt></span></span> </dl>                | <span data-ttu-id="bbea4-145">Длина параметра *configurationName* превышает 80 символов.</span><span class="sxs-lookup"><span data-stu-id="bbea4-145">The *configurationName* parameter exceeds 80 characters in length.</span></span><br/>                                                                                                                                     |
| <dl> <span data-ttu-id="bbea4-146"><dt>**Виртуальная машина \_ \_Имя конфигурации \_ E \_ недопустимо \_ char**</dt> <dt>0xA0040402</dt></span><span class="sxs-lookup"><span data-stu-id="bbea4-146"><dt>**VM\_E\_CONFIG\_NAME\_INVALID\_CHAR**</dt> <dt>0xA0040402</dt></span></span> </dl>            | <span data-ttu-id="bbea4-147">Параметр *configurationName* содержит недопустимый символ (один из " \* ?: <>/ \| \\ " ").</span><span class="sxs-lookup"><span data-stu-id="bbea4-147">The *configurationName* parameter contains an invalid character (one of "\*?:<>/\|\\"").</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="bbea4-148"><dt>**Виртуальная машина \_ E \_ Конфигурация \_ дублирует \_ имя**</dt> <dt>0xA0040403</dt></span><span class="sxs-lookup"><span data-stu-id="bbea4-148"><dt>**VM\_E\_CONFIG\_DUPLICATE\_NAME**</dt> <dt>0xA0040403</dt></span></span> </dl>                | <span data-ttu-id="bbea4-149">Виртуальная машина с таким именем уже существует.</span><span class="sxs-lookup"><span data-stu-id="bbea4-149">There is already a virtual machine with this name.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="bbea4-150"><dt>**Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="bbea4-150"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="bbea4-151">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="bbea4-151">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="bbea4-152"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="bbea4-152"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="bbea4-153">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="bbea4-153">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="bbea4-154">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bbea4-154">Remarks</span></span>

<span data-ttu-id="bbea4-155">В именах виртуальных машин не учитывается регистр, например "MyVM" и "MyVM" ссылаются на одну и ту же виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="bbea4-155">Virtual machine names are case-insensitive, for example, "MyVM" and "myvm" refer to the same virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbea4-156">Требования</span><span class="sxs-lookup"><span data-stu-id="bbea4-156">Requirements</span></span>



| <span data-ttu-id="bbea4-157">Требование</span><span class="sxs-lookup"><span data-stu-id="bbea4-157">Requirement</span></span> | <span data-ttu-id="bbea4-158">Значение</span><span class="sxs-lookup"><span data-stu-id="bbea4-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbea4-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bbea4-159">Minimum supported client</span></span><br/> | <span data-ttu-id="bbea4-160">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bbea4-160">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bbea4-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bbea4-161">Minimum supported server</span></span><br/> | <span data-ttu-id="bbea4-162">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bbea4-162">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bbea4-163">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="bbea4-163">End of client support</span></span><br/>    | <span data-ttu-id="bbea4-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bbea4-164">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bbea4-165">Продукт</span><span class="sxs-lookup"><span data-stu-id="bbea4-165">Product</span></span><br/>                  | <span data-ttu-id="bbea4-166">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bbea4-166">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bbea4-167">Header</span><span class="sxs-lookup"><span data-stu-id="bbea4-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbea4-168"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbea4-168"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bbea4-169">IID</span><span class="sxs-lookup"><span data-stu-id="bbea4-169">IID</span></span><br/>                      | <span data-ttu-id="bbea4-170">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="bbea4-170">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="bbea4-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bbea4-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbea4-172">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="bbea4-172">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

