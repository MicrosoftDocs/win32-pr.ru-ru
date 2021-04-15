---
title: Метод Ивмвиртуалпк Креатевиртуалмачине (Впккоминтерфацес. h)
description: Создает новую конфигурацию виртуальной машины и извлекает объект виртуальной машины.
ms.assetid: 35f7364f-debd-4b9c-8240-23c0512eb004
keywords:
- Метод Креатевиртуалмачине Virtual PC
- Метод Креатевиртуалмачине Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, метод Креатевиртуалмачине
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 494d5166271e6c4086b8dfee12deb61e32ae8a18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492045"
---
# <a name="ivmvirtualpccreatevirtualmachine-method"></a><span data-ttu-id="67133-106">Метод Ивмвиртуалпк:: Креатевиртуалмачине</span><span class="sxs-lookup"><span data-stu-id="67133-106">IVMVirtualPC::CreateVirtualMachine method</span></span>

<span data-ttu-id="67133-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="67133-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="67133-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="67133-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="67133-109">Создает новую конфигурацию виртуальной машины и извлекает объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="67133-109">Creates a new virtual machine configuration and retrieves the virtual machine object.</span></span>

## <a name="syntax"></a><span data-ttu-id="67133-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67133-110">Syntax</span></span>


```C++
HRESULT CreateVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="67133-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="67133-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67133-112">*configurationName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="67133-112">*configurationName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67133-113">Имя создаваемой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="67133-113">The name of the virtual machine to be created.</span></span> <span data-ttu-id="67133-114">Длина имени не может превышать 80 символов, а общая длина имени и пути к файлам VMC и VMCX не может превышать **максимальную длину \_ пути** (260) символов.</span><span class="sxs-lookup"><span data-stu-id="67133-114">The length of the name cannot exceed 80 characters and the combined length of the name and path to VMC and VMCX files cannot exceed **MAX\_PATH** (260) characters.</span></span> <span data-ttu-id="67133-115">Файлы Extensions. VMC и. vmcx будут добавлены в конец имени виртуальной машины при создании файлов конфигурации.</span><span class="sxs-lookup"><span data-stu-id="67133-115">The file name extensions .vmc and .vmcx will be appended to the end of the virtual machine name when the configuration files are created.</span></span> <span data-ttu-id="67133-116">Если этот параметр имеет **значение NULL** или является пустой строкой, параметр *configurationPath* должен указывать полный путь к файлу VMC.</span><span class="sxs-lookup"><span data-stu-id="67133-116">If this parameter is **NULL** or an empty string, the *configurationPath* parameter must specify the full path to the VMC file.</span></span>

</dd> <dt>

<span data-ttu-id="67133-117">*configurationPath* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="67133-117">*configurationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67133-118">Путь к папке, в которой будет содержаться файл VMC.</span><span class="sxs-lookup"><span data-stu-id="67133-118">The path to the folder that will contain the VMC file.</span></span> <span data-ttu-id="67133-119">Если эта папка не существует, она будет создана.</span><span class="sxs-lookup"><span data-stu-id="67133-119">This folder will be created if it does not exist.</span></span> <span data-ttu-id="67133-120">Если *configurationName* имеет **значение NULL** или является пустой строкой, необходимо указать полный путь к новому файлу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="67133-120">If *configurationName* is **NULL** or an empty string, this must specify the full path of the new configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="67133-121">*virtualMachine* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="67133-121">*virtualMachine* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="67133-122">Указатель на новый объект [**ивмвиртуалмачине**](ivmvirtualmachine.md) , представляющий эту виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="67133-122">A pointer to a new [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents this virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67133-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="67133-123">Return value</span></span>

<span data-ttu-id="67133-124">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="67133-124">This method can return one of these values.</span></span>



| <span data-ttu-id="67133-125">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="67133-125">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="67133-126">Описание</span><span class="sxs-lookup"><span data-stu-id="67133-126">Description</span></span>                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="67133-127"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="67133-127"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="67133-128">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="67133-128">The operation was successful.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="67133-129"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="67133-129"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="67133-130">Недопустимый параметр *configurationName* или *configurationPath* , или параметр *virtualMachine* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="67133-130">The *configurationName* or *configurationPath* parameter is not valid, or the *virtualMachine* parameter is **NULL**.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="67133-131"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ путь ошибки \_ не \_ найден)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="67133-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="67133-132">Системе не удается найти путь, указанный параметром *configurationPath* .</span><span class="sxs-lookup"><span data-stu-id="67133-132">The system cannot find the path specified by the *configurationPath* parameter.</span></span><br/>                                                                                                                     |
| <dl> <span data-ttu-id="67133-133"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ недопустимое \_ имя)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="67133-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="67133-134">Параметр *configurationPath* содержит недопустимый символ (один из " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="67133-134">The *configurationPath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="67133-135"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ Bad \_ PATHNAME)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="67133-135"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="67133-136">Параметр *configurationPath* указывает пустой или относительный путь.</span><span class="sxs-lookup"><span data-stu-id="67133-136">The *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="67133-137">Требуется абсолютный путь.</span><span class="sxs-lookup"><span data-stu-id="67133-137">An absolute path is required.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="67133-138"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ \_ переполнение буфера ошибки)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="67133-138"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="67133-139">Путь, указанный в параметрах *configurationName* и *configurationPath* , приводит к слишком длинному пути.</span><span class="sxs-lookup"><span data-stu-id="67133-139">The path specified by the *configurationName* and *configurationPath* parameters results in a path that is too long.</span></span> <span data-ttu-id="67133-140">Общая длина пути должна быть меньше **максимального \_ пути** (260) символов.</span><span class="sxs-lookup"><span data-stu-id="67133-140">The total length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="67133-141"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ уже \_ существует)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="67133-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="67133-142">Файл конфигурации с таким именем уже существует в этом расположении.</span><span class="sxs-lookup"><span data-stu-id="67133-142">A configuration file with this name already exists at this location.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="67133-143"><dt>**Виртуальная машина \_ E \_ Конфигурация \_ без \_ имени**</dt> <dt>0xA0040400</dt></span><span class="sxs-lookup"><span data-stu-id="67133-143"><dt>**VM\_E\_CONFIG\_NO\_NAME**</dt> <dt>0xA0040400</dt></span></span> </dl>                       | <span data-ttu-id="67133-144">Параметр *configurationName* пуст.</span><span class="sxs-lookup"><span data-stu-id="67133-144">The *configurationName* parameter is empty.</span></span><br/>                                                                                                                                                         |
| <dl> <span data-ttu-id="67133-145"><dt>**Виртуальная машина \_ \_Имя конфигурации \_ E \_ слишком \_ длинное**</dt> <dt>0xA0040401</dt></span><span class="sxs-lookup"><span data-stu-id="67133-145"><dt>**VM\_E\_CONFIG\_NAME\_TOO\_LONG**</dt> <dt>0xA0040401</dt></span></span> </dl>                | <span data-ttu-id="67133-146">Длина параметра *configurationName* превышает 80 символов.</span><span class="sxs-lookup"><span data-stu-id="67133-146">The *configurationName* parameter exceeds 80 characters in length.</span></span><br/>                                                                                                                                  |
| <dl> <span data-ttu-id="67133-147"><dt>**Виртуальная машина \_ \_Имя конфигурации \_ E \_ недопустимо \_ char**</dt> <dt>0xA0040402</dt></span><span class="sxs-lookup"><span data-stu-id="67133-147"><dt>**VM\_E\_CONFIG\_NAME\_INVALID\_CHAR**</dt> <dt>0xA0040402</dt></span></span> </dl>            | <span data-ttu-id="67133-148">Параметр *configurationName* содержит недопустимый символ (один из " \* ?: <>/ \| \\ " ").</span><span class="sxs-lookup"><span data-stu-id="67133-148">The *configurationName* parameter contains an invalid character (one of "\*?:<>/\|\\"").</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="67133-149"><dt>**Виртуальная машина \_ E \_ Конфигурация \_ дублирует \_ имя**</dt> <dt>0xA0040403</dt></span><span class="sxs-lookup"><span data-stu-id="67133-149"><dt>**VM\_E\_CONFIG\_DUPLICATE\_NAME**</dt> <dt>0xA0040403</dt></span></span> </dl>                | <span data-ttu-id="67133-150">Виртуальная машина с таким именем уже существует.</span><span class="sxs-lookup"><span data-stu-id="67133-150">There is already a virtual machine with this name.</span></span><br/>                                                                                                                                                  |
| <dl> <span data-ttu-id="67133-151"><dt>**Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="67133-151"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="67133-152">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="67133-152">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="67133-153"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="67133-153"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="67133-154">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="67133-154">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="67133-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="67133-155">Remarks</span></span>

<span data-ttu-id="67133-156">В именах виртуальных машин не учитывается регистр, например "MyVM" и "MyVM" ссылаются на одну и ту же виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="67133-156">Virtual machine names are case-insensitive, for example, "MyVM" and "myvm" refer to the same virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="67133-157">Требования</span><span class="sxs-lookup"><span data-stu-id="67133-157">Requirements</span></span>



| <span data-ttu-id="67133-158">Требование</span><span class="sxs-lookup"><span data-stu-id="67133-158">Requirement</span></span> | <span data-ttu-id="67133-159">Значение</span><span class="sxs-lookup"><span data-stu-id="67133-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="67133-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="67133-160">Minimum supported client</span></span><br/> | <span data-ttu-id="67133-161">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="67133-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="67133-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="67133-162">Minimum supported server</span></span><br/> | <span data-ttu-id="67133-163">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="67133-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="67133-164">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="67133-164">End of client support</span></span><br/>    | <span data-ttu-id="67133-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="67133-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="67133-166">Продукт</span><span class="sxs-lookup"><span data-stu-id="67133-166">Product</span></span><br/>                  | <span data-ttu-id="67133-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="67133-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="67133-168">Header</span><span class="sxs-lookup"><span data-stu-id="67133-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="67133-169"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="67133-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="67133-170">IID</span><span class="sxs-lookup"><span data-stu-id="67133-170">IID</span></span><br/>                      | <span data-ttu-id="67133-171">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="67133-171">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="67133-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="67133-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67133-173">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="67133-173">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

