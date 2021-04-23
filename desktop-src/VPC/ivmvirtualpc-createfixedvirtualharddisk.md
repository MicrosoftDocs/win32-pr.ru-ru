---
title: Метод Ивмвиртуалпк Креатефикседвиртуалхарддиск (Впккоминтерфацес. h)
description: Создает виртуальный жесткий диск фиксированного размера.
ms.assetid: c58a7f2c-efd7-4a39-9ce5-617baa82084b
keywords:
- Метод Креатефикседвиртуалхарддиск Virtual PC
- Метод Креатефикседвиртуалхарддиск Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, метод Креатефикседвиртуалхарддиск
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateFixedVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c1c260611ba3a8b55f87f23d0957c53a304a471
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136086"
---
# <a name="ivmvirtualpccreatefixedvirtualharddisk-method"></a><span data-ttu-id="3186f-106">Метод Ивмвиртуалпк:: Креатефикседвиртуалхарддиск</span><span class="sxs-lookup"><span data-stu-id="3186f-106">IVMVirtualPC::CreateFixedVirtualHardDisk method</span></span>

<span data-ttu-id="3186f-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3186f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3186f-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3186f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3186f-109">Создает виртуальный жесткий диск фиксированного размера.</span><span class="sxs-lookup"><span data-stu-id="3186f-109">Creates a fixed-size virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="3186f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3186f-110">Syntax</span></span>


