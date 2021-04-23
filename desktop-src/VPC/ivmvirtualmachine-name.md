---
title: Свойство имени Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Имя конфигурации виртуальной машины.
ms.assetid: 90acedbf-4159-48a3-a9e9-6f1ee00dab8b
keywords:
- Имя свойство Virtual PC
- Имя свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство Name
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Name
- IVMVirtualMachine.get_Name
- IVMVirtualMachine.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c163173a778d8103922fd8c8948ab5156f512ed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136179"
---
# <a name="ivmvirtualmachinename-property"></a><span data-ttu-id="0c500-106">Свойство Ивмвиртуалмачине:: Name</span><span class="sxs-lookup"><span data-stu-id="0c500-106">IVMVirtualMachine::Name property</span></span>

<span data-ttu-id="0c500-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0c500-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0c500-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0c500-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0c500-109">Извлекает и задает имя конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0c500-109">Retrieves and sets the name of the virtual machine configuration.</span></span>

<span data-ttu-id="0c500-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="0c500-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c500-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c500-111">Syntax</span></span>


```C++
HRESULT put_Name(
  [in]          BSTR virtualMachineName
);

HRESULT get_Name(
  [out, retval] BSTR *virtualMachineName
);
```



## <a name="property-value"></a><span data-ttu-id="0c500-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0c500-112">Property value</span></span>

<span data-ttu-id="0c500-113">Указывает имя конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0c500-113">Specifies the name of the virtual machine configuration.</span></span> <span data-ttu-id="0c500-114">Длина имени не может превышать 80 символов, а общая длина полного пути, включающего в себя файл конфигурации имени виртуальной машины, не может превышать **Максимальное значение \_ пути** (260) символов.</span><span class="sxs-lookup"><span data-stu-id="0c500-114">The length of the name cannot be more than 80 characters and the total length of the fully qualified path that includes the virtual machine name configuration file cannot be more than **MAX\_PATH** (260) characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0c500-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="0c500-115">Error codes</span></span>



| <span data-ttu-id="0c500-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="0c500-116">Name/value</span></span>                                                                                                                                                                    | <span data-ttu-id="0c500-117">Значение</span><span class="sxs-lookup"><span data-stu-id="0c500-117">Meaning</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0c500-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0c500-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                       | <span data-ttu-id="0c500-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="0c500-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="0c500-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="0c500-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                         | <span data-ttu-id="0c500-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0c500-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="0c500-122"><dt>Д \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="0c500-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                      | <span data-ttu-id="0c500-123">Параметр недопустим или является пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="0c500-123">The parameter is not valid or is an empty string.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0c500-124"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0c500-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                 | <span data-ttu-id="0c500-125">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="0c500-125">The configuration is unknown.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="0c500-126"><dt>Виртуальная машина \_ \_Преф \_ Виртуальная машина E \_ Active</dt> <dt>0xA0040302</dt></span><span class="sxs-lookup"><span data-stu-id="0c500-126"><dt>VM\_E\_PREF\_VM\_ACTIVE</dt> <dt>0xA0040302</dt></span></span> </dl>            | <span data-ttu-id="0c500-127">Виртуальная машина запущена или сохранена.</span><span class="sxs-lookup"><span data-stu-id="0c500-127">The virtual machine is running or saved.</span></span><br/>                                             |
| <dl> <span data-ttu-id="0c500-128"><dt>Виртуальная машина \_ E \_ Конфигурация \_ без \_ имени</dt> <dt>0xA0040400</dt></span><span class="sxs-lookup"><span data-stu-id="0c500-128"><dt>VM\_E\_CONFIG\_NO\_NAME</dt> <dt>0xA0040400</dt></span></span> </dl>            | <span data-ttu-id="0c500-129">Параметр *virtualMachineName* пуст.</span><span class="sxs-lookup"><span data-stu-id="0c500-129">The *virtualMachineName* parameter is empty.</span></span><br/>                                         |
| <dl> <span data-ttu-id="0c500-130"><dt>Виртуальная машина \_ \_Имя конфигурации \_ E \_ слишком \_ длинное</dt> <dt>0xA00400401</dt></span><span class="sxs-lookup"><span data-stu-id="0c500-130"><dt>VM\_E\_CONFIG\_NAME\_TOO\_LONG</dt> <dt>0xA00400401</dt></span></span> </dl>    | <span data-ttu-id="0c500-131">Параметр содержит слишком много символов.</span><span class="sxs-lookup"><span data-stu-id="0c500-131">The parameter contains too many characters.</span></span><br/>                                          |
| <dl> <span data-ttu-id="0c500-132"><dt>Виртуальная машина \_ \_Имя конфигурации \_ E \_ недопустимо \_ char</dt> <dt>0xA0040402</dt></span><span class="sxs-lookup"><span data-stu-id="0c500-132"><dt>VM\_E\_CONFIG\_NAME\_INVALID\_CHAR</dt> <dt>0xA0040402</dt></span></span> </dl> | <span data-ttu-id="0c500-133">Параметр содержит один из следующих недопустимых символов " \* ?: <>/ \| \\ " ".</span><span class="sxs-lookup"><span data-stu-id="0c500-133">The parameter contains one of the following invalid characters "\*?:<>/\|\\"".</span></span><br/> |
| <dl> <span data-ttu-id="0c500-134"><dt>Виртуальная машина \_ E \_ Конфигурация \_ дублирует \_ имя</dt> <dt>0xA0040403</dt></span><span class="sxs-lookup"><span data-stu-id="0c500-134"><dt>VM\_E\_CONFIG\_DUPLICATE\_NAME</dt> <dt>0xA0040403</dt></span></span> </dl>     | <span data-ttu-id="0c500-135">Указанное имя уже существует в качестве имени другой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0c500-135">The specified name already exists as the name of another virtual machine.</span></span><br/>            |
| <dl> <span data-ttu-id="0c500-136"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0c500-136"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                 | <span data-ttu-id="0c500-137">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="0c500-137">An unexpected error has occurred.</span></span><br/>                                                    |



