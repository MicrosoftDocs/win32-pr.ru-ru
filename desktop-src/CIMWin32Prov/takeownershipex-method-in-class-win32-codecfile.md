---
description: Получает владение логическим файлом кодека, указанным в пути объекта. Этот метод является расширенной версией метода Такеовнершип.
ms.assetid: 8f3b495a-f654-4818-b0ea-dc88819d72af
ms.tgt_platform: multiple
title: Метод Такеовнершипекс класса Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 36512d48fe724da42c39c0d3d0686a706f54472d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895397"
---
# <a name="takeownershipex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="44a7a-104">Метод Такеовнершипекс \_ класса Win32 кодекфиле</span><span class="sxs-lookup"><span data-stu-id="44a7a-104">TakeOwnerShipEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="44a7a-105">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) такеовнершипекс получает владение логическим файлом кодека, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="44a7a-105">The **TakeOwnerShipEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical codec file specified in the object path.</span></span> <span data-ttu-id="44a7a-106">Этот метод является расширенной версией метода [**такеовнершип**](takeownership-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="44a7a-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="44a7a-107">Если логический файл фактически является каталогом, этот метод работает рекурсивно, принимая во внимание владение всеми файлами и подкаталогами, которые содержит каталог.</span><span class="sxs-lookup"><span data-stu-id="44a7a-107">If the logical file is actually a directory, then this method acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="44a7a-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="44a7a-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="44a7a-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="44a7a-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="44a7a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44a7a-110">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="44a7a-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="44a7a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44a7a-112">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="44a7a-112">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44a7a-113">Имя файла или каталога, в котором произошел сбой метода **такеовнершипекс** .</span><span class="sxs-lookup"><span data-stu-id="44a7a-113">Name of the file or directory where the **TakeOwnerShipEx** method failed.</span></span> <span data-ttu-id="44a7a-114">Если метод завершится с ошибкой, этот параметр будет иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="44a7a-114">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="44a7a-115">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="44a7a-115">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="44a7a-116">Имя дочернего файла или каталога, который будет использоваться в качестве отправной точки для **такеовнершипекс**. Параметр *StartFileName* обычно представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="44a7a-116">Names the child file or directory to use as a starting point for **TakeOwnerShipEx**.The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="44a7a-117">Если этот параметр имеет **значение NULL**, операция выполняется над файлом или каталогом, указанным в вызове метода **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="44a7a-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="44a7a-118">*Рекурсивно* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="44a7a-118">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="44a7a-119">Если **значение — true**, изменение владельца будет применяться рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="44a7a-119">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="44a7a-120">Примечание. для экземпляров файлов входной параметр *recursive* не учитывается.</span><span class="sxs-lookup"><span data-stu-id="44a7a-120">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44a7a-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44a7a-121">Return value</span></span>

<span data-ttu-id="44a7a-122">Возвращает целочисленное значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="44a7a-122">Returns an integer value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="44a7a-123">**0**</span><span class="sxs-lookup"><span data-stu-id="44a7a-123">**0**</span></span>
</dt> <dd>

<span data-ttu-id="44a7a-124">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="44a7a-124">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="44a7a-125">**2**</span><span class="sxs-lookup"><span data-stu-id="44a7a-125">**2**</span></span>
</dt> <dd>

<span data-ttu-id="44a7a-126">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="44a7a-126">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="44a7a-127">**8**</span><span class="sxs-lookup"><span data-stu-id="44a7a-127">**8**</span></span>
</dt> <dd>

<span data-ttu-id="44a7a-128">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="44a7a-128">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="44a7a-129">**9**</span><span class="sxs-lookup"><span data-stu-id="44a7a-129">**9**</span></span>
</dt> <dd>

<span data-ttu-id="44a7a-130">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="44a7a-130">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="44a7a-131">**10**</span><span class="sxs-lookup"><span data-stu-id="44a7a-131">**10**</span></span>
</dt> <dd>

<span data-ttu-id="44a7a-132">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="44a7a-132">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="44a7a-133">**11**</span><span class="sxs-lookup"><span data-stu-id="44a7a-133">**11**</span></span>
</dt> <dd>

<span data-ttu-id="44a7a-134">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="44a7a-134">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="44a7a-135">**12**</span><span class="sxs-lookup"><span data-stu-id="44a7a-135">**12**</span></span>
</dt> <dd>

<span data-ttu-id="44a7a-136">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="44a7a-136">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="44a7a-137">**13**</span><span class="sxs-lookup"><span data-stu-id="44a7a-137">**13**</span></span>
</dt> <dd>

<span data-ttu-id="44a7a-138">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="44a7a-138">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="44a7a-139">**14**</span><span class="sxs-lookup"><span data-stu-id="44a7a-139">**14**</span></span>
</dt> <dd>

<span data-ttu-id="44a7a-140">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="44a7a-140">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="44a7a-141">**15**</span><span class="sxs-lookup"><span data-stu-id="44a7a-141">**15**</span></span>
</dt> <dd>

<span data-ttu-id="44a7a-142">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="44a7a-142">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="44a7a-143">**16**</span><span class="sxs-lookup"><span data-stu-id="44a7a-143">**16**</span></span>
</dt> <dd>

<span data-ttu-id="44a7a-144">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="44a7a-144">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="44a7a-145">**17**</span><span class="sxs-lookup"><span data-stu-id="44a7a-145">**17**</span></span>
</dt> <dd>

<span data-ttu-id="44a7a-146">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="44a7a-146">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="44a7a-147">**открыт**</span><span class="sxs-lookup"><span data-stu-id="44a7a-147">**21**</span></span>
</dt> <dd>

<span data-ttu-id="44a7a-148">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="44a7a-148">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44a7a-149">Требования</span><span class="sxs-lookup"><span data-stu-id="44a7a-149">Requirements</span></span>



| <span data-ttu-id="44a7a-150">Требование</span><span class="sxs-lookup"><span data-stu-id="44a7a-150">Requirement</span></span> | <span data-ttu-id="44a7a-151">Значение</span><span class="sxs-lookup"><span data-stu-id="44a7a-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44a7a-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44a7a-152">Minimum supported client</span></span><br/> | <span data-ttu-id="44a7a-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44a7a-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="44a7a-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44a7a-154">Minimum supported server</span></span><br/> | <span data-ttu-id="44a7a-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44a7a-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="44a7a-156">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="44a7a-156">Namespace</span></span><br/>                | <span data-ttu-id="44a7a-157">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="44a7a-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="44a7a-158">MOF</span><span class="sxs-lookup"><span data-stu-id="44a7a-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44a7a-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44a7a-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="44a7a-160">DLL</span><span class="sxs-lookup"><span data-stu-id="44a7a-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44a7a-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44a7a-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44a7a-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44a7a-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="44a7a-163">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="44a7a-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="44a7a-164">**\_Кодекфиле Win32**</span><span class="sxs-lookup"><span data-stu-id="44a7a-164">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

