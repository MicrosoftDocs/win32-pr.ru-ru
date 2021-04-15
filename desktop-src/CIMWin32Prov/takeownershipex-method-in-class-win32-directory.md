---
description: Получает владение файлом записи логического каталога, указанным в пути объекта. Этот метод является расширенной версией метода Такеовнершип.
ms.assetid: 73726207-e885-4957-bff8-6903c4b99278
ms.tgt_platform: multiple
title: Метод Такеовнершипекс класса Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2e391e942e581d0f80d46b0f59b9b273d7bff499
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655674"
---
# <a name="takeownershipex-method-of-the-win32_directory-class"></a><span data-ttu-id="7578e-104">Метод Такеовнершипекс \_ класса каталога Win32</span><span class="sxs-lookup"><span data-stu-id="7578e-104">TakeOwnerShipEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="7578e-105">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) такеовнершипекс получает владение файлом записи логического каталога, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="7578e-105">The **TakeOwnerShipEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="7578e-106">Этот метод является расширенной версией метода [**такеовнершип**](takeownership-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="7578e-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="7578e-107">Если логический файл фактически является каталогом, этот метод работает рекурсивно, принимая во внимание владение всеми файлами и подкаталогами, которые содержит каталог.</span><span class="sxs-lookup"><span data-stu-id="7578e-107">If the logical file is actually a directory, then this method acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="7578e-108">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="7578e-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7578e-109">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7578e-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7578e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7578e-110">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="7578e-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="7578e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7578e-112">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7578e-112">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7578e-113">Имя файла или каталога, в котором произошел сбой метода **такеовнершипекс** .</span><span class="sxs-lookup"><span data-stu-id="7578e-113">Name of the file or directory where the **TakeOwnerShipEx** method failed.</span></span> <span data-ttu-id="7578e-114">Если метод выполнен, этот параметр имеет **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="7578e-114">This parameter is **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="7578e-115">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="7578e-115">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7578e-116">Имя дочернего файла или каталога, который будет использоваться в качестве отправной точки для **такеовнершипекс**.</span><span class="sxs-lookup"><span data-stu-id="7578e-116">Names the child file or directory to use as a starting point for **TakeOwnerShipEx**.</span></span> <span data-ttu-id="7578e-117">Параметр *StartFileName* обычно представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="7578e-117">The *StartFileName* parameter is typically the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="7578e-118">Если этот параметр имеет **значение NULL**, операция выполняется над файлом или каталогом, указанным в вызове метода [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="7578e-118">If this parameter is **NULL**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod) call.</span></span>

<span data-ttu-id="7578e-119">Если используется параметр *StartFileName* , то для *рекурсии* необходимо также задать значение true.</span><span class="sxs-lookup"><span data-stu-id="7578e-119">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="7578e-120">*Рекурсивно* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="7578e-120">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7578e-121">Если **значение — true**, изменение владельца применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="7578e-121">If **True**, the change of ownership is applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="7578e-122">Для экземпляров файлов *рекурсивный* входной параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="7578e-122">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7578e-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7578e-123">Return value</span></span>

<span data-ttu-id="7578e-124">Возвращает целочисленное значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="7578e-124">Returns an integer value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="7578e-125">**0**</span><span class="sxs-lookup"><span data-stu-id="7578e-125">**0**</span></span>
</dt> <dd>

<span data-ttu-id="7578e-126">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="7578e-126">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="7578e-127">**2**</span><span class="sxs-lookup"><span data-stu-id="7578e-127">**2**</span></span>
</dt> <dd>

<span data-ttu-id="7578e-128">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="7578e-128">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="7578e-129">**8**</span><span class="sxs-lookup"><span data-stu-id="7578e-129">**8**</span></span>
</dt> <dd>

<span data-ttu-id="7578e-130">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="7578e-130">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="7578e-131">**9**</span><span class="sxs-lookup"><span data-stu-id="7578e-131">**9**</span></span>
</dt> <dd>

<span data-ttu-id="7578e-132">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="7578e-132">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="7578e-133">**10**</span><span class="sxs-lookup"><span data-stu-id="7578e-133">**10**</span></span>
</dt> <dd>

<span data-ttu-id="7578e-134">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="7578e-134">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="7578e-135">**11**</span><span class="sxs-lookup"><span data-stu-id="7578e-135">**11**</span></span>
</dt> <dd>

<span data-ttu-id="7578e-136">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="7578e-136">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="7578e-137">**12**</span><span class="sxs-lookup"><span data-stu-id="7578e-137">**12**</span></span>
</dt> <dd>

<span data-ttu-id="7578e-138">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="7578e-138">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="7578e-139">**13**</span><span class="sxs-lookup"><span data-stu-id="7578e-139">**13**</span></span>
</dt> <dd>

<span data-ttu-id="7578e-140">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="7578e-140">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="7578e-141">**14**</span><span class="sxs-lookup"><span data-stu-id="7578e-141">**14**</span></span>
</dt> <dd>

<span data-ttu-id="7578e-142">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="7578e-142">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="7578e-143">**15**</span><span class="sxs-lookup"><span data-stu-id="7578e-143">**15**</span></span>
</dt> <dd>

<span data-ttu-id="7578e-144">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="7578e-144">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="7578e-145">**16**</span><span class="sxs-lookup"><span data-stu-id="7578e-145">**16**</span></span>
</dt> <dd>

<span data-ttu-id="7578e-146">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="7578e-146">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="7578e-147">**17**</span><span class="sxs-lookup"><span data-stu-id="7578e-147">**17**</span></span>
</dt> <dd>

<span data-ttu-id="7578e-148">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="7578e-148">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="7578e-149">**открыт**</span><span class="sxs-lookup"><span data-stu-id="7578e-149">**21**</span></span>
</dt> <dd>

<span data-ttu-id="7578e-150">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="7578e-150">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="7578e-151">Примеры</span><span class="sxs-lookup"><span data-stu-id="7578e-151">Examples</span></span>

<span data-ttu-id="7578e-152">Следующий код скрипта Visual Basic вызывает метод [**такеовнершипекс**](takeownershipex-method-in-class-cim-directory.md) , чтобы стать владельцем папки C: \\ TEMP.</span><span class="sxs-lookup"><span data-stu-id="7578e-152">The following Visual Basic Script code calls the [**TakeOwnerShipEx**](takeownershipex-method-in-class-cim-directory.md) method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx").inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod("Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="7578e-153">Требования</span><span class="sxs-lookup"><span data-stu-id="7578e-153">Requirements</span></span>



| <span data-ttu-id="7578e-154">Требование</span><span class="sxs-lookup"><span data-stu-id="7578e-154">Requirement</span></span> | <span data-ttu-id="7578e-155">Значение</span><span class="sxs-lookup"><span data-stu-id="7578e-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7578e-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7578e-156">Minimum supported client</span></span><br/> | <span data-ttu-id="7578e-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7578e-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7578e-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7578e-158">Minimum supported server</span></span><br/> | <span data-ttu-id="7578e-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7578e-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7578e-160">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7578e-160">Namespace</span></span><br/>                | <span data-ttu-id="7578e-161">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7578e-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7578e-162">MOF</span><span class="sxs-lookup"><span data-stu-id="7578e-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7578e-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7578e-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7578e-164">DLL</span><span class="sxs-lookup"><span data-stu-id="7578e-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7578e-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7578e-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7578e-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7578e-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="7578e-167">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7578e-167">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7578e-168">**\_Каталог Win32**</span><span class="sxs-lookup"><span data-stu-id="7578e-168">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

