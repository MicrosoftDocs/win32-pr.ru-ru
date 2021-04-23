---
title: Метод Ивмхарддиск Мержето (Впккоминтерфацес. h)
description: Объединяет разностный виртуальный жесткий диск со всеми его родительскими элементами.
ms.assetid: 3c63f892-7c05-4ed6-a59a-914a921ec391
keywords:
- Метод Мержето Virtual PC
- Метод Мержето Virtual PC, интерфейс Ивмхарддиск
- Ивмхарддиск интерфейс Virtual PC, метод Мержето
topic_type:
- apiref
api_name:
- IVMHardDisk.MergeTo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13d0db44388c8ee021fa8cc8c8fdbfe2c434833f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136090"
---
# <a name="ivmharddiskmergeto-method"></a><span data-ttu-id="d69d9-106">Метод Ивмхарддиск:: Мержето</span><span class="sxs-lookup"><span data-stu-id="d69d9-106">IVMHardDisk::MergeTo method</span></span>

<span data-ttu-id="d69d9-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d69d9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d69d9-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d69d9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d69d9-109">Слияние разностного виртуального жесткого диска со всеми его родительскими элементами (вплоть до корневого родительского виртуального жесткого диска и включая его) в новый файл жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="d69d9-109">Merges a differencing virtual hard disk with all of its parents (up to and including the root parent virtual hard disk) to a new hard disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d69d9-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d69d9-110">Syntax</span></span>


```C++
HRESULT MergeTo(
  [in]          BSTR           newDiskImagePath,
  [in]          VMHardDiskType newDiskImageType,
  [out, retval] IVMTask        **mergeTask
);
```



## <a name="parameters"></a><span data-ttu-id="d69d9-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d69d9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d69d9-112">*невдискимажепас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d69d9-112">*newDiskImagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d69d9-113">Путь к новому целевому образу диска, в который будут объединены выбранные образы дисков.</span><span class="sxs-lookup"><span data-stu-id="d69d9-113">The path to the new target disk image where the selected disk images will be merged.</span></span>

</dd> <dt>

<span data-ttu-id="d69d9-114">*невдискимажетипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d69d9-114">*newDiskImageType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d69d9-115">Тип нового образа целевого диска.</span><span class="sxs-lookup"><span data-stu-id="d69d9-115">The type of new target disk image.</span></span> <span data-ttu-id="d69d9-116">Для нового образа целевого диска допустимы следующие типы образов: **вмдисктипе \_ dynamic** и **вмдисктипе \_ FixedSize**.</span><span class="sxs-lookup"><span data-stu-id="d69d9-116">The image types allowed for the new target disk image are **vmDiskType\_Dynamic** and **vmDiskType\_FixedSize**.</span></span> <span data-ttu-id="d69d9-117">Дополнительные сведения см. в разделе [**вмхарддисктипе**](vmharddisktype.md).</span><span class="sxs-lookup"><span data-stu-id="d69d9-117">For more information, see [**VMHardDiskType**](vmharddisktype.md).</span></span>

</dd> <dt>

<span data-ttu-id="d69d9-118">*мержетаск* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d69d9-118">*mergeTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d69d9-119">Объект [**ивмтаск**](ivmtask.md) , который используется для отслеживания завершения процесса слияния.</span><span class="sxs-lookup"><span data-stu-id="d69d9-119">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the merging process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d69d9-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d69d9-120">Return value</span></span>

<span data-ttu-id="d69d9-121">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="d69d9-121">This method can return one of these values.</span></span>



