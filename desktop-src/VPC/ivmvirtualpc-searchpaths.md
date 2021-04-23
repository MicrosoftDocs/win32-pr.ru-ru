---
title: Свойство Сеарчпасс Ивмвиртуалпк (Впккоминтерфацес. h)
description: Пути файловой системы, используемые для поиска файлов, связанных с Windows Virtual PC.
ms.assetid: 2a2deee5-7e6b-4b90-8ce9-0b0dbeef0f30
keywords:
- Сеарчпасс свойство Virtual PC
- Сеарчпасс свойство Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, свойство Сеарчпасс
topic_type:
- apiref
api_name:
- IVMVirtualPC.SearchPaths
- IVMVirtualPC.get_SearchPaths
- IVMVirtualPC.put_SearchPaths
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 287eb07bc9205f9b6f0851bd8809f9a49dcf3242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800959"
---
# <a name="ivmvirtualpcsearchpaths-property"></a><span data-ttu-id="aa7ff-106">Свойство Ивмвиртуалпк:: Сеарчпасс</span><span class="sxs-lookup"><span data-stu-id="aa7ff-106">IVMVirtualPC::SearchPaths property</span></span>

<span data-ttu-id="aa7ff-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="aa7ff-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="aa7ff-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="aa7ff-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="aa7ff-109">Извлекает и задает пути файловой системы, используемые для поиска файлов, связанных с Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="aa7ff-109">Retrieves and sets the file system paths that are used to find files associated with Windows Virtual PC.</span></span>

<span data-ttu-id="aa7ff-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="aa7ff-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa7ff-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa7ff-111">Syntax</span></span>


```C++
HRESULT put_SearchPaths(
  [in]          VARIANT searchPaths
);

HRESULT get_SearchPaths(
  [out, retval] VARIANT *searchPaths
);
```



## <a name="property-value"></a><span data-ttu-id="aa7ff-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="aa7ff-112">Property value</span></span>

<span data-ttu-id="aa7ff-113">Задает массив SafeArray, содержащий путь к файловой системе для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="aa7ff-113">Specifies a safearray containing a file system path for each entry.</span></span>

## <a name="error-codes"></a><span data-ttu-id="aa7ff-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="aa7ff-114">Error codes</span></span>



