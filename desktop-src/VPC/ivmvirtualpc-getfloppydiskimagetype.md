---
title: Метод Ивмвиртуалпк Жетфлоппидискимажетипе (Впккоминтерфацес. h)
description: Возвращает тип существующего файла образа гибкого диска.
ms.assetid: 34956a0c-1da0-4968-9a6c-c114d7037da1
keywords:
- Метод Жетфлоппидискимажетипе Virtual PC
- Метод Жетфлоппидискимажетипе Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, метод Жетфлоппидискимажетипе
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e5e2974f80865f8572f1153721cf10233fdb389
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137474"
---
# <a name="ivmvirtualpcgetfloppydiskimagetype-method"></a><span data-ttu-id="6c69c-106">Метод Ивмвиртуалпк:: Жетфлоппидискимажетипе</span><span class="sxs-lookup"><span data-stu-id="6c69c-106">IVMVirtualPC::GetFloppyDiskImageType method</span></span>

<span data-ttu-id="6c69c-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6c69c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6c69c-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6c69c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6c69c-109">Возвращает тип существующего файла образа гибкого диска.</span><span class="sxs-lookup"><span data-stu-id="6c69c-109">Retrieves the type of an existing floppy disk image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c69c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c69c-110">Syntax</span></span>


```C++
HRESULT GetFloppyDiskImageType(
  [in]          BSTR                  imagePath,
  [out, retval] VMFloppyDiskImageType *imageType
);
```



## <a name="parameters"></a><span data-ttu-id="6c69c-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c69c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c69c-112">*imagePath* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6c69c-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c69c-113">Полный путь к файлу образа диска.</span><span class="sxs-lookup"><span data-stu-id="6c69c-113">The full path to the disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="6c69c-114">*imageType* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6c69c-114">*imageType* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6c69c-115">Тип образа диска.</span><span class="sxs-lookup"><span data-stu-id="6c69c-115">The disk image type.</span></span> <span data-ttu-id="6c69c-116">Список значений см. в разделе [**вмфлоппидискимажетипе**](vmfloppydiskimagetype.md).</span><span class="sxs-lookup"><span data-stu-id="6c69c-116">For a list of values, see [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c69c-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c69c-117">Return value</span></span>

<span data-ttu-id="6c69c-118">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="6c69c-118">This method can return one of these values.</span></span>



| <span data-ttu-id="6c69c-119">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="6c69c-119">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="6c69c-120">Описание</span><span class="sxs-lookup"><span data-stu-id="6c69c-120">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c69c-121"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6c69c-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="6c69c-122">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="6c69c-122">The operation was successful.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="6c69c-123"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="6c69c-123"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="6c69c-124">Параметр *imagePath* или *ImageType* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6c69c-124">The *imagePath* or *imageType* parameter is **NULL**.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="6c69c-125"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ файл ошибки \_ не \_ найден)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="6c69c-125"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="6c69c-126">Системе не удается найти файл, указанный параметром *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="6c69c-126">The system cannot find the file specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="6c69c-127"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ путь ошибки \_ не \_ найден)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="6c69c-127"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="6c69c-128">Системе не удается найти путь, указанный параметром *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="6c69c-128">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="6c69c-129"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ недопустимое \_ имя)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="6c69c-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="6c69c-130">Параметр *imagePath* содержит недопустимый символ (один из " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="6c69c-130">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                  |
| <dl> <span data-ttu-id="6c69c-131"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ Bad \_ PATHNAME)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="6c69c-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="6c69c-132">Параметр *imagePath* указывает пустой или относительный путь.</span><span class="sxs-lookup"><span data-stu-id="6c69c-132">The *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="6c69c-133">Требуется абсолютный путь.</span><span class="sxs-lookup"><span data-stu-id="6c69c-133">An absolute path is required.</span></span><br/>                          |
| <dl> <span data-ttu-id="6c69c-134"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ \_ переполнение буфера ошибки)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="6c69c-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="6c69c-135">Слишком длинный путь, указанный параметром *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="6c69c-135">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="6c69c-136">Длина пути должна быть меньше 260 символов.</span><span class="sxs-lookup"><span data-stu-id="6c69c-136">The length of the path must be less than 260 characters.</span></span><br/> |
| <dl> <span data-ttu-id="6c69c-137"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6c69c-137"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="6c69c-138">Файл, указанный в параметре *imagePath* , не является образом дискеты или произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="6c69c-138">The file specified by *imagePath* is not a floppy image, or an unexpected error has occurred.</span></span><br/>                         |
| <dl> <span data-ttu-id="6c69c-139"><dt>**Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="6c69c-139"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="6c69c-140">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="6c69c-140">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="6c69c-141">Требования</span><span class="sxs-lookup"><span data-stu-id="6c69c-141">Requirements</span></span>



| <span data-ttu-id="6c69c-142">Требование</span><span class="sxs-lookup"><span data-stu-id="6c69c-142">Requirement</span></span> | <span data-ttu-id="6c69c-143">Значение</span><span class="sxs-lookup"><span data-stu-id="6c69c-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c69c-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c69c-144">Minimum supported client</span></span><br/> | <span data-ttu-id="6c69c-145">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6c69c-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6c69c-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c69c-146">Minimum supported server</span></span><br/> | <span data-ttu-id="6c69c-147">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6c69c-147">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6c69c-148">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="6c69c-148">End of client support</span></span><br/>    | <span data-ttu-id="6c69c-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6c69c-149">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6c69c-150">Продукт</span><span class="sxs-lookup"><span data-stu-id="6c69c-150">Product</span></span><br/>                  | <span data-ttu-id="6c69c-151">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6c69c-151">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6c69c-152">Header</span><span class="sxs-lookup"><span data-stu-id="6c69c-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c69c-153"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c69c-153"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6c69c-154">IID</span><span class="sxs-lookup"><span data-stu-id="6c69c-154">IID</span></span><br/>                      | <span data-ttu-id="6c69c-155">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="6c69c-155">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="6c69c-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c69c-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c69c-157">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="6c69c-157">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