```C++
HRESULT CreateFixedVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          long    size,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a><span data-ttu-id="3186f-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="3186f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3186f-112">*imagePath* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3186f-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3186f-113">Полный путь к новому файлу образа диска.</span><span class="sxs-lookup"><span data-stu-id="3186f-113">The full path to the new disk image file.</span></span> <span data-ttu-id="3186f-114">Содержащаяся папка будет создана, если она не существует.</span><span class="sxs-lookup"><span data-stu-id="3186f-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="3186f-115">*Размер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3186f-115">*size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3186f-116">Размер изображения в мегабайтах.</span><span class="sxs-lookup"><span data-stu-id="3186f-116">The size, in megabytes, of the image.</span></span> <span data-ttu-id="3186f-117">Максимальный размер — 2 088 960 МБ (2040GB).</span><span class="sxs-lookup"><span data-stu-id="3186f-117">Maximum size is 2,088,960 MB (2040GB).</span></span>

</dd> <dt>

<span data-ttu-id="3186f-118">*дисктаск* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3186f-118">*diskTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3186f-119">Объект [**ивмтаск**](ivmtask.md) , используемый для отслеживания создания образа.</span><span class="sxs-lookup"><span data-stu-id="3186f-119">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3186f-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3186f-120">Return value</span></span>

<span data-ttu-id="3186f-121">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="3186f-121">This method can return one of these values.</span></span>



| <span data-ttu-id="3186f-122">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="3186f-122">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="3186f-123">Описание</span><span class="sxs-lookup"><span data-stu-id="3186f-123">Description</span></span>                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3186f-124"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3186f-124"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="3186f-125">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="3186f-125">The operation was successful.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="3186f-126"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="3186f-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="3186f-127">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3186f-127">A parameter is **NULL**.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="3186f-128"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="3186f-128"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="3186f-129">Параметр *size* меньше или равен 0.</span><span class="sxs-lookup"><span data-stu-id="3186f-129">The *size* parameter is less than or equal to 0.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="3186f-130"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ путь ошибки \_ не \_ найден)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="3186f-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="3186f-131">Системе не удается найти путь, указанный параметром *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="3186f-131">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="3186f-132"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ недопустимого \_ диска)**</dt> <dt>0x8007000f</dt></span><span class="sxs-lookup"><span data-stu-id="3186f-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_DRIVE)**</dt> <dt>0x8007000f</dt></span></span> </dl>   | <span data-ttu-id="3186f-133">Файл, указанный параметром *imagePath* , находится на компакт-диске или DVD-диске.</span><span class="sxs-lookup"><span data-stu-id="3186f-133">The file specified by the *imagePath* parameter is on a CD-ROM or DVD-ROM.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="3186f-134"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ недопустимое \_ имя)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="3186f-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="3186f-135">Параметр *imagePath* содержит недопустимый символ (один из " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="3186f-135">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="3186f-136"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ Bad \_ PATHNAME)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="3186f-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="3186f-137">Параметр *imagePath* задает пустой или относительный путь.</span><span class="sxs-lookup"><span data-stu-id="3186f-137">Both the *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="3186f-138">По крайней мере один из параметров должен быть абсолютным путем.</span><span class="sxs-lookup"><span data-stu-id="3186f-138">At least one of the parameters must be an absolute path.</span></span><br/>                         |
| <dl> <span data-ttu-id="3186f-139"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ \_ переполнение буфера ошибки)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="3186f-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="3186f-140">Слишком длинный путь, указанный параметром *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="3186f-140">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="3186f-141">Длина пути должна быть меньше **максимального \_ пути** (260) символов.</span><span class="sxs-lookup"><span data-stu-id="3186f-141">The length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/>                |
| <dl> <span data-ttu-id="3186f-142"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ уже \_ существует)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="3186f-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="3186f-143">Файл, на который ссылается параметр *imagePath* , уже существует.</span><span class="sxs-lookup"><span data-stu-id="3186f-143">The file referenced by the *imagePath* parameter already exists.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="3186f-144"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (на \_ диске с ошибкой \_ Full)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="3186f-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="3186f-145">Для динамического расширяющего образа виртуального жесткого диска требуется по меньшей мере 8 МБ свободного места на томе узла.</span><span class="sxs-lookup"><span data-stu-id="3186f-145">The dynamically expanding virtual hard disk image needs at least 8 MB free on the host volume.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="3186f-146"><dt>**Виртуальная машина \_ \_Размер изображения \_ E \_ слишком \_ велик**</dt> <dt>0xA0040683</dt></span><span class="sxs-lookup"><span data-stu-id="3186f-146"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_LARGE**</dt> <dt>0xA0040683</dt></span></span> </dl>                | <span data-ttu-id="3186f-147">Значение параметра *size* должно быть меньше 2 088 960 МБ.</span><span class="sxs-lookup"><span data-stu-id="3186f-147">The *size* parameter must be less than 2,088,960 MB.</span></span> <span data-ttu-id="3186f-148">Если используется формат FAT16, значение параметра *size* должно быть меньше 2000 МБ.</span><span class="sxs-lookup"><span data-stu-id="3186f-148">If the format is FAT16, then the *size* parameter must be less than 2000 MB.</span></span><br/>                    |
| <dl> <span data-ttu-id="3186f-149"><dt>**Виртуальная машина \_ \_Размер образа \_ E \_ слишком \_ мал**</dt> <dt>0xA0040684</dt></span><span class="sxs-lookup"><span data-stu-id="3186f-149"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_SMALL**</dt> <dt>0xA0040684</dt></span></span> </dl>                | <span data-ttu-id="3186f-150">Образы виртуальных жестких дисков в формате неформатированного и FAT16 должны иметь по крайней мере 3 МБ.</span><span class="sxs-lookup"><span data-stu-id="3186f-150">Unformatted and FAT16 formatted virtual hard disk images must be at least 3 MB.</span></span> <span data-ttu-id="3186f-151">Образы виртуальных жестких дисков в формате FAT32 должны иметь не менее 514 МБ.</span><span class="sxs-lookup"><span data-stu-id="3186f-151">FAT32 formatted virtual hard disk images must be at least 514 MB.</span></span><br/>    |
| <dl> <span data-ttu-id="3186f-152"><dt>**Виртуальная машина \_ \_ \_ Слишком большой файл \_ E \_ для \_ тома**</dt> <dt>0xA0040679</dt></span><span class="sxs-lookup"><span data-stu-id="3186f-152"><dt>**VM\_E\_FILE\_TOO\_LARGE\_FOR\_VOLUME**</dt> <dt>0xA0040679</dt></span></span> </dl>          | <span data-ttu-id="3186f-153">Том узла не поддерживает файл такого размера.</span><span class="sxs-lookup"><span data-stu-id="3186f-153">The host volume cannot support a file this size.</span></span> <span data-ttu-id="3186f-154">Максимальный размер файла для тома FAT32 составляет 4 ГБ.</span><span class="sxs-lookup"><span data-stu-id="3186f-154">The maximum file size for a FAT32 volume is 4 GB.</span></span> <span data-ttu-id="3186f-155">Максимальный размер файла для тома FAT16 составляет 2 ГБ.</span><span class="sxs-lookup"><span data-stu-id="3186f-155">The maximum file size for a FAT16 volume is 2 GB.</span></span><br/> |
| <dl> <span data-ttu-id="3186f-156"><dt>**Виртуальная машина \_ \_Приложение E \_ завершает работу \_**</dt> <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="3186f-156"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                    | <span data-ttu-id="3186f-157">Невозможно создать виртуальный жесткий диск после начала работы приложения.</span><span class="sxs-lookup"><span data-stu-id="3186f-157">The virtual hard disk cannot be created after the application has started shutting down.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="3186f-158"><dt>**Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="3186f-158"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="3186f-159">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="3186f-159">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="3186f-160"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3186f-160"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="3186f-161">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="3186f-161">An unexpected error has occurred.</span></span><br/>                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="3186f-162">Требования</span><span class="sxs-lookup"><span data-stu-id="3186f-162">Requirements</span></span>



| <span data-ttu-id="3186f-163">Требование</span><span class="sxs-lookup"><span data-stu-id="3186f-163">Requirement</span></span> | <span data-ttu-id="3186f-164">Значение</span><span class="sxs-lookup"><span data-stu-id="3186f-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3186f-165">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3186f-165">Minimum supported client</span></span><br/> | <span data-ttu-id="3186f-166">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3186f-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3186f-167">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3186f-167">Minimum supported server</span></span><br/> | <span data-ttu-id="3186f-168">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3186f-168">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3186f-169">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="3186f-169">End of client support</span></span><br/>    | <span data-ttu-id="3186f-170">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3186f-170">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3186f-171">Продукт</span><span class="sxs-lookup"><span data-stu-id="3186f-171">Product</span></span><br/>                  | <span data-ttu-id="3186f-172">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3186f-172">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3186f-173">Header</span><span class="sxs-lookup"><span data-stu-id="3186f-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="3186f-174"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="3186f-174"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3186f-175">IID</span><span class="sxs-lookup"><span data-stu-id="3186f-175">IID</span></span><br/>                      | <span data-ttu-id="3186f-176">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="3186f-176">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="3186f-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3186f-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3186f-178">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="3186f-178">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

