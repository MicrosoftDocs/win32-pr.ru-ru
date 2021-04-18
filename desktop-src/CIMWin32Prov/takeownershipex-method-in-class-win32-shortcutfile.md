---
description: Получает владение логическим файлом ярлыка, указанным в пути объекта. Этот метод является расширенной версией метода Такеовнершип.
ms.assetid: 1345562c-343e-4e3a-b6ed-3b64a7260c89
ms.tgt_platform: multiple
title: Метод Такеовнершипекс класса Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 69988c7995ee295297c92bbabf0ee83059304a94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655672"
---
# <a name="takeownershipex-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="46cc0-104">Метод Такеовнершипекс \_ класса Win32 шорткутфиле</span><span class="sxs-lookup"><span data-stu-id="46cc0-104">TakeOwnerShipEx method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="46cc0-105">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) такеовнершипекс получает владение логическим файлом ярлыка, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="46cc0-105">The **TakeOwnerShipEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical shortcut file specified in the object path.</span></span> <span data-ttu-id="46cc0-106">Этот метод является расширенной версией метода [**такеовнершип**](takeownership-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="46cc0-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="46cc0-107">Если логический файл фактически является каталогом, этот метод работает рекурсивно, принимая во внимание владение всеми файлами и подкаталогами, которые содержит каталог.</span><span class="sxs-lookup"><span data-stu-id="46cc0-107">If the logical file is actually a directory, then this method acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="46cc0-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="46cc0-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="46cc0-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="46cc0-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="46cc0-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46cc0-110">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="46cc0-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="46cc0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46cc0-112">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="46cc0-112">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46cc0-113">Имя файла или каталога, в котором произошел сбой метода **такеовнершипекс** .</span><span class="sxs-lookup"><span data-stu-id="46cc0-113">Name of the file or directory where the **TakeOwnerShipEx** method failed.</span></span> <span data-ttu-id="46cc0-114">Если метод завершится с ошибкой, этот параметр будет иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="46cc0-114">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="46cc0-115">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="46cc0-115">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="46cc0-116">Имя дочернего файла или каталога, который будет использоваться в качестве отправной точки для **такеовнершипекс**.</span><span class="sxs-lookup"><span data-stu-id="46cc0-116">Names the child file or directory to use as a starting point for **TakeOwnerShipEx**.</span></span> <span data-ttu-id="46cc0-117">Параметр *StartFileName* обычно представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="46cc0-117">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="46cc0-118">Если этот параметр имеет **значение NULL**, операция выполняется над файлом или каталогом, указанным в вызове метода ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="46cc0-118">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="46cc0-119">*Рекурсивно* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="46cc0-119">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="46cc0-120">Если **значение — true**, изменение владельца будет применяться рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="46cc0-120">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="46cc0-121">Для экземпляров файлов *рекурсивный* параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="46cc0-121">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46cc0-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46cc0-122">Return value</span></span>

<span data-ttu-id="46cc0-123">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="46cc0-123">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="46cc0-124">**0**</span><span class="sxs-lookup"><span data-stu-id="46cc0-124">**0**</span></span>
</dt> <dd>

<span data-ttu-id="46cc0-125">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="46cc0-125">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="46cc0-126">**2**</span><span class="sxs-lookup"><span data-stu-id="46cc0-126">**2**</span></span>
</dt> <dd>

<span data-ttu-id="46cc0-127">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="46cc0-127">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="46cc0-128">**8**</span><span class="sxs-lookup"><span data-stu-id="46cc0-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="46cc0-129">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="46cc0-129">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="46cc0-130">**9**</span><span class="sxs-lookup"><span data-stu-id="46cc0-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="46cc0-131">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="46cc0-131">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="46cc0-132">**10**</span><span class="sxs-lookup"><span data-stu-id="46cc0-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="46cc0-133">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="46cc0-133">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="46cc0-134">**11**</span><span class="sxs-lookup"><span data-stu-id="46cc0-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="46cc0-135">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="46cc0-135">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="46cc0-136">**12**</span><span class="sxs-lookup"><span data-stu-id="46cc0-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="46cc0-137">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="46cc0-137">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="46cc0-138">**13**</span><span class="sxs-lookup"><span data-stu-id="46cc0-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="46cc0-139">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="46cc0-139">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="46cc0-140">**14**</span><span class="sxs-lookup"><span data-stu-id="46cc0-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="46cc0-141">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="46cc0-141">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="46cc0-142">**15**</span><span class="sxs-lookup"><span data-stu-id="46cc0-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="46cc0-143">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="46cc0-143">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="46cc0-144">**16**</span><span class="sxs-lookup"><span data-stu-id="46cc0-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="46cc0-145">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="46cc0-145">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="46cc0-146">**17**</span><span class="sxs-lookup"><span data-stu-id="46cc0-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="46cc0-147">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="46cc0-147">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="46cc0-148">**открыт**</span><span class="sxs-lookup"><span data-stu-id="46cc0-148">**21**</span></span>
</dt> <dd>

<span data-ttu-id="46cc0-149">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="46cc0-149">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46cc0-150">Требования</span><span class="sxs-lookup"><span data-stu-id="46cc0-150">Requirements</span></span>



| <span data-ttu-id="46cc0-151">Требование</span><span class="sxs-lookup"><span data-stu-id="46cc0-151">Requirement</span></span> | <span data-ttu-id="46cc0-152">Значение</span><span class="sxs-lookup"><span data-stu-id="46cc0-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46cc0-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46cc0-153">Minimum supported client</span></span><br/> | <span data-ttu-id="46cc0-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46cc0-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="46cc0-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46cc0-155">Minimum supported server</span></span><br/> | <span data-ttu-id="46cc0-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46cc0-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="46cc0-157">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="46cc0-157">Namespace</span></span><br/>                | <span data-ttu-id="46cc0-158">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="46cc0-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="46cc0-159">MOF</span><span class="sxs-lookup"><span data-stu-id="46cc0-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46cc0-160"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46cc0-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="46cc0-161">DLL</span><span class="sxs-lookup"><span data-stu-id="46cc0-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46cc0-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46cc0-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46cc0-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46cc0-163">See also</span></span>

<dl> <dt>

<span data-ttu-id="46cc0-164">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="46cc0-164">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="46cc0-165">**\_Шорткутфиле Win32**</span><span class="sxs-lookup"><span data-stu-id="46cc0-165">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

