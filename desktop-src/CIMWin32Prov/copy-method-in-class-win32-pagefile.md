---
description: Копирует логический файл подкачки или каталог, указанный в пути к объекту, в расположение, указанное входным параметром.
ms.assetid: e1ff3e91-dc30-4849-b80a-8838b527ad63
ms.tgt_platform: multiple
title: Метод Copy класса Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bde9e0b5cf9b8ab88b5efa1c6aae58a9b8a54cfb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262658"
---
# <a name="copy-method-of-the-win32_pagefile-class"></a><span data-ttu-id="40d6b-103">Метод Copy \_ класса файла подкачки Win32</span><span class="sxs-lookup"><span data-stu-id="40d6b-103">Copy method of the Win32\_PageFile class</span></span>

<span data-ttu-id="40d6b-104">Метод класса **Copy** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) копирует логический файл подкачки или каталог, указанный в пути к объекту, в расположение, указанное параметром input.</span><span class="sxs-lookup"><span data-stu-id="40d6b-104">The **Copy** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical paging file or directory specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="40d6b-105">Копирование не поддерживается, если требуется перезапись существующего логического файла.</span><span class="sxs-lookup"><span data-stu-id="40d6b-105">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="40d6b-106">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="40d6b-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="40d6b-107">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="40d6b-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="40d6b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40d6b-108">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="40d6b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="40d6b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40d6b-110">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="40d6b-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40d6b-111">Полное имя копии файла (или каталога).</span><span class="sxs-lookup"><span data-stu-id="40d6b-111">Fully qualified name of the copy of the file (or directory).</span></span>

<span data-ttu-id="40d6b-112">Пример: c: \\ temp \\ невдиректори</span><span class="sxs-lookup"><span data-stu-id="40d6b-112">Example: c:\\temp\\newdirectory</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40d6b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="40d6b-113">Return value</span></span>

<span data-ttu-id="40d6b-114">Возвращает значение 0 (нуль), если файл был успешно скопирован, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="40d6b-114">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="40d6b-115">**0**</span><span class="sxs-lookup"><span data-stu-id="40d6b-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="40d6b-116">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="40d6b-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="40d6b-117">**2**</span><span class="sxs-lookup"><span data-stu-id="40d6b-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="40d6b-118">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="40d6b-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="40d6b-119">**8**</span><span class="sxs-lookup"><span data-stu-id="40d6b-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="40d6b-120">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="40d6b-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="40d6b-121">**9**</span><span class="sxs-lookup"><span data-stu-id="40d6b-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="40d6b-122">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="40d6b-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="40d6b-123">**10**</span><span class="sxs-lookup"><span data-stu-id="40d6b-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="40d6b-124">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="40d6b-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="40d6b-125">**11**</span><span class="sxs-lookup"><span data-stu-id="40d6b-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="40d6b-126">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="40d6b-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="40d6b-127">**12**</span><span class="sxs-lookup"><span data-stu-id="40d6b-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="40d6b-128">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="40d6b-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="40d6b-129">**13**</span><span class="sxs-lookup"><span data-stu-id="40d6b-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="40d6b-130">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="40d6b-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="40d6b-131">**14**</span><span class="sxs-lookup"><span data-stu-id="40d6b-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="40d6b-132">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="40d6b-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="40d6b-133">**15**</span><span class="sxs-lookup"><span data-stu-id="40d6b-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="40d6b-134">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="40d6b-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="40d6b-135">**16**</span><span class="sxs-lookup"><span data-stu-id="40d6b-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="40d6b-136">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="40d6b-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="40d6b-137">**17**</span><span class="sxs-lookup"><span data-stu-id="40d6b-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="40d6b-138">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="40d6b-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="40d6b-139">**открыт**</span><span class="sxs-lookup"><span data-stu-id="40d6b-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="40d6b-140">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="40d6b-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40d6b-141">Требования</span><span class="sxs-lookup"><span data-stu-id="40d6b-141">Requirements</span></span>



| <span data-ttu-id="40d6b-142">Требование</span><span class="sxs-lookup"><span data-stu-id="40d6b-142">Requirement</span></span> | <span data-ttu-id="40d6b-143">Значение</span><span class="sxs-lookup"><span data-stu-id="40d6b-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40d6b-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="40d6b-144">Minimum supported client</span></span><br/> | <span data-ttu-id="40d6b-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40d6b-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="40d6b-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="40d6b-146">Minimum supported server</span></span><br/> | <span data-ttu-id="40d6b-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40d6b-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="40d6b-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="40d6b-148">Namespace</span></span><br/>                | <span data-ttu-id="40d6b-149">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="40d6b-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="40d6b-150">MOF</span><span class="sxs-lookup"><span data-stu-id="40d6b-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40d6b-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40d6b-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="40d6b-152">DLL</span><span class="sxs-lookup"><span data-stu-id="40d6b-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40d6b-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40d6b-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40d6b-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40d6b-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="40d6b-155">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="40d6b-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="40d6b-156">**\_Файл подкачки Win32**</span><span class="sxs-lookup"><span data-stu-id="40d6b-156">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

