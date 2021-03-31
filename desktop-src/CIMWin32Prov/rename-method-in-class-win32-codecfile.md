---
description: Переименовывает файл кодека, указанный в пути объекта.
ms.assetid: fd6ce02c-d513-4643-ac27-313c32732f1e
ms.tgt_platform: multiple
title: Метод Rename класса Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a4eb931a0155518ad9644ebb1cce0b604be80602
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990711"
---
# <a name="rename-method-of-the-win32_codecfile-class"></a><span data-ttu-id="585ba-103">Метод Rename класса Win32 \_ кодекфиле</span><span class="sxs-lookup"><span data-stu-id="585ba-103">Rename method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="585ba-104">Метод класса **Rename** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) переименовывает файл кодека, указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="585ba-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames the codec file specified in the object path.</span></span> <span data-ttu-id="585ba-105">Переименование не поддерживается, если место назначения находится на другом диске или требуется перезапись существующего логического файла.</span><span class="sxs-lookup"><span data-stu-id="585ba-105">A rename is not supported if the destination is on another drive or if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="585ba-106">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="585ba-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="585ba-107">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="585ba-107">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="585ba-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="585ba-108">Syntax</span></span>


```mof
uint32 Rename(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="585ba-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="585ba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="585ba-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="585ba-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="585ba-111">Полное новое имя файла (или каталога).</span><span class="sxs-lookup"><span data-stu-id="585ba-111">Fully qualified new name of the file (or directory).</span></span> <span data-ttu-id="585ba-112">Пример: c: \\ temp \\newfile.txt.</span><span class="sxs-lookup"><span data-stu-id="585ba-112">Example: c:\\temp\\newfile.txt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="585ba-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="585ba-113">Return value</span></span>

<span data-ttu-id="585ba-114">Возвращает целочисленное значение 0 (ноль), если файл был успешно переименован, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="585ba-114">Returns an integer value of 0 (zero) if the file was successfully renamed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="585ba-115">**0**</span><span class="sxs-lookup"><span data-stu-id="585ba-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="585ba-116">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="585ba-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="585ba-117">**2**</span><span class="sxs-lookup"><span data-stu-id="585ba-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="585ba-118">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="585ba-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="585ba-119">**8**</span><span class="sxs-lookup"><span data-stu-id="585ba-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="585ba-120">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="585ba-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="585ba-121">**9**</span><span class="sxs-lookup"><span data-stu-id="585ba-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="585ba-122">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="585ba-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="585ba-123">**10**</span><span class="sxs-lookup"><span data-stu-id="585ba-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="585ba-124">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="585ba-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="585ba-125">**11**</span><span class="sxs-lookup"><span data-stu-id="585ba-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="585ba-126">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="585ba-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="585ba-127">**12**</span><span class="sxs-lookup"><span data-stu-id="585ba-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="585ba-128">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="585ba-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="585ba-129">**13**</span><span class="sxs-lookup"><span data-stu-id="585ba-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="585ba-130">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="585ba-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="585ba-131">**14**</span><span class="sxs-lookup"><span data-stu-id="585ba-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="585ba-132">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="585ba-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="585ba-133">**15**</span><span class="sxs-lookup"><span data-stu-id="585ba-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="585ba-134">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="585ba-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="585ba-135">**16**</span><span class="sxs-lookup"><span data-stu-id="585ba-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="585ba-136">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="585ba-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="585ba-137">**17**</span><span class="sxs-lookup"><span data-stu-id="585ba-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="585ba-138">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="585ba-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="585ba-139">**открыт**</span><span class="sxs-lookup"><span data-stu-id="585ba-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="585ba-140">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="585ba-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="585ba-141">Требования</span><span class="sxs-lookup"><span data-stu-id="585ba-141">Requirements</span></span>



| <span data-ttu-id="585ba-142">Требование</span><span class="sxs-lookup"><span data-stu-id="585ba-142">Requirement</span></span> | <span data-ttu-id="585ba-143">Значение</span><span class="sxs-lookup"><span data-stu-id="585ba-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="585ba-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="585ba-144">Minimum supported client</span></span><br/> | <span data-ttu-id="585ba-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="585ba-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="585ba-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="585ba-146">Minimum supported server</span></span><br/> | <span data-ttu-id="585ba-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="585ba-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="585ba-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="585ba-148">Namespace</span></span><br/>                | <span data-ttu-id="585ba-149">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="585ba-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="585ba-150">MOF</span><span class="sxs-lookup"><span data-stu-id="585ba-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="585ba-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="585ba-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="585ba-152">DLL</span><span class="sxs-lookup"><span data-stu-id="585ba-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="585ba-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="585ba-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="585ba-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="585ba-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="585ba-155">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="585ba-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="585ba-156">**\_Кодекфиле Win32**</span><span class="sxs-lookup"><span data-stu-id="585ba-156">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

