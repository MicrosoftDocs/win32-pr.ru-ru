---
title: Метод Convert (Впккоминтерфацес. h) Ивмхарддиск
description: Преобразует виртуальный жесткий диск фиксированного размера в динамически расширяемый виртуальный жесткий диск или преобразует динамически расширяемый виртуальный жесткий диск в виртуальный жесткий диск фиксированного размера.
ms.assetid: 0dee802a-1cac-499e-918a-7dbb6c98415f
keywords:
- Преобразование метода Virtual PC
- Преобразование метода Virtual PC, интерфейс Ивмхарддиск
- Интерфейс Ивмхарддиск Virtual PC, метод Convert
topic_type:
- apiref
api_name:
- IVMHardDisk.Convert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2398cf4a2f3b366709c009885bf2c2767828fee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492696"
---
# <a name="ivmharddiskconvert-method"></a><span data-ttu-id="6c3e3-106">Метод Ивмхарддиск:: Convert</span><span class="sxs-lookup"><span data-stu-id="6c3e3-106">IVMHardDisk::Convert method</span></span>

<span data-ttu-id="6c3e3-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6c3e3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6c3e3-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6c3e3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6c3e3-109">Преобразует виртуальный жесткий диск фиксированного размера в динамически расширяемый виртуальный жесткий диск или преобразует динамически расширяемый виртуальный жесткий диск в виртуальный жесткий диск фиксированного размера.</span><span class="sxs-lookup"><span data-stu-id="6c3e3-109">Converts a fixed-size virtual hard disk to a dynamically expanding virtual hard disk or converts a dynamically expanding virtual hard disk to a fixed-size virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c3e3-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c3e3-110">Syntax</span></span>


```C++
HRESULT Convert(
  [in]          BSTR           convertedDiskImagePath,
  [in]          VMHardDiskType convertedDiskImageType,
  [out, retval] IVMTask        **convertTask
);
```



## <a name="parameters"></a><span data-ttu-id="6c3e3-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c3e3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c3e3-112">*конвертеддискимажепас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6c3e3-112">*convertedDiskImagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c3e3-113">Путь к файлу образа целевого диска.</span><span class="sxs-lookup"><span data-stu-id="6c3e3-113">The path to the target disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="6c3e3-114">*конвертеддискимажетипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6c3e3-114">*convertedDiskImageType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c3e3-115">Тип образа целевого диска.</span><span class="sxs-lookup"><span data-stu-id="6c3e3-115">The type of the target disk image.</span></span> <span data-ttu-id="6c3e3-116">Список значений см. в разделе [**вмхарддисктипе**](vmharddisktype.md).</span><span class="sxs-lookup"><span data-stu-id="6c3e3-116">For a list of values, see [**VMHardDiskType**](vmharddisktype.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c3e3-117">*конверттаск* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6c3e3-117">*convertTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6c3e3-118">Объект [**ивмтаск**](ivmtask.md) , используемый для отслеживания завершения процесса преобразования.</span><span class="sxs-lookup"><span data-stu-id="6c3e3-118">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the conversion process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c3e3-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c3e3-119">Return value</span></span>

<span data-ttu-id="6c3e3-120">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="6c3e3-120">This method can return one of these values.</span></span>



