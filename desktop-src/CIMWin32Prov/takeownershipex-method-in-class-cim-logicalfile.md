---
description: Получает владение логическим файлом, указанным в пути объекта. Этот метод является расширенной версией метода Такеовнершип.
ms.assetid: c01ab071-86e4-484d-aaed-4783b6c3bebf
ms.tgt_platform: multiple
title: Метод Такеовнершипекс класса CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2e7f08413440ec32037554476ced386c56827239
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655678"
---
# <a name="takeownershipex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="fb555-104">Метод Такеовнершипекс \_ класса CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="fb555-104">TakeOwnerShipEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="fb555-105">Метод **такеовнершипекс** получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="fb555-105">The **TakeOwnerShipEx** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="fb555-106">Этот метод является расширенной версией метода [**такеовнершип**](takeownership-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="fb555-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-logicalfile.md) method.</span></span> <span data-ttu-id="fb555-107">Если логический файл является каталогом, этот метод работает рекурсивно, перепринимая владение всеми файлами и подкаталогами, которые содержит каталог.</span><span class="sxs-lookup"><span data-stu-id="fb555-107">If the logical file is a directory, then this method acts recursively, taking ownership of all files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb555-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="fb555-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fb555-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fb555-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fb555-110">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="fb555-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fb555-111">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fb555-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb555-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb555-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="fb555-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb555-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb555-114">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fb555-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb555-115">Строка, представляющая имя файла (или каталога), в котором произошел сбой метода.</span><span class="sxs-lookup"><span data-stu-id="fb555-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="fb555-116">Если метод выполнен, этот параметр имеет **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="fb555-116">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="fb555-117">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="fb555-117">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fb555-118">Строка, которая присваивает имя дочернему файлу (или каталогу), используемому в качестве отправной точки для метода.</span><span class="sxs-lookup"><span data-stu-id="fb555-118">String that names the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="fb555-119">Как правило, этот параметр представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="fb555-119">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="fb555-120">Если этот параметр имеет **значение NULL**, операция выполняется над файлом (или каталогом), указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="fb555-120">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="fb555-121">*Рекурсивно* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="fb555-121">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fb555-122">Если **значение — true**, метод также применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="fb555-122">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="fb555-123">Для экземпляров файлов этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="fb555-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb555-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb555-124">Return value</span></span>

<span data-ttu-id="fb555-125">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="fb555-125">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="fb555-126">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="fb555-126">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="fb555-127">0</span><span class="sxs-lookup"><span data-stu-id="fb555-127">0</span></span>

<span data-ttu-id="fb555-128">Успешно.</span><span class="sxs-lookup"><span data-stu-id="fb555-128">Success.</span></span>

</dd> <dt>

<span data-ttu-id="fb555-129">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="fb555-129">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="fb555-130">2</span><span class="sxs-lookup"><span data-stu-id="fb555-130">2</span></span>

<span data-ttu-id="fb555-131">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="fb555-131">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="fb555-132">**Неопределенный сбой**</span><span class="sxs-lookup"><span data-stu-id="fb555-132">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="fb555-133">8</span><span class="sxs-lookup"><span data-stu-id="fb555-133">8</span></span>

<span data-ttu-id="fb555-134">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="fb555-134">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="fb555-135">**Недопустимый объект**</span><span class="sxs-lookup"><span data-stu-id="fb555-135">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="fb555-136">9</span><span class="sxs-lookup"><span data-stu-id="fb555-136">9</span></span>

<span data-ttu-id="fb555-137">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="fb555-137">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="fb555-138">**Объект уже существует**</span><span class="sxs-lookup"><span data-stu-id="fb555-138">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="fb555-139">10</span><span class="sxs-lookup"><span data-stu-id="fb555-139">10</span></span>

<span data-ttu-id="fb555-140">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="fb555-140">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="fb555-141">**Файловая система не NTFS**</span><span class="sxs-lookup"><span data-stu-id="fb555-141">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="fb555-142">11</span><span class="sxs-lookup"><span data-stu-id="fb555-142">11</span></span>

<span data-ttu-id="fb555-143">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="fb555-143">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="fb555-144">**Платформа не NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="fb555-144">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="fb555-145">12</span><span class="sxs-lookup"><span data-stu-id="fb555-145">12</span></span>

<span data-ttu-id="fb555-146">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="fb555-146">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="fb555-147">**Диск не совпадает**</span><span class="sxs-lookup"><span data-stu-id="fb555-147">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="fb555-148">13</span><span class="sxs-lookup"><span data-stu-id="fb555-148">13</span></span>

<span data-ttu-id="fb555-149">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="fb555-149">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="fb555-150">**Каталог не пуст**</span><span class="sxs-lookup"><span data-stu-id="fb555-150">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="fb555-151">14</span><span class="sxs-lookup"><span data-stu-id="fb555-151">14</span></span>

<span data-ttu-id="fb555-152">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="fb555-152">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="fb555-153">**Нарушение общего доступа**</span><span class="sxs-lookup"><span data-stu-id="fb555-153">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="fb555-154">15</span><span class="sxs-lookup"><span data-stu-id="fb555-154">15</span></span>

<span data-ttu-id="fb555-155">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="fb555-155">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="fb555-156">**Недопустимый файл запуска**</span><span class="sxs-lookup"><span data-stu-id="fb555-156">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="fb555-157">16</span><span class="sxs-lookup"><span data-stu-id="fb555-157">16</span></span>

<span data-ttu-id="fb555-158">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="fb555-158">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="fb555-159">**Привилегия не удерживается**</span><span class="sxs-lookup"><span data-stu-id="fb555-159">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="fb555-160">17</span><span class="sxs-lookup"><span data-stu-id="fb555-160">17</span></span>

<span data-ttu-id="fb555-161">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="fb555-161">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="fb555-162">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="fb555-162">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="fb555-163">21</span><span class="sxs-lookup"><span data-stu-id="fb555-163">21</span></span>

<span data-ttu-id="fb555-164">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="fb555-164">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb555-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fb555-165">Remarks</span></span>

<span data-ttu-id="fb555-166">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="fb555-166">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="fb555-167">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="fb555-167">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="fb555-168">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="fb555-168">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fb555-169">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="fb555-169">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb555-170">Требования</span><span class="sxs-lookup"><span data-stu-id="fb555-170">Requirements</span></span>



| <span data-ttu-id="fb555-171">Требование</span><span class="sxs-lookup"><span data-stu-id="fb555-171">Requirement</span></span> | <span data-ttu-id="fb555-172">Значение</span><span class="sxs-lookup"><span data-stu-id="fb555-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb555-173">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb555-173">Minimum supported client</span></span><br/> | <span data-ttu-id="fb555-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb555-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fb555-175">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb555-175">Minimum supported server</span></span><br/> | <span data-ttu-id="fb555-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb555-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fb555-177">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fb555-177">Namespace</span></span><br/>                | <span data-ttu-id="fb555-178">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fb555-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fb555-179">MOF</span><span class="sxs-lookup"><span data-stu-id="fb555-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb555-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb555-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb555-181">DLL</span><span class="sxs-lookup"><span data-stu-id="fb555-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb555-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb555-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb555-183">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb555-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb555-184">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="fb555-184">CIM\_LogicalFile</span></span>](takeownershipex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="fb555-185">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="fb555-185">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