## <a name="remarks"></a><span data-ttu-id="0c500-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0c500-138">Remarks</span></span>

<span data-ttu-id="0c500-139">В именах виртуальных машин не учитывается регистр, например "MyVM" и "MyVM" ссылаются на одну и ту же виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="0c500-139">Virtual machine names are case-insensitive, e.g. "MyVM" and "myvm" refer to the same virtual machine.</span></span> <span data-ttu-id="0c500-140">Это свойство по умолчанию для [**ивмвиртуалмачине**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="0c500-140">This is the default property for [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

<span data-ttu-id="0c500-141">Если VPC.exe выполняется и виртуальная машина сохранена, установка свойства **Name** не будет выполнена.</span><span class="sxs-lookup"><span data-stu-id="0c500-141">If VPC.exe is running and the VM is saved then setting the **Name** property will not succeed.</span></span> <span data-ttu-id="0c500-142">Если VPC.exe не выполняется и виртуальная машина сохранена, при следующем запуске VPC.exe свойство **Name** будет иметь значение.</span><span class="sxs-lookup"><span data-stu-id="0c500-142">If VPC.exe is not running and the VM is saved then setting the **Name** property will succeed when VPC.exe is next started.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c500-143">Требования</span><span class="sxs-lookup"><span data-stu-id="0c500-143">Requirements</span></span>



| <span data-ttu-id="0c500-144">Требование</span><span class="sxs-lookup"><span data-stu-id="0c500-144">Requirement</span></span> | <span data-ttu-id="0c500-145">Значение</span><span class="sxs-lookup"><span data-stu-id="0c500-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c500-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c500-146">Minimum supported client</span></span><br/> | <span data-ttu-id="0c500-147">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0c500-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0c500-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c500-148">Minimum supported server</span></span><br/> | <span data-ttu-id="0c500-149">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0c500-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0c500-150">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="0c500-150">End of client support</span></span><br/>    | <span data-ttu-id="0c500-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0c500-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0c500-152">Продукт</span><span class="sxs-lookup"><span data-stu-id="0c500-152">Product</span></span><br/>                  | <span data-ttu-id="0c500-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0c500-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0c500-154">Header</span><span class="sxs-lookup"><span data-stu-id="0c500-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c500-155"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c500-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0c500-156">IID</span><span class="sxs-lookup"><span data-stu-id="0c500-156">IID</span></span><br/>                      | <span data-ttu-id="0c500-157">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="0c500-157">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="0c500-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c500-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c500-159">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="0c500-159">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

