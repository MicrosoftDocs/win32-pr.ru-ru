---
description: Сжимает логический файл подкачки (или каталог), указанный в пути объекта (этот метод является расширенной версией метода сжатия).
ms.assetid: ea99367b-4d5e-4cd2-aa89-d250d1161f8f
ms.tgt_platform: multiple
title: Метод Компрессекс класса Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2823d12fc474b5a5023890596a116062d94a045f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895481"
---
# <a name="compressex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="41165-103">Метод Компрессекс \_ класса файла подкачки Win32</span><span class="sxs-lookup"><span data-stu-id="41165-103">CompressEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="41165-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) компрессекс сжимает логический файл подкачки (или каталог), указанный в пути к объекту (этот метод является расширенной версией метода [**сжатия**](compress-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="41165-104">The **CompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical paging file (or directory) specified in the object path (this method is an extended version of the [**Compress**](compress-method-in-class-win32-directory.md) method).</span></span>

<span data-ttu-id="41165-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="41165-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="41165-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="41165-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="41165-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41165-107">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="41165-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="41165-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41165-109">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="41165-109">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41165-110">Имя файла или каталога, в котором произошел сбой метода **компрессекс** .</span><span class="sxs-lookup"><span data-stu-id="41165-110">Name of the file or directory where the **CompressEx** method failed.</span></span> <span data-ttu-id="41165-111">Если метод выполнен, этот параметр имеет **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="41165-111">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="41165-112">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="41165-112">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="41165-113">Имя дочернего файла или каталога, который будет использоваться в качестве отправной точки для **компрессекс**.</span><span class="sxs-lookup"><span data-stu-id="41165-113">Names the child file or directory to use as a starting point for **CompressEx**.</span></span> <span data-ttu-id="41165-114">Параметр *StartFileName* обычно представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="41165-114">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="41165-115">Если этот параметр имеет **значение NULL**, операция выполняется над файлом или каталогом, указанным в вызове метода **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="41165-115">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="41165-116">*Рекурсивно* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="41165-116">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="41165-117">Если **значение — true**, изменение владельца будет применяться рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="41165-117">If **true**, the change of ownership will be applied recursively to the files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="41165-118">Для экземпляров файлов *рекурсивный* параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="41165-118">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41165-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41165-119">Return value</span></span>

<span data-ttu-id="41165-120">Возвращает значение 0 (ноль), если файл был успешно сжат, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="41165-120">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="41165-121">**0**</span><span class="sxs-lookup"><span data-stu-id="41165-121">**0**</span></span>
</dt> <dd>

<span data-ttu-id="41165-122">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="41165-122">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="41165-123">**2**</span><span class="sxs-lookup"><span data-stu-id="41165-123">**2**</span></span>
</dt> <dd>

<span data-ttu-id="41165-124">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="41165-124">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="41165-125">**8**</span><span class="sxs-lookup"><span data-stu-id="41165-125">**8**</span></span>
</dt> <dd>

<span data-ttu-id="41165-126">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="41165-126">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="41165-127">**9**</span><span class="sxs-lookup"><span data-stu-id="41165-127">**9**</span></span>
</dt> <dd>

<span data-ttu-id="41165-128">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="41165-128">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="41165-129">**10**</span><span class="sxs-lookup"><span data-stu-id="41165-129">**10**</span></span>
</dt> <dd>

<span data-ttu-id="41165-130">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="41165-130">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="41165-131">**11**</span><span class="sxs-lookup"><span data-stu-id="41165-131">**11**</span></span>
</dt> <dd>

<span data-ttu-id="41165-132">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="41165-132">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="41165-133">**12**</span><span class="sxs-lookup"><span data-stu-id="41165-133">**12**</span></span>
</dt> <dd>

<span data-ttu-id="41165-134">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="41165-134">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="41165-135">**13**</span><span class="sxs-lookup"><span data-stu-id="41165-135">**13**</span></span>
</dt> <dd>

<span data-ttu-id="41165-136">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="41165-136">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="41165-137">**14**</span><span class="sxs-lookup"><span data-stu-id="41165-137">**14**</span></span>
</dt> <dd>

<span data-ttu-id="41165-138">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="41165-138">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="41165-139">**15**</span><span class="sxs-lookup"><span data-stu-id="41165-139">**15**</span></span>
</dt> <dd>

<span data-ttu-id="41165-140">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="41165-140">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="41165-141">**16**</span><span class="sxs-lookup"><span data-stu-id="41165-141">**16**</span></span>
</dt> <dd>

<span data-ttu-id="41165-142">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="41165-142">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="41165-143">**17**</span><span class="sxs-lookup"><span data-stu-id="41165-143">**17**</span></span>
</dt> <dd>

<span data-ttu-id="41165-144">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="41165-144">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="41165-145">**открыт**</span><span class="sxs-lookup"><span data-stu-id="41165-145">**21**</span></span>
</dt> <dd>

<span data-ttu-id="41165-146">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="41165-146">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41165-147">Требования</span><span class="sxs-lookup"><span data-stu-id="41165-147">Requirements</span></span>



| <span data-ttu-id="41165-148">Требование</span><span class="sxs-lookup"><span data-stu-id="41165-148">Requirement</span></span> | <span data-ttu-id="41165-149">Значение</span><span class="sxs-lookup"><span data-stu-id="41165-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41165-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41165-150">Minimum supported client</span></span><br/> | <span data-ttu-id="41165-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41165-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41165-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41165-152">Minimum supported server</span></span><br/> | <span data-ttu-id="41165-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41165-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41165-154">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="41165-154">Namespace</span></span><br/>                | <span data-ttu-id="41165-155">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="41165-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="41165-156">MOF</span><span class="sxs-lookup"><span data-stu-id="41165-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41165-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41165-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="41165-158">DLL</span><span class="sxs-lookup"><span data-stu-id="41165-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41165-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41165-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41165-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41165-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="41165-161">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="41165-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="41165-162">**\_Файл подкачки Win32**</span><span class="sxs-lookup"><span data-stu-id="41165-162">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

