---
description: Копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное параметром FileName.
ms.assetid: 534d8b73-fc22-4a42-b8e6-24a54353bb14
ms.tgt_platform: multiple
title: Метод Копекс класса CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ec7c44ec3fc01074a0f4af70249236aa366d64bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656081"
---
# <a name="copyex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="089a0-103">Метод Копекс \_ класса CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="089a0-103">CopyEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="089a0-104">Метод **копекс** копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное параметром *filename* .</span><span class="sxs-lookup"><span data-stu-id="089a0-104">The **CopyEx** method copies the logical file (or directory) specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="089a0-105">Копирование не поддерживается, если требуется перезапись существующего логического файла.</span><span class="sxs-lookup"><span data-stu-id="089a0-105">A copy is not supported if overwriting an existing logical file is required.</span></span> <span data-ttu-id="089a0-106">Этот метод является расширенной версией метода [**Copy**](copy-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="089a0-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="089a0-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="089a0-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="089a0-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="089a0-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="089a0-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="089a0-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="089a0-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="089a0-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="089a0-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="089a0-111">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="089a0-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="089a0-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="089a0-113">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="089a0-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="089a0-114">Полное имя целевого файла (или каталога).</span><span class="sxs-lookup"><span data-stu-id="089a0-114">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="089a0-115">Пример: "c: \\ temp \\ невдиректори"</span><span class="sxs-lookup"><span data-stu-id="089a0-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="089a0-116">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="089a0-116">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="089a0-117">Строка, представляющая имя файла (или каталога), в котором произошел сбой метода.</span><span class="sxs-lookup"><span data-stu-id="089a0-117">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="089a0-118">Если метод выполнен, этот параметр имеет **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="089a0-118">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="089a0-119">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="089a0-119">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="089a0-120">Строка, которая присваивает имя дочернему файлу (или каталогу), используемому в качестве отправной точки для этого метода.</span><span class="sxs-lookup"><span data-stu-id="089a0-120">String that names the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="089a0-121">Как правило, параметр *StartFileName* — это параметр *стопфиленаме* , указывающий файл (или каталог), в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="089a0-121">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="089a0-122">Если этот параметр имеет **значение NULL**, операция выполняется над файлом или каталогом, указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="089a0-122">If this parameter is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="089a0-123">*Рекурсивно* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="089a0-123">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="089a0-124">Если значение — TRUE, метод также применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="089a0-124">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="089a0-125">Для экземпляров файлов этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="089a0-125">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="089a0-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="089a0-126">Return value</span></span>

<span data-ttu-id="089a0-127">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="089a0-127">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="089a0-128">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="089a0-128">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="089a0-129">0</span><span class="sxs-lookup"><span data-stu-id="089a0-129">0</span></span>

<span data-ttu-id="089a0-130">Успешно.</span><span class="sxs-lookup"><span data-stu-id="089a0-130">Success.</span></span>

</dd> <dt>

<span data-ttu-id="089a0-131">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="089a0-131">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="089a0-132">2</span><span class="sxs-lookup"><span data-stu-id="089a0-132">2</span></span>

<span data-ttu-id="089a0-133">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="089a0-133">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="089a0-134">**Неопределенный сбой**</span><span class="sxs-lookup"><span data-stu-id="089a0-134">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="089a0-135">8</span><span class="sxs-lookup"><span data-stu-id="089a0-135">8</span></span>

<span data-ttu-id="089a0-136">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="089a0-136">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="089a0-137">**Недопустимый объект**</span><span class="sxs-lookup"><span data-stu-id="089a0-137">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="089a0-138">9</span><span class="sxs-lookup"><span data-stu-id="089a0-138">9</span></span>

<span data-ttu-id="089a0-139">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="089a0-139">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="089a0-140">**Объект уже существует**</span><span class="sxs-lookup"><span data-stu-id="089a0-140">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="089a0-141">10</span><span class="sxs-lookup"><span data-stu-id="089a0-141">10</span></span>

<span data-ttu-id="089a0-142">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="089a0-142">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="089a0-143">**Файловая система не NTFS**</span><span class="sxs-lookup"><span data-stu-id="089a0-143">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="089a0-144">11</span><span class="sxs-lookup"><span data-stu-id="089a0-144">11</span></span>

<span data-ttu-id="089a0-145">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="089a0-145">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="089a0-146">**Платформа не NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="089a0-146">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="089a0-147">12</span><span class="sxs-lookup"><span data-stu-id="089a0-147">12</span></span>

<span data-ttu-id="089a0-148">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="089a0-148">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="089a0-149">**Диск не совпадает**</span><span class="sxs-lookup"><span data-stu-id="089a0-149">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="089a0-150">13</span><span class="sxs-lookup"><span data-stu-id="089a0-150">13</span></span>

<span data-ttu-id="089a0-151">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="089a0-151">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="089a0-152">**Каталог не пуст**</span><span class="sxs-lookup"><span data-stu-id="089a0-152">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="089a0-153">14</span><span class="sxs-lookup"><span data-stu-id="089a0-153">14</span></span>

<span data-ttu-id="089a0-154">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="089a0-154">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="089a0-155">**Нарушение общего доступа**</span><span class="sxs-lookup"><span data-stu-id="089a0-155">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="089a0-156">15</span><span class="sxs-lookup"><span data-stu-id="089a0-156">15</span></span>

<span data-ttu-id="089a0-157">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="089a0-157">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="089a0-158">**Недопустимый файл запуска**</span><span class="sxs-lookup"><span data-stu-id="089a0-158">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="089a0-159">16</span><span class="sxs-lookup"><span data-stu-id="089a0-159">16</span></span>

<span data-ttu-id="089a0-160">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="089a0-160">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="089a0-161">**Привилегия не удерживается**</span><span class="sxs-lookup"><span data-stu-id="089a0-161">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="089a0-162">17</span><span class="sxs-lookup"><span data-stu-id="089a0-162">17</span></span>

<span data-ttu-id="089a0-163">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="089a0-163">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="089a0-164">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="089a0-164">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="089a0-165">21</span><span class="sxs-lookup"><span data-stu-id="089a0-165">21</span></span>

<span data-ttu-id="089a0-166">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="089a0-166">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="089a0-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="089a0-167">Remarks</span></span>

<span data-ttu-id="089a0-168">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="089a0-168">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="089a0-169">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="089a0-169">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="089a0-170">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="089a0-170">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="089a0-171">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="089a0-171">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="089a0-172">Требования</span><span class="sxs-lookup"><span data-stu-id="089a0-172">Requirements</span></span>



| <span data-ttu-id="089a0-173">Требование</span><span class="sxs-lookup"><span data-stu-id="089a0-173">Requirement</span></span> | <span data-ttu-id="089a0-174">Значение</span><span class="sxs-lookup"><span data-stu-id="089a0-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="089a0-175">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="089a0-175">Minimum supported client</span></span><br/> | <span data-ttu-id="089a0-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="089a0-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="089a0-177">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="089a0-177">Minimum supported server</span></span><br/> | <span data-ttu-id="089a0-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="089a0-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="089a0-179">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="089a0-179">Namespace</span></span><br/>                | <span data-ttu-id="089a0-180">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="089a0-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="089a0-181">MOF</span><span class="sxs-lookup"><span data-stu-id="089a0-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="089a0-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="089a0-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="089a0-183">DLL</span><span class="sxs-lookup"><span data-stu-id="089a0-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="089a0-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="089a0-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="089a0-185">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="089a0-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="089a0-186">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="089a0-186">CIM\_LogicalFile</span></span>](copyex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="089a0-187">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="089a0-187">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

