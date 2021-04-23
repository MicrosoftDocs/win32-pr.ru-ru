---
description: Распаковывает логический файл кодека (или каталог), указанный в пути объекта. Этот метод является расширенной версией метода uncompressия.
ms.assetid: 257c69fa-c4f7-48be-8317-55db4b01601b
ms.tgt_platform: multiple
title: Метод Ункомпрессекс класса Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 547062a85336681b78a6081646801e78e4713e3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539242"
---
# <a name="uncompressex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="6a288-104">Метод Ункомпрессекс \_ класса Win32 кодекфиле</span><span class="sxs-lookup"><span data-stu-id="6a288-104">UncompressEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="6a288-105">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) ункомпрессекс распаковывает логический файл кодека (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="6a288-105">The **UncompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical codec file (or directory) specified in the object path.</span></span> <span data-ttu-id="6a288-106">Этот метод является расширенной версией метода [**uncompressия**](uncompress-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="6a288-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="6a288-107">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="6a288-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6a288-108">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6a288-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a288-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a288-109">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="6a288-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a288-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a288-111">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6a288-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a288-112">Имя файла или каталога, в котором произошел сбой метода **ункомпрессекс** .</span><span class="sxs-lookup"><span data-stu-id="6a288-112">Name of the file or directory where the **UncompressEx** method failed.</span></span> <span data-ttu-id="6a288-113">Если метод завершится с ошибкой, этот параметр будет иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="6a288-113">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="6a288-114">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="6a288-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6a288-115">Имя дочернего файла или каталога, который будет использоваться в качестве отправной точки для **ункомпрессекс**. Параметр *StartFileName* обычно представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="6a288-115">Names the child file or directory to use as a starting point for **UncompressEx**.The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="6a288-116">Если этот параметр имеет **значение NULL**, операция выполняется над файлом или каталогом, указанным в вызове метода **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="6a288-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="6a288-117">*Рекурсивно* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="6a288-117">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6a288-118">Если **значение — true**, изменение владельца будет применяться рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="6a288-118">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="6a288-119">Примечание. для экземпляров файлов входной параметр *recursive* не учитывается.</span><span class="sxs-lookup"><span data-stu-id="6a288-119">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a288-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6a288-120">Return value</span></span>

<span data-ttu-id="6a288-121">Возвращает целочисленное значение 0 (ноль), если файл был успешно распакован, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="6a288-121">Returns an integer value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="6a288-122">**0**</span><span class="sxs-lookup"><span data-stu-id="6a288-122">**0**</span></span>
</dt> <dd>

<span data-ttu-id="6a288-123">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="6a288-123">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="6a288-124">**2**</span><span class="sxs-lookup"><span data-stu-id="6a288-124">**2**</span></span>
</dt> <dd>

<span data-ttu-id="6a288-125">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="6a288-125">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="6a288-126">**8**</span><span class="sxs-lookup"><span data-stu-id="6a288-126">**8**</span></span>
</dt> <dd>

<span data-ttu-id="6a288-127">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="6a288-127">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="6a288-128">**9**</span><span class="sxs-lookup"><span data-stu-id="6a288-128">**9**</span></span>
</dt> <dd>

<span data-ttu-id="6a288-129">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="6a288-129">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6a288-130">**10**</span><span class="sxs-lookup"><span data-stu-id="6a288-130">**10**</span></span>
</dt> <dd>

<span data-ttu-id="6a288-131">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="6a288-131">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="6a288-132">**11**</span><span class="sxs-lookup"><span data-stu-id="6a288-132">**11**</span></span>
</dt> <dd>

<span data-ttu-id="6a288-133">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="6a288-133">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="6a288-134">**12**</span><span class="sxs-lookup"><span data-stu-id="6a288-134">**12**</span></span>
</dt> <dd>

<span data-ttu-id="6a288-135">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="6a288-135">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="6a288-136">**13**</span><span class="sxs-lookup"><span data-stu-id="6a288-136">**13**</span></span>
</dt> <dd>

<span data-ttu-id="6a288-137">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="6a288-137">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="6a288-138">**14**</span><span class="sxs-lookup"><span data-stu-id="6a288-138">**14**</span></span>
</dt> <dd>

<span data-ttu-id="6a288-139">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="6a288-139">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="6a288-140">**15**</span><span class="sxs-lookup"><span data-stu-id="6a288-140">**15**</span></span>
</dt> <dd>

<span data-ttu-id="6a288-141">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="6a288-141">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="6a288-142">**16**</span><span class="sxs-lookup"><span data-stu-id="6a288-142">**16**</span></span>
</dt> <dd>

<span data-ttu-id="6a288-143">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="6a288-143">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6a288-144">**17**</span><span class="sxs-lookup"><span data-stu-id="6a288-144">**17**</span></span>
</dt> <dd>

<span data-ttu-id="6a288-145">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="6a288-145">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="6a288-146">**открыт**</span><span class="sxs-lookup"><span data-stu-id="6a288-146">**21**</span></span>
</dt> <dd>

<span data-ttu-id="6a288-147">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="6a288-147">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6a288-148">Требования</span><span class="sxs-lookup"><span data-stu-id="6a288-148">Requirements</span></span>



| <span data-ttu-id="6a288-149">Требование</span><span class="sxs-lookup"><span data-stu-id="6a288-149">Requirement</span></span> | <span data-ttu-id="6a288-150">Значение</span><span class="sxs-lookup"><span data-stu-id="6a288-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a288-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a288-151">Minimum supported client</span></span><br/> | <span data-ttu-id="6a288-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a288-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6a288-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a288-153">Minimum supported server</span></span><br/> | <span data-ttu-id="6a288-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a288-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6a288-155">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6a288-155">Namespace</span></span><br/>                | <span data-ttu-id="6a288-156">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6a288-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6a288-157">MOF</span><span class="sxs-lookup"><span data-stu-id="6a288-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a288-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a288-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a288-159">DLL</span><span class="sxs-lookup"><span data-stu-id="6a288-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a288-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a288-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a288-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a288-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="6a288-162">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6a288-162">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6a288-163">**\_Кодекфиле Win32**</span><span class="sxs-lookup"><span data-stu-id="6a288-163">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