| <span data-ttu-id="6c3e3-121">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="6c3e3-121">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="6c3e3-122">Описание</span><span class="sxs-lookup"><span data-stu-id="6c3e3-122">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c3e3-123"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6c3e3-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="6c3e3-124">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="6c3e3-124">The operation was successful.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="6c3e3-125"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="6c3e3-125"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                   | <span data-ttu-id="6c3e3-126">Параметр *конвертеддискимажепас* пуст или не содержит расширение VHD для имени файла.</span><span class="sxs-lookup"><span data-stu-id="6c3e3-126">The *convertedDiskImagePath* parameter is empty or missing the .vhd extension on the file name.</span></span><br/>                                      |
| <dl> <span data-ttu-id="6c3e3-127"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="6c3e3-127"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="6c3e3-128">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6c3e3-128">A parameter is **NULL**.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="6c3e3-129"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ путь ошибки \_ не \_ найден)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="6c3e3-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl>   | <span data-ttu-id="6c3e3-130">Системе не удается найти путь, указанный параметром *конвертеддискимажепас* .</span><span class="sxs-lookup"><span data-stu-id="6c3e3-130">The system cannot find the path specified by the *convertedDiskImagePath* parameter.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="6c3e3-131"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ недопустимое \_ имя)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="6c3e3-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>      | <span data-ttu-id="6c3e3-132">Параметр *конвертеддискимажепас* содержит недопустимый символ (один из " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="6c3e3-132">The *convertedDiskImagePath* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                    |
| <dl> <span data-ttu-id="6c3e3-133"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ Bad \_ PATHNAME)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="6c3e3-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>      | <span data-ttu-id="6c3e3-134">Параметр *конвертеддискимажепас* указывает пустой или относительный путь.</span><span class="sxs-lookup"><span data-stu-id="6c3e3-134">The *convertedDiskImagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="6c3e3-135">Требуется абсолютный путь.</span><span class="sxs-lookup"><span data-stu-id="6c3e3-135">An absolute path is required.</span></span><br/>                            |
| <dl> <span data-ttu-id="6c3e3-136"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ \_ переполнение буфера ошибки)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="6c3e3-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl>   | <span data-ttu-id="6c3e3-137">Путь, указанный в параметре *конвертеддискимажепас* , слишком длинный.</span><span class="sxs-lookup"><span data-stu-id="6c3e3-137">The path specified by the *convertedDiskImagePath* parameter is too long.</span></span> <span data-ttu-id="6c3e3-138">Длина пути должна быть меньше **максимального \_ пути** (260).</span><span class="sxs-lookup"><span data-stu-id="6c3e3-138">The path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="6c3e3-139"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ \_ нарушение общего доступа к ошибкам)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="6c3e3-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="6c3e3-140">Виртуальный жесткий диск, на который ссылается этот объект, уже используется или является родительским для этого виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="6c3e3-140">Either the virtual hard disk referenced by this object is in use or the parent of this virtual hard disk is in use.</span></span><br/>                  |
| <dl> <span data-ttu-id="6c3e3-141"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (на \_ диске с ошибкой \_ Full)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="6c3e3-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>         | <span data-ttu-id="6c3e3-142">На томе узла недостаточно места для преобразования этого виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="6c3e3-142">The host volume does not have enough space to convert this virtual hard disk.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="6c3e3-143"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ уже \_ существует)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="6c3e3-143"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>    | <span data-ttu-id="6c3e3-144">Файл, на который ссылается параметр *конвертеддискимажепас* , уже существует.</span><span class="sxs-lookup"><span data-stu-id="6c3e3-144">The file referenced by the *convertedDiskImagePath* parameter already exists.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="6c3e3-145"><dt>**Виртуальная машина \_ \_Неверный \_ \_ \_ тип**</dt> <dt>0xA004067Bного</dt> образа HD</span><span class="sxs-lookup"><span data-stu-id="6c3e3-145"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="6c3e3-146">Параметр *конвертеддискимажепас* должен иметь значение **Вмдисктипе \_ dynamic** или **вмдисктипе \_ FixedSize**.</span><span class="sxs-lookup"><span data-stu-id="6c3e3-146">The *convertedDiskImagePath* parameter must be either **vmDiskType\_Dynamic** or **vmDiskType\_FixedSize**.</span></span><br/>                          |
| <dl> <span data-ttu-id="6c3e3-147"><dt>**Виртуальная машина \_ E \_ Недопустимый \_ \_ файл HD**</dt> <dt>0xA0040682</dt></span><span class="sxs-lookup"><span data-stu-id="6c3e3-147"><dt>**VM\_E\_INVALID\_HD\_FILE**</dt> <dt>0xA0040682</dt></span></span> </dl>                        | <span data-ttu-id="6c3e3-148">Возможно, образ виртуального жесткого диска, на который ссылается этот объект [**ивмхарддиск**](ivmharddisk.md) , не является допустимым образом.</span><span class="sxs-lookup"><span data-stu-id="6c3e3-148">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object does not seem to be a valid image.</span></span><br/>          |
| <dl> <span data-ttu-id="6c3e3-149"><dt>**Виртуальная машина \_ \_ \_ Путь к родительскому каталогу E \_ не \_ найден**</dt> <dt>0xA0040677</dt></span><span class="sxs-lookup"><span data-stu-id="6c3e3-149"><dt>**VM\_E\_PARENT\_PATH\_NOT\_FOUND**</dt> <dt>0xA0040677</dt></span></span> </dl>                 | <span data-ttu-id="6c3e3-150">Родительский элемент виртуального жесткого диска, на который ссылается этот объект, не существует.</span><span class="sxs-lookup"><span data-stu-id="6c3e3-150">The parent of the virtual hard disk referenced by this object does not exist.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="6c3e3-151"><dt>**Виртуальная машина \_ \_Приложение E \_ завершает работу \_**</dt> <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="6c3e3-151"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="6c3e3-152">Невозможно преобразовать образ виртуального жесткого диска, так как приложение завершает работу.</span><span class="sxs-lookup"><span data-stu-id="6c3e3-152">The virtual hard disk image cannot be converted because the application is shutting down.</span></span><br/>                                            |
| <dl> <span data-ttu-id="6c3e3-153"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6c3e3-153"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="6c3e3-154">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="6c3e3-154">An unexpected error has occurred.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="6c3e3-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c3e3-155">Remarks</span></span>

<span data-ttu-id="6c3e3-156">Исходный файл остается неизменным после процесса преобразования.</span><span class="sxs-lookup"><span data-stu-id="6c3e3-156">The source file is left intact after the conversion process.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c3e3-157">Требования</span><span class="sxs-lookup"><span data-stu-id="6c3e3-157">Requirements</span></span>



| <span data-ttu-id="6c3e3-158">Требование</span><span class="sxs-lookup"><span data-stu-id="6c3e3-158">Requirement</span></span> | <span data-ttu-id="6c3e3-159">Значение</span><span class="sxs-lookup"><span data-stu-id="6c3e3-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c3e3-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c3e3-160">Minimum supported client</span></span><br/> | <span data-ttu-id="6c3e3-161">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6c3e3-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6c3e3-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c3e3-162">Minimum supported server</span></span><br/> | <span data-ttu-id="6c3e3-163">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6c3e3-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6c3e3-164">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="6c3e3-164">End of client support</span></span><br/>    | <span data-ttu-id="6c3e3-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6c3e3-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6c3e3-166">Продукт</span><span class="sxs-lookup"><span data-stu-id="6c3e3-166">Product</span></span><br/>                  | <span data-ttu-id="6c3e3-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6c3e3-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6c3e3-168">Header</span><span class="sxs-lookup"><span data-stu-id="6c3e3-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c3e3-169"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c3e3-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6c3e3-170">IID</span><span class="sxs-lookup"><span data-stu-id="6c3e3-170">IID</span></span><br/>                      | <span data-ttu-id="6c3e3-171">IID \_ ивмхарддиск определен как ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="6c3e3-171">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="6c3e3-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c3e3-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c3e3-173">**ивмхарддиск**</span><span class="sxs-lookup"><span data-stu-id="6c3e3-173">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

