---
description: Такеовнершип&\# 8194; Метод класса WMI получает владение логическим файлом, указанным в пути объекта.
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
ms.openlocfilehash: 5da7a237ae1943e65bc1cc757d5c4a16c6df8900
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990392"
---
# <a name="takeownership-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="1adee-103">Метод Такеовнершип \_ класса Win32 шорткутфиле</span><span class="sxs-lookup"><span data-stu-id="1adee-103">TakeOwnerShip method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="1adee-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) такеовнершип получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="1adee-104">The **TakeOwnerShip** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="1adee-105">Если логический файл фактически является каталогом, **такеовнершип** работает рекурсивно, перепринимая владение всеми файлами и подкаталогами, которые содержит каталог.</span><span class="sxs-lookup"><span data-stu-id="1adee-105">If the logical file is actually a directory, then **TakeOwnerShip** acts recursively, taking ownership of all the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="1adee-106">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="1adee-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1adee-107">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1adee-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1adee-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1adee-108">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="1adee-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1adee-109">Parameters</span></span>

<span data-ttu-id="1adee-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1adee-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1adee-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1adee-111">Return value</span></span>

<span data-ttu-id="1adee-112">Возвращает одно из следующих целочисленных значений.</span><span class="sxs-lookup"><span data-stu-id="1adee-112">Returns one of the following integer values.</span></span>

<dl> <dt>

<span data-ttu-id="1adee-113">**0**</span><span class="sxs-lookup"><span data-stu-id="1adee-113">**0**</span></span>
</dt> <dd>

<span data-ttu-id="1adee-114">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="1adee-114">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="1adee-115">**2**</span><span class="sxs-lookup"><span data-stu-id="1adee-115">**2**</span></span>
</dt> <dd>

<span data-ttu-id="1adee-116">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="1adee-116">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="1adee-117">**8**</span><span class="sxs-lookup"><span data-stu-id="1adee-117">**8**</span></span>
</dt> <dd>

<span data-ttu-id="1adee-118">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="1adee-118">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="1adee-119">**9**</span><span class="sxs-lookup"><span data-stu-id="1adee-119">**9**</span></span>
</dt> <dd>

<span data-ttu-id="1adee-120">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="1adee-120">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1adee-121">**10**</span><span class="sxs-lookup"><span data-stu-id="1adee-121">**10**</span></span>
</dt> <dd>

<span data-ttu-id="1adee-122">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="1adee-122">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1adee-123">**11**</span><span class="sxs-lookup"><span data-stu-id="1adee-123">**11**</span></span>
</dt> <dd>

<span data-ttu-id="1adee-124">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="1adee-124">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="1adee-125">**12**</span><span class="sxs-lookup"><span data-stu-id="1adee-125">**12**</span></span>
</dt> <dd>

<span data-ttu-id="1adee-126">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="1adee-126">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="1adee-127">**13**</span><span class="sxs-lookup"><span data-stu-id="1adee-127">**13**</span></span>
</dt> <dd>

<span data-ttu-id="1adee-128">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="1adee-128">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="1adee-129">**14**</span><span class="sxs-lookup"><span data-stu-id="1adee-129">**14**</span></span>
</dt> <dd>

<span data-ttu-id="1adee-130">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="1adee-130">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="1adee-131">**15**</span><span class="sxs-lookup"><span data-stu-id="1adee-131">**15**</span></span>
</dt> <dd>

<span data-ttu-id="1adee-132">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="1adee-132">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="1adee-133">**16**</span><span class="sxs-lookup"><span data-stu-id="1adee-133">**16**</span></span>
</dt> <dd>

<span data-ttu-id="1adee-134">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="1adee-134">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1adee-135">**17**</span><span class="sxs-lookup"><span data-stu-id="1adee-135">**17**</span></span>
</dt> <dd>

<span data-ttu-id="1adee-136">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="1adee-136">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="1adee-137">**открыт**</span><span class="sxs-lookup"><span data-stu-id="1adee-137">**21**</span></span>
</dt> <dd>

<span data-ttu-id="1adee-138">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="1adee-138">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1adee-139">Требования</span><span class="sxs-lookup"><span data-stu-id="1adee-139">Requirements</span></span>



| <span data-ttu-id="1adee-140">Требование</span><span class="sxs-lookup"><span data-stu-id="1adee-140">Requirement</span></span> | <span data-ttu-id="1adee-141">Значение</span><span class="sxs-lookup"><span data-stu-id="1adee-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1adee-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1adee-142">Minimum supported client</span></span><br/> | <span data-ttu-id="1adee-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1adee-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1adee-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1adee-144">Minimum supported server</span></span><br/> | <span data-ttu-id="1adee-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1adee-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1adee-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1adee-146">Namespace</span></span><br/>                | <span data-ttu-id="1adee-147">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1adee-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1adee-148">MOF</span><span class="sxs-lookup"><span data-stu-id="1adee-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1adee-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1adee-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1adee-150">DLL</span><span class="sxs-lookup"><span data-stu-id="1adee-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1adee-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1adee-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1adee-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1adee-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="1adee-153">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1adee-153">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1adee-154">**\_Шорткутфиле Win32**</span><span class="sxs-lookup"><span data-stu-id="1adee-154">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

