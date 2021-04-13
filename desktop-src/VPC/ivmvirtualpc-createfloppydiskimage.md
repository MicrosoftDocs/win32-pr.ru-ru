---
title: Метод Ивмвиртуалпк Креатефлоппидискимаже (Впккоминтерфацес. h)
description: Создает файл образа гибкого диска.
ms.assetid: 474e86a4-2019-41bd-9361-e494291d1961
keywords:
- Метод Креатефлоппидискимаже Virtual PC
- Метод Креатефлоппидискимаже Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, метод Креатефлоппидискимаже
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateFloppyDiskImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ff94ba5cb922aeb75f4effac413bb83b080b3fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492042"
---
# <a name="ivmvirtualpccreatefloppydiskimage-method"></a><span data-ttu-id="d4504-106">Метод Ивмвиртуалпк:: Креатефлоппидискимаже</span><span class="sxs-lookup"><span data-stu-id="d4504-106">IVMVirtualPC::CreateFloppyDiskImage method</span></span>

<span data-ttu-id="d4504-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d4504-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d4504-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d4504-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d4504-109">Создает файл образа гибкого диска.</span><span class="sxs-lookup"><span data-stu-id="d4504-109">Creates a floppy disk image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4504-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4504-110">Syntax</span></span>


```C++
HRESULT CreateFloppyDiskImage(
  [in] BSTR                  imagePath,
  [in] VMFloppyDiskImageType imageType
);
```



## <a name="parameters"></a><span data-ttu-id="d4504-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4504-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4504-112">*imagePath* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4504-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4504-113">Полный путь к новому файлу образа диска.</span><span class="sxs-lookup"><span data-stu-id="d4504-113">The full path to the new disk image file.</span></span> <span data-ttu-id="d4504-114">Содержащаяся папка будет создана, если она не существует.</span><span class="sxs-lookup"><span data-stu-id="d4504-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="d4504-115">*imageType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d4504-115">*imageType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4504-116">Тип создаваемого образа гибкого диска.</span><span class="sxs-lookup"><span data-stu-id="d4504-116">The type of floppy disk image to create.</span></span> <span data-ttu-id="d4504-117">Поддерживаются только **вмфлоппидискимаже \_ ловденсити** (1) и **вмфлоппидискимаже \_ хигхденсити** (2).</span><span class="sxs-lookup"><span data-stu-id="d4504-117">Only **vmFloppyDiskImage\_LowDensity** (1) and **vmFloppyDiskImage\_HighDensity** (2) are supported.</span></span> <span data-ttu-id="d4504-118">См. [**вмфлоппидискимажетипе**](vmfloppydiskimagetype.md).</span><span class="sxs-lookup"><span data-stu-id="d4504-118">See [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4504-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4504-119">Return value</span></span>

<span data-ttu-id="d4504-120">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="d4504-120">This method can return one of these values.</span></span>



| <span data-ttu-id="d4504-121">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="d4504-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="d4504-122">Описание</span><span class="sxs-lookup"><span data-stu-id="d4504-122">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d4504-123"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="d4504-123"><dt>**S\_OK**</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="d4504-124">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d4504-124">The operation was successful.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="d4504-125"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="d4504-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="d4504-126">Параметр *imagePath* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d4504-126">The *imagePath* parameter is **NULL**.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="d4504-127"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="d4504-127"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="d4504-128">Параметр *imageType* не [**вмфлоппидискимаже \_ ловденсити**](vmfloppydiskimagetype.md) (1) или **вмфлоппидискимаже \_ хигхденсити** (2).</span><span class="sxs-lookup"><span data-stu-id="d4504-128">The *imageType* parameter is not [**vmFloppyDiskImage\_LowDensity**](vmfloppydiskimagetype.md) (1) or **vmFloppyDiskImage\_HighDensity** (2).</span></span><br/> |
| <dl> <span data-ttu-id="d4504-129"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ путь ошибки \_ не \_ найден)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="d4504-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="d4504-130">Системе не удается найти путь, указанный параметром *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="d4504-130">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="d4504-131"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ недопустимое \_ имя)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="d4504-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="d4504-132">Параметр *imagePath* содержит недопустимый символ (один из " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="d4504-132">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                           |
| <dl> <span data-ttu-id="d4504-133"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ Bad \_ PATHNAME)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="d4504-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="d4504-134">Параметр *imagePath* указывает пустой или относительный путь.</span><span class="sxs-lookup"><span data-stu-id="d4504-134">The *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="d4504-135">Требуется абсолютный путь.</span><span class="sxs-lookup"><span data-stu-id="d4504-135">An absolute path is required.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="d4504-136"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ \_ переполнение буфера ошибки)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="d4504-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="d4504-137">Слишком длинный путь, указанный параметром *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="d4504-137">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="d4504-138">Длина пути должна быть меньше 260 символов.</span><span class="sxs-lookup"><span data-stu-id="d4504-138">The length of the path must be less than 260 characters.</span></span><br/>                          |
| <dl> <span data-ttu-id="d4504-139"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ уже \_ существует)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="d4504-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="d4504-140">Файл, на который ссылается параметр *imagePath* , уже существует.</span><span class="sxs-lookup"><span data-stu-id="d4504-140">The file referenced by the parameter *imagePath* already exists.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="d4504-141"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (на \_ диске с ошибкой \_ Full)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="d4504-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="d4504-142">Недостаточно места на томе узла для создания образа виртуального гибкого диска.</span><span class="sxs-lookup"><span data-stu-id="d4504-142">There is insufficient space on the host volume to create the virtual floppy disk image.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="d4504-143"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d4504-143"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="d4504-144">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d4504-144">An unexpected error occurred.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="d4504-145"><dt>**Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="d4504-145"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="d4504-146">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="d4504-146">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                           |



 

## <a name="requirements"></a><span data-ttu-id="d4504-147">Требования</span><span class="sxs-lookup"><span data-stu-id="d4504-147">Requirements</span></span>



| <span data-ttu-id="d4504-148">Требование</span><span class="sxs-lookup"><span data-stu-id="d4504-148">Requirement</span></span> | <span data-ttu-id="d4504-149">Значение</span><span class="sxs-lookup"><span data-stu-id="d4504-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4504-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4504-150">Minimum supported client</span></span><br/> | <span data-ttu-id="d4504-151">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d4504-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d4504-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4504-152">Minimum supported server</span></span><br/> | <span data-ttu-id="d4504-153">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d4504-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d4504-154">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d4504-154">End of client support</span></span><br/>    | <span data-ttu-id="d4504-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d4504-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d4504-156">Продукт</span><span class="sxs-lookup"><span data-stu-id="d4504-156">Product</span></span><br/>                  | <span data-ttu-id="d4504-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d4504-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d4504-158">Header</span><span class="sxs-lookup"><span data-stu-id="d4504-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4504-159"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4504-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d4504-160">IID</span><span class="sxs-lookup"><span data-stu-id="d4504-160">IID</span></span><br/>                      | <span data-ttu-id="d4504-161">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="d4504-161">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="d4504-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4504-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4504-163">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="d4504-163">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

