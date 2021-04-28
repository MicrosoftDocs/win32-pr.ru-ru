---
description: Метод Такеовнершип класса Win32_ShortcutFile — Такеовнершип&\# 8194; Метод класса WMI получает владение логическим файлом, указанным в пути объекта.
ms.assetid: 1a8ff156-50b2-4550-abcc-7a6ae0e4630f
ms.tgt_platform: multiple
title: Метод Такеовнершип класса Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 36364a55276842518480c3d3d37c57c3ae0a06ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086002"
---
# <a name="takeownership-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="5dadc-103">Метод Такеовнершип \_ класса Win32 шорткутфиле</span><span class="sxs-lookup"><span data-stu-id="5dadc-103">TakeOwnerShip method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="5dadc-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) такеовнершип получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="5dadc-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="5dadc-105">Если логический файл фактически является каталогом, **такеовнершип** работает рекурсивно, перепринимая владение всеми файлами и подкаталогами, которые содержит каталог.</span><span class="sxs-lookup"><span data-stu-id="5dadc-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="5dadc-106">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="5dadc-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5dadc-107">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5dadc-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5dadc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5dadc-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="5dadc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5dadc-109">Parameters</span></span>

<span data-ttu-id="5dadc-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="5dadc-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5dadc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5dadc-111">Return value</span></span>

<span data-ttu-id="5dadc-112">Возвращает одно из следующих целочисленных значений.</span><span class="sxs-lookup"><span data-stu-id="5dadc-112">Returns one of the following integer values.</span></span>

<dl> <dt>

<span data-ttu-id="5dadc-113">**0**</span><span class="sxs-lookup"><span data-stu-id="5dadc-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="5dadc-114">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="5dadc-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="5dadc-115">**2**</span><span class="sxs-lookup"><span data-stu-id="5dadc-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="5dadc-116">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="5dadc-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="5dadc-117">**8**</span><span class="sxs-lookup"><span data-stu-id="5dadc-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="5dadc-118">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="5dadc-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="5dadc-119">**9**</span><span class="sxs-lookup"><span data-stu-id="5dadc-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="5dadc-120">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="5dadc-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5dadc-121">**10**</span><span class="sxs-lookup"><span data-stu-id="5dadc-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="5dadc-122">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="5dadc-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5dadc-123">**11**</span><span class="sxs-lookup"><span data-stu-id="5dadc-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="5dadc-124">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="5dadc-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="5dadc-125">**12**</span><span class="sxs-lookup"><span data-stu-id="5dadc-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="5dadc-126">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="5dadc-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="5dadc-127">**13**</span><span class="sxs-lookup"><span data-stu-id="5dadc-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="5dadc-128">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="5dadc-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="5dadc-129">**14**</span><span class="sxs-lookup"><span data-stu-id="5dadc-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="5dadc-130">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="5dadc-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="5dadc-131">**15**</span><span class="sxs-lookup"><span data-stu-id="5dadc-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="5dadc-132">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="5dadc-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="5dadc-133">**16**</span><span class="sxs-lookup"><span data-stu-id="5dadc-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="5dadc-134">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="5dadc-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5dadc-135">**17**</span><span class="sxs-lookup"><span data-stu-id="5dadc-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="5dadc-136">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="5dadc-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="5dadc-137">**открыт**</span><span class="sxs-lookup"><span data-stu-id="5dadc-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="5dadc-138">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="5dadc-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5dadc-139">Требования</span><span class="sxs-lookup"><span data-stu-id="5dadc-139">Requirements</span></span>



| <span data-ttu-id="5dadc-140">Требование</span><span class="sxs-lookup"><span data-stu-id="5dadc-140">Requirement</span></span> | <span data-ttu-id="5dadc-141">Значение</span><span class="sxs-lookup"><span data-stu-id="5dadc-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5dadc-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5dadc-142">Minimum supported client</span></span><br/> | <span data-ttu-id="5dadc-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5dadc-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5dadc-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5dadc-144">Minimum supported server</span></span><br/> | <span data-ttu-id="5dadc-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5dadc-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5dadc-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5dadc-146">Namespace</span></span><br/>                | <span data-ttu-id="5dadc-147">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5dadc-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5dadc-148">MOF</span><span class="sxs-lookup"><span data-stu-id="5dadc-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5dadc-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5dadc-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5dadc-150">DLL</span><span class="sxs-lookup"><span data-stu-id="5dadc-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5dadc-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dadc-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dadc-152">См. также</span><span class="sxs-lookup"><span data-stu-id="5dadc-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="5dadc-153">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5dadc-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5dadc-154">**\_Шорткутфиле Win32**</span><span class="sxs-lookup"><span data-stu-id="5dadc-154">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

