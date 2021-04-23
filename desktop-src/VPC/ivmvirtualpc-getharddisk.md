---
title: Метод Ивмвиртуалпк Жесарддиск (Впккоминтерфацес. h)
description: Извлекает объект, соответствующий существующему файлу образа диска.
ms.assetid: 648a3f8a-5114-4c14-b9a9-f175941333ab
keywords:
- Метод Жесарддиск Virtual PC
- Метод Жесарддиск Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, метод Жесарддиск
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 558d098b6745718830c63dd700c14febf4f6bed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989137"
---
# <a name="ivmvirtualpcgetharddisk-method"></a><span data-ttu-id="c171f-106">Метод Ивмвиртуалпк:: Жесарддиск</span><span class="sxs-lookup"><span data-stu-id="c171f-106">IVMVirtualPC::GetHardDisk method</span></span>

<span data-ttu-id="c171f-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c171f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c171f-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c171f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c171f-109">Извлекает объект, соответствующий существующему файлу образа диска.</span><span class="sxs-lookup"><span data-stu-id="c171f-109">Retrieves an object corresponding to an existing disk image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c171f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c171f-110">Syntax</span></span>


```C++
HRESULT GetHardDisk(
  [in]          BSTR        imagePath,
  [out, retval] IVMHardDisk **hardDisk
);
```



## <a name="parameters"></a><span data-ttu-id="c171f-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="c171f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c171f-112">*imagePath* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c171f-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c171f-113">Полный путь к существующему файлу образа диска.</span><span class="sxs-lookup"><span data-stu-id="c171f-113">The full path to an existing disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="c171f-114">*жесткого* \[ диска out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c171f-114">*hardDisk* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c171f-115">Объект [**ивмхарддиск**](ivmharddisk.md) , соответствующий этому образу диска.</span><span class="sxs-lookup"><span data-stu-id="c171f-115">An [**IVMHardDisk**](ivmharddisk.md) object corresponding to this disk image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c171f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c171f-116">Return value</span></span>

<span data-ttu-id="c171f-117">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="c171f-117">This method can return one of these values.</span></span>



| <span data-ttu-id="c171f-118">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="c171f-118">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="c171f-119">Описание</span><span class="sxs-lookup"><span data-stu-id="c171f-119">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c171f-120"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c171f-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="c171f-121">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c171f-121">The operation was successful.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="c171f-122"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="c171f-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="c171f-123">Параметр *imagePath* или *жесткого* диска имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c171f-123">The *imagePath* or *hardDisk* parameter is **NULL**.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="c171f-124"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ файл ошибки \_ не \_ найден)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="c171f-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="c171f-125">Системе не удается найти файл, указанный параметром *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="c171f-125">The system cannot find the file specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="c171f-126"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ путь ошибки \_ не \_ найден)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="c171f-126"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="c171f-127">Системе не удается найти путь, указанный параметром *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="c171f-127">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="c171f-128"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ недопустимое \_ имя)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="c171f-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="c171f-129">Параметр *imagePath* содержит недопустимый символ (один из " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="c171f-129">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                  |
| <dl> <span data-ttu-id="c171f-130"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ Bad \_ PATHNAME)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="c171f-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="c171f-131">Параметр *imagePath* указывает пустой или относительный путь.</span><span class="sxs-lookup"><span data-stu-id="c171f-131">The *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="c171f-132">Требуется абсолютный путь.</span><span class="sxs-lookup"><span data-stu-id="c171f-132">An absolute path is required.</span></span><br/>                          |
| <dl> <span data-ttu-id="c171f-133"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ \_ переполнение буфера ошибки)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="c171f-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="c171f-134">Слишком длинный путь, указанный параметром *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="c171f-134">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="c171f-135">Длина пути должна быть меньше 260 символов.</span><span class="sxs-lookup"><span data-stu-id="c171f-135">The length of the path must be less than 260 characters.</span></span><br/> |
| <dl> <span data-ttu-id="c171f-136"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c171f-136"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="c171f-137">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c171f-137">An unexpected error has occurred.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="c171f-138"><dt>**Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="c171f-138"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="c171f-139">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="c171f-139">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="c171f-140">Требования</span><span class="sxs-lookup"><span data-stu-id="c171f-140">Requirements</span></span>



| <span data-ttu-id="c171f-141">Требование</span><span class="sxs-lookup"><span data-stu-id="c171f-141">Requirement</span></span> | <span data-ttu-id="c171f-142">Значение</span><span class="sxs-lookup"><span data-stu-id="c171f-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c171f-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c171f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="c171f-144">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c171f-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c171f-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c171f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="c171f-146">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c171f-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c171f-147">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c171f-147">End of client support</span></span><br/>    | <span data-ttu-id="c171f-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c171f-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c171f-149">Продукт</span><span class="sxs-lookup"><span data-stu-id="c171f-149">Product</span></span><br/>                  | <span data-ttu-id="c171f-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c171f-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c171f-151">Header</span><span class="sxs-lookup"><span data-stu-id="c171f-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="c171f-152"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="c171f-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c171f-153">IID</span><span class="sxs-lookup"><span data-stu-id="c171f-153">IID</span></span><br/>                      | <span data-ttu-id="c171f-154">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="c171f-154">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="c171f-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c171f-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c171f-156">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="c171f-156">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

