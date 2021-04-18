---
title: Метод Ивмвиртуалпк КреатедифференЦингвиртуалхарддиск (Впккоминтерфацес. h)
description: Создает разностный виртуальный жесткий диск.
ms.assetid: 6a33aa6f-a0e8-45d8-bdc1-0864561db162
keywords:
- Метод КреатедифференЦингвиртуалхарддиск Virtual PC
- Метод КреатедифференЦингвиртуалхарддиск Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, метод КреатедифференЦингвиртуалхарддиск
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateDifferencingVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2bab178d64008b236988bfb723bd75a09a7edaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691909"
---
# <a name="ivmvirtualpccreatedifferencingvirtualharddisk-method"></a><span data-ttu-id="91ca8-106">Метод Ивмвиртуалпк:: КреатедифференЦингвиртуалхарддиск</span><span class="sxs-lookup"><span data-stu-id="91ca8-106">IVMVirtualPC::CreateDifferencingVirtualHardDisk method</span></span>

<span data-ttu-id="91ca8-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="91ca8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="91ca8-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="91ca8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="91ca8-109">Создает разностный виртуальный жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="91ca8-109">Creates a differencing virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="91ca8-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91ca8-110">Syntax</span></span>


```C++
HRESULT CreateDifferencingVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          BSTR    parentPath,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a><span data-ttu-id="91ca8-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="91ca8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91ca8-112">*imagePath* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="91ca8-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91ca8-113">Путь к новому файлу образа диска.</span><span class="sxs-lookup"><span data-stu-id="91ca8-113">The path to the new disk image file.</span></span> <span data-ttu-id="91ca8-114">Содержащаяся папка будет создана, если она не существует.</span><span class="sxs-lookup"><span data-stu-id="91ca8-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="91ca8-115">*парентпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="91ca8-115">*parentPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91ca8-116">Путь к файлу образа родительского диска.</span><span class="sxs-lookup"><span data-stu-id="91ca8-116">The path to the parent disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="91ca8-117">*дисктаск* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="91ca8-117">*diskTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="91ca8-118">Объект [**ивмтаск**](ivmtask.md) , используемый для отслеживания создания образа.</span><span class="sxs-lookup"><span data-stu-id="91ca8-118">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91ca8-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91ca8-119">Return value</span></span>

<span data-ttu-id="91ca8-120">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="91ca8-120">This method can return one of these values.</span></span>



| <span data-ttu-id="91ca8-121">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="91ca8-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="91ca8-122">Описание</span><span class="sxs-lookup"><span data-stu-id="91ca8-122">Description</span></span>                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="91ca8-123"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="91ca8-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="91ca8-124">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="91ca8-124">The operation was successful.</span></span><br/>                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="91ca8-125"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="91ca8-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="91ca8-126">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="91ca8-126">A parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="91ca8-127"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ путь ошибки \_ не \_ найден)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="91ca8-127"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="91ca8-128">Системе не удается найти путь, указанный параметром *imagePath* или *парентпас* .</span><span class="sxs-lookup"><span data-stu-id="91ca8-128">The system cannot find the path specified by the *imagePath* or *parentPath* parameter.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="91ca8-129"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ недопустимого \_ диска)**</dt> <dt>0x8007000f</dt></span><span class="sxs-lookup"><span data-stu-id="91ca8-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_DRIVE)**</dt> <dt>0x8007000f</dt></span></span> </dl>   | <span data-ttu-id="91ca8-130">Файл, указанный параметром *imagePath* , находится на компакт-диске или DVD-диске.</span><span class="sxs-lookup"><span data-stu-id="91ca8-130">The file specified by the *imagePath* parameter is on a CD-ROM or DVD-ROM.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="91ca8-131"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ недопустимое \_ имя)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="91ca8-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="91ca8-132">Параметр *imagePath* или *парентпас* содержит недопустимый символ (один из " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="91ca8-132">The *imagePath* or *parentPath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="91ca8-133"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ Bad \_ PATHNAME)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="91ca8-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="91ca8-134">Параметр *imagePath* и *парентпас* указывает пустой или относительный путь.</span><span class="sxs-lookup"><span data-stu-id="91ca8-134">Both the *imagePath* and *parentPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="91ca8-135">По крайней мере один из параметров должен быть абсолютным путем.</span><span class="sxs-lookup"><span data-stu-id="91ca8-135">At least one of the parameters must be an absolute path.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="91ca8-136"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ \_ переполнение буфера ошибки)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="91ca8-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="91ca8-137">Путь, указанный в параметре *imagePath* или *парентпас* , слишком длинный.</span><span class="sxs-lookup"><span data-stu-id="91ca8-137">The path specified by the *imagePath* or *parentPath* parameters is too long.</span></span> <span data-ttu-id="91ca8-138">Длина пути должна быть меньше 260 символов.</span><span class="sxs-lookup"><span data-stu-id="91ca8-138">The length of the path must be less than 260 characters.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="91ca8-139"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ уже \_ существует)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="91ca8-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="91ca8-140">Файл, на который ссылается параметр *imagePath* , уже существует.</span><span class="sxs-lookup"><span data-stu-id="91ca8-140">The file referenced by the *imagePath* parameter already exists.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="91ca8-141"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (на \_ диске с ошибкой \_ Full)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="91ca8-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="91ca8-142">Для динамического расширяющего образа виртуального жесткого диска требуется по меньшей мере 8 МБ свободного места на томе узла.</span><span class="sxs-lookup"><span data-stu-id="91ca8-142">The dynamically expanding virtual hard disk image needs at least 8 MB free on the host volume.</span></span><br/>                                                                                                                                      |
| <dl> <span data-ttu-id="91ca8-143"><dt>**Виртуальная машина \_ \_Размер изображения \_ E \_ слишком \_ велик**</dt> <dt>0xA0040683</dt></span><span class="sxs-lookup"><span data-stu-id="91ca8-143"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_LARGE**</dt> <dt>0xA0040683</dt></span></span> </dl>                | <span data-ttu-id="91ca8-144">*Размер* параметра должен быть менее 2 088 960 МБ.</span><span class="sxs-lookup"><span data-stu-id="91ca8-144">The parameter *size* must be less than 2,088,960 MB.</span></span> <span data-ttu-id="91ca8-145">Если используется формат FAT16, размер должен быть менее 2000 МБ.</span><span class="sxs-lookup"><span data-stu-id="91ca8-145">If the format is FAT16, then size must be less than 2000 MB.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="91ca8-146"><dt>**Виртуальная машина \_ \_Размер образа \_ E \_ слишком \_ мал**</dt> <dt>0xA0040684</dt></span><span class="sxs-lookup"><span data-stu-id="91ca8-146"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_SMALL**</dt> <dt>0xA0040684</dt></span></span> </dl>                | <span data-ttu-id="91ca8-147">Образы виртуальных жестких дисков в формате неформатированного и FAT16 должны иметь по крайней мере 3 МБ.</span><span class="sxs-lookup"><span data-stu-id="91ca8-147">Unformatted and FAT16 formatted virtual hard disk images must be at least 3 MB.</span></span> <span data-ttu-id="91ca8-148">Образы виртуальных жестких дисков в формате FAT32 должны иметь не менее 514 МБ.</span><span class="sxs-lookup"><span data-stu-id="91ca8-148">FAT32 formatted virtual hard disk images must be at least 514 MB.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="91ca8-149"><dt>**Виртуальная машина \_ \_ \_ Слишком большой файл \_ E \_ для \_ тома**</dt> <dt>0xA0040679</dt></span><span class="sxs-lookup"><span data-stu-id="91ca8-149"><dt>**VM\_E\_FILE\_TOO\_LARGE\_FOR\_VOLUME**</dt> <dt>0xA0040679</dt></span></span> </dl>          | <span data-ttu-id="91ca8-150">Том узла не поддерживает файл такого размера, если динамически расширяемый образ виртуального жесткого диска расширяется до полного предела.</span><span class="sxs-lookup"><span data-stu-id="91ca8-150">The host volume cannot support a file this size if the dynamically expanding virtual hard disk image expands to its full limit.</span></span> <span data-ttu-id="91ca8-151">Максимальный размер файла для тома FAT32 составляет 4 ГБ.</span><span class="sxs-lookup"><span data-stu-id="91ca8-151">The maximum file size for a FAT32 volume is 4 GB.</span></span> <span data-ttu-id="91ca8-152">Максимальный размер файла для тома FAT16 составляет 2 ГБ.</span><span class="sxs-lookup"><span data-stu-id="91ca8-152">The maximum file size for a FAT16 volume is 2 GB.</span></span><br/> |
| <dl> <span data-ttu-id="91ca8-153"><dt>**Виртуальная машина \_ \_Приложение E \_ завершает работу \_**</dt> <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="91ca8-153"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                    | <span data-ttu-id="91ca8-154">Невозможно создать виртуальный жесткий диск после начала работы приложения.</span><span class="sxs-lookup"><span data-stu-id="91ca8-154">The virtual hard disk cannot be created after the application has started shutting down.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="91ca8-155"><dt>**Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="91ca8-155"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="91ca8-156">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="91ca8-156">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="91ca8-157"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="91ca8-157"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="91ca8-158">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="91ca8-158">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="91ca8-159">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91ca8-159">Remarks</span></span>

<span data-ttu-id="91ca8-160">Хотя либо *imagePath* , либо *парентпас* могут быть относительным путем, по крайней мере один из них должен быть абсолютным путем.</span><span class="sxs-lookup"><span data-stu-id="91ca8-160">Although either *imagePath* or *parentPath* can be a relative path, at least one of these must be an absolute path.</span></span> <span data-ttu-id="91ca8-161">Если один параметр пути является относительным, предполагается, что он является относительным по отношению к другому параметру пути.</span><span class="sxs-lookup"><span data-stu-id="91ca8-161">If one path parameter is a relative path, it is assumed to be relative to the other path parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="91ca8-162">Требования</span><span class="sxs-lookup"><span data-stu-id="91ca8-162">Requirements</span></span>



| <span data-ttu-id="91ca8-163">Требование</span><span class="sxs-lookup"><span data-stu-id="91ca8-163">Requirement</span></span> | <span data-ttu-id="91ca8-164">Значение</span><span class="sxs-lookup"><span data-stu-id="91ca8-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="91ca8-165">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91ca8-165">Minimum supported client</span></span><br/> | <span data-ttu-id="91ca8-166">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="91ca8-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="91ca8-167">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91ca8-167">Minimum supported server</span></span><br/> | <span data-ttu-id="91ca8-168">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="91ca8-168">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="91ca8-169">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="91ca8-169">End of client support</span></span><br/>    | <span data-ttu-id="91ca8-170">Windows 7</span><span class="sxs-lookup"><span data-stu-id="91ca8-170">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="91ca8-171">Продукт</span><span class="sxs-lookup"><span data-stu-id="91ca8-171">Product</span></span><br/>                  | <span data-ttu-id="91ca8-172">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="91ca8-172">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="91ca8-173">Header</span><span class="sxs-lookup"><span data-stu-id="91ca8-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="91ca8-174"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="91ca8-174"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="91ca8-175">IID</span><span class="sxs-lookup"><span data-stu-id="91ca8-175">IID</span></span><br/>                      | <span data-ttu-id="91ca8-176">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="91ca8-176">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="91ca8-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91ca8-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91ca8-178">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="91ca8-178">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