| <span data-ttu-id="d69d9-122">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="d69d9-122">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="d69d9-123">Описание</span><span class="sxs-lookup"><span data-stu-id="d69d9-123">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d69d9-124"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d69d9-124"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="d69d9-125">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d69d9-125">The operation was successful.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="d69d9-126"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="d69d9-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="d69d9-127">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d69d9-127">A parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="d69d9-128"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="d69d9-128"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                   | <span data-ttu-id="d69d9-129">Параметр *невдискимажепас* пуст.</span><span class="sxs-lookup"><span data-stu-id="d69d9-129">The *newDiskImagePath* parameter is empty.</span></span><br/>                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="d69d9-130"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ файл ошибки \_ не \_ найден)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="d69d9-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl>   | <span data-ttu-id="d69d9-131">Системе не удается найти файл, указанный параметром *невдискимажепас* .</span><span class="sxs-lookup"><span data-stu-id="d69d9-131">The system cannot find the file specified by the *newDiskImagePath* parameter.</span></span><br/>                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="d69d9-132"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ путь ошибки \_ не \_ найден)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="d69d9-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl>   | <span data-ttu-id="d69d9-133">Системе не удается найти путь, указанный параметром *невдискимажепас* .</span><span class="sxs-lookup"><span data-stu-id="d69d9-133">The system cannot find the path specified by the *newDiskImagePath* parameter.</span></span><br/>                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="d69d9-134"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ недопустимое \_ имя)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="d69d9-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>      | <span data-ttu-id="d69d9-135">Параметр *невдискимажепас* содержит недопустимый символ (один из следующих: " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="d69d9-135">The *newDiskImagePath* parameter contains an invalid character (one of the following: "\*?<>/\|":").</span></span><br/>                                                                                                                                                                                         |
| <dl> <span data-ttu-id="d69d9-136"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ Bad \_ PATHNAME)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="d69d9-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>      | <span data-ttu-id="d69d9-137">Параметр *невдискимажепас* указывает пустой или относительный путь.</span><span class="sxs-lookup"><span data-stu-id="d69d9-137">The *newDiskImagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="d69d9-138">Требуется абсолютный путь.</span><span class="sxs-lookup"><span data-stu-id="d69d9-138">An absolute path is required.</span></span><br/>                                                                                                                                                                                                |
| <dl> <span data-ttu-id="d69d9-139"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ \_ переполнение буфера ошибки)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="d69d9-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl>   | <span data-ttu-id="d69d9-140">Путь, указанный в параметре *невдискимажепас* , слишком длинный.</span><span class="sxs-lookup"><span data-stu-id="d69d9-140">The path specified by the *newDiskImagePath* parameter is too long.</span></span> <span data-ttu-id="d69d9-141">Длина пути должна быть меньше 260 символов.</span><span class="sxs-lookup"><span data-stu-id="d69d9-141">The path must be less than 260 characters.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="d69d9-142"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ \_ нарушение общего доступа к ошибкам)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="d69d9-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="d69d9-143">Виртуальный жесткий диск, на который ссылается этот объект, уже используется или является родительским для этого виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="d69d9-143">Either the virtual hard disk referenced by this object is in use or the parent of this virtual hard disk is in use.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="d69d9-144"><dt>**Виртуальная машина \_ \_Неверный \_ \_ \_ тип**</dt> <dt>0xA004067Bного</dt> образа HD</span><span class="sxs-lookup"><span data-stu-id="d69d9-144"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="d69d9-145">Эта ошибка возникает из-за того, что образ виртуального жесткого диска, на который ссылается этот объект [**ивмхарддиск**](ivmharddisk.md) , не является образом разностного диска или если параметр *невдискимажетипе* не является одним из допустимых значений, **вмдисктипе \_ dynamic** или **вмдисктипе \_ FixedSize**.</span><span class="sxs-lookup"><span data-stu-id="d69d9-145">This error is caused either because the virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is not a differencing disk image or because the parameter *newDiskImageType* is not one of the accepted values, **vmDiskType\_Dynamic** or **vmDiskType\_FixedSize**.</span></span><br/> |
| <dl> <span data-ttu-id="d69d9-146"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ уже \_ существует)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="d69d9-146"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>    | <span data-ttu-id="d69d9-147">Файл, на который ссылается параметр *невдискимажепас* , уже существует.</span><span class="sxs-lookup"><span data-stu-id="d69d9-147">The file referenced by the *newDiskImagePath* parameter already exists.</span></span><br/>                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="d69d9-148"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (на \_ диске с ошибкой \_ Full)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="d69d9-148"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>         | <span data-ttu-id="d69d9-149">На томе узла недостаточно места для слияния этого виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="d69d9-149">The host volume does not have enough space to merge this virtual hard disk.</span></span><br/>                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="d69d9-150"><dt>**Виртуальная машина \_ \_ \_ Путь к родительскому каталогу E \_ не \_ найден**</dt> <dt>0xA0040677</dt></span><span class="sxs-lookup"><span data-stu-id="d69d9-150"><dt>**VM\_E\_PARENT\_PATH\_NOT\_FOUND**</dt> <dt>0xA0040677</dt></span></span> </dl>                 | <span data-ttu-id="d69d9-151">Родительский элемент виртуального жесткого диска, на который ссылается этот объект, не существует.</span><span class="sxs-lookup"><span data-stu-id="d69d9-151">The parent of the virtual hard disk referenced by this object does not exist.</span></span><br/>                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="d69d9-152"><dt>**Виртуальная машина \_ \_Приложение E \_ завершает работу \_**</dt> <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="d69d9-152"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="d69d9-153">Не удается выполнить слияние образа виртуального жесткого диска, так как приложение завершает работу.</span><span class="sxs-lookup"><span data-stu-id="d69d9-153">The virtual hard disk image cannot be merged because the application is shutting down.</span></span><br/>                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="d69d9-154"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d69d9-154"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="d69d9-155">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d69d9-155">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="d69d9-156">Требования</span><span class="sxs-lookup"><span data-stu-id="d69d9-156">Requirements</span></span>



| <span data-ttu-id="d69d9-157">Требование</span><span class="sxs-lookup"><span data-stu-id="d69d9-157">Requirement</span></span> | <span data-ttu-id="d69d9-158">Значение</span><span class="sxs-lookup"><span data-stu-id="d69d9-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d69d9-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d69d9-159">Minimum supported client</span></span><br/> | <span data-ttu-id="d69d9-160">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d69d9-160">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d69d9-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d69d9-161">Minimum supported server</span></span><br/> | <span data-ttu-id="d69d9-162">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d69d9-162">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d69d9-163">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d69d9-163">End of client support</span></span><br/>    | <span data-ttu-id="d69d9-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d69d9-164">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d69d9-165">Продукт</span><span class="sxs-lookup"><span data-stu-id="d69d9-165">Product</span></span><br/>                  | <span data-ttu-id="d69d9-166">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d69d9-166">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d69d9-167">Header</span><span class="sxs-lookup"><span data-stu-id="d69d9-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="d69d9-168"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="d69d9-168"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d69d9-169">IID</span><span class="sxs-lookup"><span data-stu-id="d69d9-169">IID</span></span><br/>                      | <span data-ttu-id="d69d9-170">IID \_ ивмхарддиск определен как ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="d69d9-170">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="d69d9-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d69d9-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d69d9-172">**ивмхарддиск**</span><span class="sxs-lookup"><span data-stu-id="d69d9-172">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

