---
description: Метод Такеовнершип класса Win32_PageFile — Такеовнершип&\# 8194; Метод класса WMI получает владение логическим файлом, указанным в пути объекта.
ms.assetid: c4f42d54-562c-4163-a5ec-e94f76932631
ms.tgt_platform: multiple
title: Метод Такеовнершип класса Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3aa0b2ec9f3805f1877f86bdf86d72b921d53ac9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086022"
---
# <a name="takeownership-method-of-the-win32_pagefile-class"></a><span data-ttu-id="2f5a8-103">Метод Такеовнершип \_ класса файла подкачки Win32</span><span class="sxs-lookup"><span data-stu-id="2f5a8-103">TakeOwnerShip method of the Win32\_PageFile class</span></span>

<span data-ttu-id="2f5a8-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) такеовнершип получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="2f5a8-105">Если логический файл фактически является каталогом, **такеовнершип** работает рекурсивно, перепринимая владение всеми файлами и подкаталогами, которые содержит каталог.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="2f5a8-106">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="2f5a8-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2f5a8-107">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2f5a8-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f5a8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f5a8-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="2f5a8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f5a8-109">Parameters</span></span>

<span data-ttu-id="2f5a8-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f5a8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f5a8-111">Return value</span></span>

<span data-ttu-id="2f5a8-112">Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-112">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="2f5a8-113">**0**</span><span class="sxs-lookup"><span data-stu-id="2f5a8-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="2f5a8-114">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="2f5a8-115">**2**</span><span class="sxs-lookup"><span data-stu-id="2f5a8-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="2f5a8-116">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="2f5a8-117">**8**</span><span class="sxs-lookup"><span data-stu-id="2f5a8-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="2f5a8-118">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="2f5a8-119">**9**</span><span class="sxs-lookup"><span data-stu-id="2f5a8-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="2f5a8-120">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2f5a8-121">**10**</span><span class="sxs-lookup"><span data-stu-id="2f5a8-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="2f5a8-122">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2f5a8-123">**11**</span><span class="sxs-lookup"><span data-stu-id="2f5a8-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="2f5a8-124">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="2f5a8-125">**12**</span><span class="sxs-lookup"><span data-stu-id="2f5a8-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="2f5a8-126">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="2f5a8-127">**13**</span><span class="sxs-lookup"><span data-stu-id="2f5a8-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="2f5a8-128">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="2f5a8-129">**14**</span><span class="sxs-lookup"><span data-stu-id="2f5a8-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="2f5a8-130">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="2f5a8-131">**15**</span><span class="sxs-lookup"><span data-stu-id="2f5a8-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="2f5a8-132">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="2f5a8-133">**16**</span><span class="sxs-lookup"><span data-stu-id="2f5a8-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="2f5a8-134">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="2f5a8-135">**17**</span><span class="sxs-lookup"><span data-stu-id="2f5a8-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="2f5a8-136">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="2f5a8-137">**открыт**</span><span class="sxs-lookup"><span data-stu-id="2f5a8-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="2f5a8-138">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="2f5a8-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f5a8-139">Требования</span><span class="sxs-lookup"><span data-stu-id="2f5a8-139">Requirements</span></span>



| <span data-ttu-id="2f5a8-140">Требование</span><span class="sxs-lookup"><span data-stu-id="2f5a8-140">Requirement</span></span> | <span data-ttu-id="2f5a8-141">Значение</span><span class="sxs-lookup"><span data-stu-id="2f5a8-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f5a8-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f5a8-142">Minimum supported client</span></span><br/> | <span data-ttu-id="2f5a8-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f5a8-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2f5a8-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f5a8-144">Minimum supported server</span></span><br/> | <span data-ttu-id="2f5a8-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f5a8-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2f5a8-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2f5a8-146">Namespace</span></span><br/>                | <span data-ttu-id="2f5a8-147">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2f5a8-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2f5a8-148">MOF</span><span class="sxs-lookup"><span data-stu-id="2f5a8-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f5a8-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f5a8-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f5a8-150">DLL</span><span class="sxs-lookup"><span data-stu-id="2f5a8-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f5a8-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f5a8-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f5a8-152">См. также</span><span class="sxs-lookup"><span data-stu-id="2f5a8-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="2f5a8-153">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2f5a8-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2f5a8-154">**\_Файл подкачки Win32**</span><span class="sxs-lookup"><span data-stu-id="2f5a8-154">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

