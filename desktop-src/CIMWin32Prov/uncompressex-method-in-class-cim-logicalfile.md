---
description: Распаковывает логический файл (или каталог), указанный в пути объекта. Этот метод является расширенной версией метода uncompressия.
ms.assetid: 383475ba-77d4-4bfb-a241-9c37aa594a1e
ms.tgt_platform: multiple
title: Метод Ункомпрессекс класса CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c514939425625c15f3b683e4dc10bd5e05cb511
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807852"
---
# <a name="uncompressex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="3b554-104">Метод Ункомпрессекс \_ класса CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="3b554-104">UncompressEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="3b554-105">Метод **ункомпрессекс** распаковывает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="3b554-105">The **UncompressEx** method uncompresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="3b554-106">Этот метод является расширенной версией метода [**uncompressия**](uncompress-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="3b554-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3b554-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="3b554-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3b554-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3b554-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3b554-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="3b554-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3b554-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3b554-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3b554-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b554-111">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="3b554-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b554-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b554-113">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3b554-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b554-114">Имя файла (или каталога), в котором произошел сбой метода.</span><span class="sxs-lookup"><span data-stu-id="3b554-114">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="3b554-115">Если метод выполнен, этот параметр имеет **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="3b554-115">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="3b554-116">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="3b554-116">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3b554-117">Имя дочернего файла (или каталога), который будет использоваться в качестве отправной точки для метода.</span><span class="sxs-lookup"><span data-stu-id="3b554-117">Name of the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="3b554-118">Как правило, этот параметр представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="3b554-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="3b554-119">Если этот параметр имеет **значение NULL**, операция выполняется над файлом или каталогом, указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="3b554-119">If this parameter is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="3b554-120">*Рекурсивно* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="3b554-120">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3b554-121">Если **значение — true**, метод также применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="3b554-121">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="3b554-122">Для экземпляров файлов этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="3b554-122">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b554-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b554-123">Return value</span></span>

<span data-ttu-id="3b554-124">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="3b554-124">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="3b554-125">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="3b554-125">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="3b554-126">0</span><span class="sxs-lookup"><span data-stu-id="3b554-126">0</span></span>

<span data-ttu-id="3b554-127">Успешно.</span><span class="sxs-lookup"><span data-stu-id="3b554-127">Success.</span></span>

</dd> <dt>

<span data-ttu-id="3b554-128">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="3b554-128">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="3b554-129">2</span><span class="sxs-lookup"><span data-stu-id="3b554-129">2</span></span>

<span data-ttu-id="3b554-130">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="3b554-130">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="3b554-131">**Неопределенный сбой**</span><span class="sxs-lookup"><span data-stu-id="3b554-131">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="3b554-132">8</span><span class="sxs-lookup"><span data-stu-id="3b554-132">8</span></span>

<span data-ttu-id="3b554-133">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="3b554-133">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="3b554-134">**Недопустимый объект**</span><span class="sxs-lookup"><span data-stu-id="3b554-134">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="3b554-135">9</span><span class="sxs-lookup"><span data-stu-id="3b554-135">9</span></span>

<span data-ttu-id="3b554-136">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="3b554-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="3b554-137">**Объект уже существует**</span><span class="sxs-lookup"><span data-stu-id="3b554-137">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="3b554-138">10</span><span class="sxs-lookup"><span data-stu-id="3b554-138">10</span></span>

<span data-ttu-id="3b554-139">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="3b554-139">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3b554-140">**Файловая система не NTFS**</span><span class="sxs-lookup"><span data-stu-id="3b554-140">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="3b554-141">11</span><span class="sxs-lookup"><span data-stu-id="3b554-141">11</span></span>

<span data-ttu-id="3b554-142">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="3b554-142">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="3b554-143">**Платформа не NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="3b554-143">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="3b554-144">12</span><span class="sxs-lookup"><span data-stu-id="3b554-144">12</span></span>

<span data-ttu-id="3b554-145">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="3b554-145">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="3b554-146">**Диск не совпадает**</span><span class="sxs-lookup"><span data-stu-id="3b554-146">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="3b554-147">13</span><span class="sxs-lookup"><span data-stu-id="3b554-147">13</span></span>

<span data-ttu-id="3b554-148">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="3b554-148">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="3b554-149">**Каталог не пуст**</span><span class="sxs-lookup"><span data-stu-id="3b554-149">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="3b554-150">14</span><span class="sxs-lookup"><span data-stu-id="3b554-150">14</span></span>

<span data-ttu-id="3b554-151">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="3b554-151">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="3b554-152">**Нарушение общего доступа**</span><span class="sxs-lookup"><span data-stu-id="3b554-152">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="3b554-153">15</span><span class="sxs-lookup"><span data-stu-id="3b554-153">15</span></span>

<span data-ttu-id="3b554-154">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="3b554-154">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="3b554-155">**Недопустимый файл запуска**</span><span class="sxs-lookup"><span data-stu-id="3b554-155">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="3b554-156">16</span><span class="sxs-lookup"><span data-stu-id="3b554-156">16</span></span>

<span data-ttu-id="3b554-157">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="3b554-157">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="3b554-158">**Привилегия не удерживается**</span><span class="sxs-lookup"><span data-stu-id="3b554-158">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="3b554-159">17</span><span class="sxs-lookup"><span data-stu-id="3b554-159">17</span></span>

<span data-ttu-id="3b554-160">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="3b554-160">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="3b554-161">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="3b554-161">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3b554-162">21</span><span class="sxs-lookup"><span data-stu-id="3b554-162">21</span></span>

<span data-ttu-id="3b554-163">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="3b554-163">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b554-164">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b554-164">Remarks</span></span>

<span data-ttu-id="3b554-165">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="3b554-165">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="3b554-166">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="3b554-166">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="3b554-167">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="3b554-167">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3b554-168">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="3b554-168">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b554-169">Требования</span><span class="sxs-lookup"><span data-stu-id="3b554-169">Requirements</span></span>



| <span data-ttu-id="3b554-170">Требование</span><span class="sxs-lookup"><span data-stu-id="3b554-170">Requirement</span></span> | <span data-ttu-id="3b554-171">Значение</span><span class="sxs-lookup"><span data-stu-id="3b554-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b554-172">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3b554-172">Minimum supported client</span></span><br/> | <span data-ttu-id="3b554-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b554-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3b554-174">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3b554-174">Minimum supported server</span></span><br/> | <span data-ttu-id="3b554-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b554-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3b554-176">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3b554-176">Namespace</span></span><br/>                | <span data-ttu-id="3b554-177">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3b554-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3b554-178">MOF</span><span class="sxs-lookup"><span data-stu-id="3b554-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b554-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b554-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b554-180">DLL</span><span class="sxs-lookup"><span data-stu-id="3b554-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b554-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b554-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b554-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b554-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b554-183">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="3b554-183">CIM\_LogicalFile</span></span>](uncompressex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="3b554-184">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="3b554-184">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

