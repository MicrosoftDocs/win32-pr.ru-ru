---
description: Метод Такеовнершип получает владение логическим файлом, указанным в пути объекта. Если логический файл является каталогом, этот метод работает рекурсивно, перепринимая владение всеми файлами и подкаталогами, которые содержит каталог.
ms.assetid: 5db62da0-ac93-4a8c-af17-306e02bfa756
ms.tgt_platform: multiple
title: Метод Такеовнершип класса CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7cdd9515a5e947a3e707464dcbd524c875f7785f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538414"
---
# <a name="takeownership-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="4454a-104">Метод Такеовнершип \_ класса CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="4454a-104">TakeOwnerShip method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="4454a-105">Метод **такеовнершип** получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="4454a-105">The **TakeOwnerShip** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="4454a-106">Если логический файл является каталогом, этот метод работает рекурсивно, перепринимая владение всеми файлами и подкаталогами, которые содержит каталог.</span><span class="sxs-lookup"><span data-stu-id="4454a-106">If the logical file is a directory, then this method acts recursively, taking ownership of all files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4454a-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="4454a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4454a-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4454a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4454a-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="4454a-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4454a-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4454a-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4454a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4454a-111">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="4454a-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="4454a-112">Parameters</span></span>

<span data-ttu-id="4454a-113">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4454a-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4454a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4454a-114">Return value</span></span>

<span data-ttu-id="4454a-115">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="4454a-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="4454a-116">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="4454a-116">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="4454a-117">0</span><span class="sxs-lookup"><span data-stu-id="4454a-117">0</span></span>

<span data-ttu-id="4454a-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="4454a-118">Success.</span></span>

</dd> <dt>

<span data-ttu-id="4454a-119">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="4454a-119">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="4454a-120">2</span><span class="sxs-lookup"><span data-stu-id="4454a-120">2</span></span>

<span data-ttu-id="4454a-121">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="4454a-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="4454a-122">**Неопределенный сбой**</span><span class="sxs-lookup"><span data-stu-id="4454a-122">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="4454a-123">8</span><span class="sxs-lookup"><span data-stu-id="4454a-123">8</span></span>

<span data-ttu-id="4454a-124">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="4454a-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="4454a-125">**Недопустимый объект**</span><span class="sxs-lookup"><span data-stu-id="4454a-125">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="4454a-126">9</span><span class="sxs-lookup"><span data-stu-id="4454a-126">9</span></span>

<span data-ttu-id="4454a-127">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="4454a-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="4454a-128">**Объект уже существует**</span><span class="sxs-lookup"><span data-stu-id="4454a-128">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="4454a-129">10</span><span class="sxs-lookup"><span data-stu-id="4454a-129">10</span></span>

<span data-ttu-id="4454a-130">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="4454a-130">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="4454a-131">**Файловая система не NTFS**</span><span class="sxs-lookup"><span data-stu-id="4454a-131">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="4454a-132">11</span><span class="sxs-lookup"><span data-stu-id="4454a-132">11</span></span>

<span data-ttu-id="4454a-133">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="4454a-133">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="4454a-134">**Платформа не NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="4454a-134">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="4454a-135">12</span><span class="sxs-lookup"><span data-stu-id="4454a-135">12</span></span>

<span data-ttu-id="4454a-136">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="4454a-136">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="4454a-137">**Диск не совпадает**</span><span class="sxs-lookup"><span data-stu-id="4454a-137">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="4454a-138">13</span><span class="sxs-lookup"><span data-stu-id="4454a-138">13</span></span>

<span data-ttu-id="4454a-139">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="4454a-139">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="4454a-140">**Каталог не пуст**</span><span class="sxs-lookup"><span data-stu-id="4454a-140">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="4454a-141">14</span><span class="sxs-lookup"><span data-stu-id="4454a-141">14</span></span>

<span data-ttu-id="4454a-142">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="4454a-142">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="4454a-143">**Нарушение общего доступа**</span><span class="sxs-lookup"><span data-stu-id="4454a-143">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="4454a-144">15</span><span class="sxs-lookup"><span data-stu-id="4454a-144">15</span></span>

<span data-ttu-id="4454a-145">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="4454a-145">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="4454a-146">**Недопустимый файл запуска**</span><span class="sxs-lookup"><span data-stu-id="4454a-146">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="4454a-147">16</span><span class="sxs-lookup"><span data-stu-id="4454a-147">16</span></span>

<span data-ttu-id="4454a-148">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="4454a-148">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="4454a-149">**Привилегия не удерживается**</span><span class="sxs-lookup"><span data-stu-id="4454a-149">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="4454a-150">17</span><span class="sxs-lookup"><span data-stu-id="4454a-150">17</span></span>

<span data-ttu-id="4454a-151">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="4454a-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="4454a-152">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="4454a-152">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4454a-153">21</span><span class="sxs-lookup"><span data-stu-id="4454a-153">21</span></span>

<span data-ttu-id="4454a-154">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="4454a-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4454a-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4454a-155">Remarks</span></span>

<span data-ttu-id="4454a-156">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="4454a-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4454a-157">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="4454a-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="4454a-158">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="4454a-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4454a-159">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="4454a-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4454a-160">Требования</span><span class="sxs-lookup"><span data-stu-id="4454a-160">Requirements</span></span>



| <span data-ttu-id="4454a-161">Требование</span><span class="sxs-lookup"><span data-stu-id="4454a-161">Requirement</span></span> | <span data-ttu-id="4454a-162">Значение</span><span class="sxs-lookup"><span data-stu-id="4454a-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4454a-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4454a-163">Minimum supported client</span></span><br/> | <span data-ttu-id="4454a-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4454a-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4454a-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4454a-165">Minimum supported server</span></span><br/> | <span data-ttu-id="4454a-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4454a-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4454a-167">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4454a-167">Namespace</span></span><br/>                | <span data-ttu-id="4454a-168">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4454a-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4454a-169">MOF</span><span class="sxs-lookup"><span data-stu-id="4454a-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4454a-170"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4454a-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4454a-171">DLL</span><span class="sxs-lookup"><span data-stu-id="4454a-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4454a-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4454a-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4454a-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4454a-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4454a-174">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="4454a-174">CIM\_LogicalFile</span></span>](takeownership-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="4454a-175">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="4454a-175">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