| <span data-ttu-id="aa7ff-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="aa7ff-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="aa7ff-116">Значение</span><span class="sxs-lookup"><span data-stu-id="aa7ff-116">Meaning</span></span>                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aa7ff-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="aa7ff-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="aa7ff-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="aa7ff-118">The operation was successful.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="aa7ff-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="aa7ff-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="aa7ff-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="aa7ff-120">The parameter is **NULL**.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="aa7ff-121"><dt>Д \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="aa7ff-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="aa7ff-122">Параметр *сеарчпасс* недопустим и не может быть проанализирован в массив путей.</span><span class="sxs-lookup"><span data-stu-id="aa7ff-122">The *searchPaths* parameter is not valid and could not be parsed into an array of paths.</span></span><br/>                                    |
| <dl> <span data-ttu-id="aa7ff-123"><dt>Значение HRESULT \_ ИЗ \_ Win32 ( \_ файл ошибки \_ не \_ найден)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="aa7ff-123"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="aa7ff-124">Системе не удается найти каталог, указанный в параметре *сеарчпасс* .</span><span class="sxs-lookup"><span data-stu-id="aa7ff-124">The system cannot find a directory specified in the *searchPaths* parameter.</span></span><br/>                                                |
| <dl> <span data-ttu-id="aa7ff-125"><dt>Значение HRESULT \_ ИЗ \_ Win32 ( \_ путь ошибки \_ не \_ найден)</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="aa7ff-125"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="aa7ff-126">Системе не удается найти путь, указанный параметром *сеарчпасс* .</span><span class="sxs-lookup"><span data-stu-id="aa7ff-126">The system cannot find a path specified by the *searchPaths* parameter.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="aa7ff-127"><dt>Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ недопустимое \_ имя)</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="aa7ff-127"><dt>HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="aa7ff-128">Путь, указанный в параметре *сеарчпасс* , содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="aa7ff-128">A path specified in the *searchPaths* parameter contains illegal characters.</span></span> <span data-ttu-id="aa7ff-129">Недопустимые символы " \* ? <>/ \| ": ".</span><span class="sxs-lookup"><span data-stu-id="aa7ff-129">The illegal characters are "\*?<>/\|":".</span></span><br/> |
| <dl> <span data-ttu-id="aa7ff-130"><dt>Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ Bad \_ PATHNAME)</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="aa7ff-130"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="aa7ff-131">Путь, содержащийся в параметре *сеарчпасс* , указывает пустой или относительный путь.</span><span class="sxs-lookup"><span data-stu-id="aa7ff-131">A path contained in the *searchPaths* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="aa7ff-132">Требуется абсолютный путь.</span><span class="sxs-lookup"><span data-stu-id="aa7ff-132">An absolute path is required.</span></span><br/>          |
| <dl> <span data-ttu-id="aa7ff-133"><dt>Значение HRESULT \_ ИЗ \_ Win32 ( \_ \_ переполнение буфера ошибки)</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="aa7ff-133"><dt>HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="aa7ff-134">Путь, указанный в параметре *сеарчпасс* , слишком длинный.</span><span class="sxs-lookup"><span data-stu-id="aa7ff-134">The path specified in the *searchPaths* parameter is too long.</span></span> <span data-ttu-id="aa7ff-135">Длина пути должна быть меньше 260 символов.</span><span class="sxs-lookup"><span data-stu-id="aa7ff-135">The length of the path must be less than 260 characters.</span></span><br/>     |
| <dl> <span data-ttu-id="aa7ff-136"><dt>Виртуальная машина \_ E \_ преф \_ не \_ Найдено</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="aa7ff-136"><dt>VM\_E\_PREF\_NOT\_FOUND</dt> <dt>0xA0040300</dt></span></span> </dl>                       | <span data-ttu-id="aa7ff-137">Предпочтение не найдено.</span><span class="sxs-lookup"><span data-stu-id="aa7ff-137">The preference was not found.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="aa7ff-138"><dt>Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="aa7ff-138"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="aa7ff-139">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="aa7ff-139">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                        |
| <dl> <span data-ttu-id="aa7ff-140"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="aa7ff-140"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="aa7ff-141">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="aa7ff-141">An unexpected error has occurred.</span></span><br/>                                                                                           |



## <a name="requirements"></a><span data-ttu-id="aa7ff-142">Требования</span><span class="sxs-lookup"><span data-stu-id="aa7ff-142">Requirements</span></span>



| <span data-ttu-id="aa7ff-143">Требование</span><span class="sxs-lookup"><span data-stu-id="aa7ff-143">Requirement</span></span> | <span data-ttu-id="aa7ff-144">Значение</span><span class="sxs-lookup"><span data-stu-id="aa7ff-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa7ff-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa7ff-145">Minimum supported client</span></span><br/> | <span data-ttu-id="aa7ff-146">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="aa7ff-146">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aa7ff-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa7ff-147">Minimum supported server</span></span><br/> | <span data-ttu-id="aa7ff-148">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="aa7ff-148">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="aa7ff-149">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="aa7ff-149">End of client support</span></span><br/>    | <span data-ttu-id="aa7ff-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="aa7ff-150">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="aa7ff-151">Продукт</span><span class="sxs-lookup"><span data-stu-id="aa7ff-151">Product</span></span><br/>                  | <span data-ttu-id="aa7ff-152">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="aa7ff-152">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="aa7ff-153">Header</span><span class="sxs-lookup"><span data-stu-id="aa7ff-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa7ff-154"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa7ff-154"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="aa7ff-155">IID</span><span class="sxs-lookup"><span data-stu-id="aa7ff-155">IID</span></span><br/>                      | <span data-ttu-id="aa7ff-156">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="aa7ff-156">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="aa7ff-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa7ff-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa7ff-158">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="aa7ff-158">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

