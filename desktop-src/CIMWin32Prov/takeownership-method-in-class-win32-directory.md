---
description: Метод Такеовнершип класса Win32_Directory. метод класса WMI Такеовнершип получает владение логическим файлом, указанным в пути объекта.
ms.assetid: 1112823b-0bb6-4dc0-a5c4-8d3839a47a3a
ms.tgt_platform: multiple
title: Метод Такеовнершип класса Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 178f1bf523d939883a7fc18b5bdbd7142cc4f824
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086032"
---
# <a name="takeownership-method-of-the-win32_directory-class"></a><span data-ttu-id="737c9-103">Метод Такеовнершип \_ класса каталога Win32</span><span class="sxs-lookup"><span data-stu-id="737c9-103">TakeOwnerShip method of the Win32\_Directory class</span></span>

<span data-ttu-id="737c9-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) такеовнершип получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="737c9-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="737c9-105">Если логический файл фактически является каталогом, **такеовнершип** работает рекурсивно, перепринимая владение всеми файлами и подкаталогами, которые содержит каталог.</span><span class="sxs-lookup"><span data-stu-id="737c9-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="737c9-106">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="737c9-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="737c9-107">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="737c9-107">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="737c9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="737c9-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="737c9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="737c9-109">Parameters</span></span>

<span data-ttu-id="737c9-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="737c9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="737c9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="737c9-111">Return value</span></span>

<span data-ttu-id="737c9-112">Возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="737c9-112">Returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="737c9-113">**0**</span><span class="sxs-lookup"><span data-stu-id="737c9-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="737c9-114">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="737c9-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="737c9-115">**2**</span><span class="sxs-lookup"><span data-stu-id="737c9-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="737c9-116">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="737c9-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="737c9-117">**8**</span><span class="sxs-lookup"><span data-stu-id="737c9-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="737c9-118">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="737c9-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="737c9-119">**9**</span><span class="sxs-lookup"><span data-stu-id="737c9-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="737c9-120">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="737c9-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="737c9-121">**10**</span><span class="sxs-lookup"><span data-stu-id="737c9-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="737c9-122">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="737c9-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="737c9-123">**11**</span><span class="sxs-lookup"><span data-stu-id="737c9-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="737c9-124">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="737c9-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="737c9-125">**12**</span><span class="sxs-lookup"><span data-stu-id="737c9-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="737c9-126">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="737c9-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="737c9-127">**13**</span><span class="sxs-lookup"><span data-stu-id="737c9-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="737c9-128">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="737c9-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="737c9-129">**14**</span><span class="sxs-lookup"><span data-stu-id="737c9-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="737c9-130">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="737c9-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="737c9-131">**15**</span><span class="sxs-lookup"><span data-stu-id="737c9-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="737c9-132">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="737c9-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="737c9-133">**16**</span><span class="sxs-lookup"><span data-stu-id="737c9-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="737c9-134">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="737c9-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="737c9-135">**17**</span><span class="sxs-lookup"><span data-stu-id="737c9-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="737c9-136">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="737c9-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="737c9-137">**открыт**</span><span class="sxs-lookup"><span data-stu-id="737c9-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="737c9-138">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="737c9-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="737c9-139">Примеры</span><span class="sxs-lookup"><span data-stu-id="737c9-139">Examples</span></span>

<span data-ttu-id="737c9-140">Следующий код скрипта Visual Basic вызывает метод [**такеовнершип**](takeownership-method-in-class-cim-directory.md) , чтобы стать владельцем папки C: \\ TEMP.</span><span class="sxs-lookup"><span data-stu-id="737c9-140">The following Visual Basic Script code calls the [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 

Set objWMIService = _
    GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 

' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\\temp'", "TakeOwnerShip")

wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="737c9-141">Требования</span><span class="sxs-lookup"><span data-stu-id="737c9-141">Requirements</span></span>



| <span data-ttu-id="737c9-142">Требование</span><span class="sxs-lookup"><span data-stu-id="737c9-142">Requirement</span></span> | <span data-ttu-id="737c9-143">Значение</span><span class="sxs-lookup"><span data-stu-id="737c9-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="737c9-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="737c9-144">Minimum supported client</span></span><br/> | <span data-ttu-id="737c9-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="737c9-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="737c9-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="737c9-146">Minimum supported server</span></span><br/> | <span data-ttu-id="737c9-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="737c9-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="737c9-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="737c9-148">Namespace</span></span><br/>                | <span data-ttu-id="737c9-149">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="737c9-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="737c9-150">MOF</span><span class="sxs-lookup"><span data-stu-id="737c9-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="737c9-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="737c9-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="737c9-152">DLL</span><span class="sxs-lookup"><span data-stu-id="737c9-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="737c9-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="737c9-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="737c9-154">См. также</span><span class="sxs-lookup"><span data-stu-id="737c9-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="737c9-155">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="737c9-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="737c9-156">**\_Каталог Win32**</span><span class="sxs-lookup"><span data-stu-id="737c9-156">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

