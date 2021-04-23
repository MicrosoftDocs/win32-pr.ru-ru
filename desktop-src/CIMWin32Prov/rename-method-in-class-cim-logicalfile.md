---
description: Метод Rename переименовывает логический файл (или каталог), указанный в пути объекта. Переименование не поддерживается, если место назначения находится на другом диске или требуется перезапись существующего логического файла.
ms.assetid: 5a62ff64-d1d2-43a2-997c-0ad46896b31f
ms.tgt_platform: multiple
title: Метод Rename класса CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0da38020d7b22dceb6f1d061f8feaf858eeb5f04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142325"
---
# <a name="rename-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="0d044-104">Метод Rename класса CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="0d044-104">Rename method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="0d044-105">Метод **Rename** переименовывает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="0d044-105">The **Rename** method renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="0d044-106">Переименование не поддерживается, если место назначения находится на другом диске или требуется перезапись существующего логического файла.</span><span class="sxs-lookup"><span data-stu-id="0d044-106">Renaming is not supported if the destination is on another drive, or overwriting an existing logical file is required.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d044-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="0d044-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0d044-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0d044-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0d044-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="0d044-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0d044-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0d044-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0d044-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d044-111">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="0d044-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d044-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d044-113">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d044-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d044-114">Полное имя нового файла (или каталога).</span><span class="sxs-lookup"><span data-stu-id="0d044-114">Fully qualified new file (or directory) name.</span></span>

<span data-ttu-id="0d044-115">Пример: "c: \\ temp \\newfile.txt"</span><span class="sxs-lookup"><span data-stu-id="0d044-115">Example: "c:\\temp\\newfile.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d044-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d044-116">Return value</span></span>

<span data-ttu-id="0d044-117">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="0d044-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="0d044-118">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="0d044-118">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="0d044-119">0</span><span class="sxs-lookup"><span data-stu-id="0d044-119">0</span></span>

<span data-ttu-id="0d044-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="0d044-120">Success.</span></span>

</dd> <dt>

<span data-ttu-id="0d044-121">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="0d044-121">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="0d044-122">2</span><span class="sxs-lookup"><span data-stu-id="0d044-122">2</span></span>

<span data-ttu-id="0d044-123">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="0d044-123">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="0d044-124">**Неопределенный сбой**</span><span class="sxs-lookup"><span data-stu-id="0d044-124">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="0d044-125">8</span><span class="sxs-lookup"><span data-stu-id="0d044-125">8</span></span>

<span data-ttu-id="0d044-126">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="0d044-126">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="0d044-127">**Недопустимый объект**</span><span class="sxs-lookup"><span data-stu-id="0d044-127">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="0d044-128">9</span><span class="sxs-lookup"><span data-stu-id="0d044-128">9</span></span>

<span data-ttu-id="0d044-129">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="0d044-129">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="0d044-130">**Объект уже существует**</span><span class="sxs-lookup"><span data-stu-id="0d044-130">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="0d044-131">10</span><span class="sxs-lookup"><span data-stu-id="0d044-131">10</span></span>

<span data-ttu-id="0d044-132">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="0d044-132">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0d044-133">**Файловая система не NTFS**</span><span class="sxs-lookup"><span data-stu-id="0d044-133">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="0d044-134">11</span><span class="sxs-lookup"><span data-stu-id="0d044-134">11</span></span>

<span data-ttu-id="0d044-135">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="0d044-135">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="0d044-136">**Платформа не NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="0d044-136">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="0d044-137">12</span><span class="sxs-lookup"><span data-stu-id="0d044-137">12</span></span>

<span data-ttu-id="0d044-138">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="0d044-138">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0d044-139">**Диск не совпадает**</span><span class="sxs-lookup"><span data-stu-id="0d044-139">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="0d044-140">13</span><span class="sxs-lookup"><span data-stu-id="0d044-140">13</span></span>

<span data-ttu-id="0d044-141">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="0d044-141">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="0d044-142">**Каталог не пуст**</span><span class="sxs-lookup"><span data-stu-id="0d044-142">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="0d044-143">14</span><span class="sxs-lookup"><span data-stu-id="0d044-143">14</span></span>

<span data-ttu-id="0d044-144">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="0d044-144">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="0d044-145">**Нарушение общего доступа**</span><span class="sxs-lookup"><span data-stu-id="0d044-145">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="0d044-146">15</span><span class="sxs-lookup"><span data-stu-id="0d044-146">15</span></span>

<span data-ttu-id="0d044-147">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="0d044-147">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="0d044-148">**Недопустимый файл запуска**</span><span class="sxs-lookup"><span data-stu-id="0d044-148">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="0d044-149">16</span><span class="sxs-lookup"><span data-stu-id="0d044-149">16</span></span>

<span data-ttu-id="0d044-150">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="0d044-150">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="0d044-151">**Привилегия не удерживается**</span><span class="sxs-lookup"><span data-stu-id="0d044-151">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="0d044-152">17</span><span class="sxs-lookup"><span data-stu-id="0d044-152">17</span></span>

<span data-ttu-id="0d044-153">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="0d044-153">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="0d044-154">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="0d044-154">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0d044-155">21</span><span class="sxs-lookup"><span data-stu-id="0d044-155">21</span></span>

<span data-ttu-id="0d044-156">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="0d044-156">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d044-157">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d044-157">Remarks</span></span>

<span data-ttu-id="0d044-158">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="0d044-158">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="0d044-159">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="0d044-159">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="0d044-160">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="0d044-160">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0d044-161">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0d044-161">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d044-162">Требования</span><span class="sxs-lookup"><span data-stu-id="0d044-162">Requirements</span></span>



| <span data-ttu-id="0d044-163">Требование</span><span class="sxs-lookup"><span data-stu-id="0d044-163">Requirement</span></span> | <span data-ttu-id="0d044-164">Значение</span><span class="sxs-lookup"><span data-stu-id="0d044-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d044-165">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d044-165">Minimum supported client</span></span><br/> | <span data-ttu-id="0d044-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d044-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d044-167">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d044-167">Minimum supported server</span></span><br/> | <span data-ttu-id="0d044-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d044-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d044-169">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0d044-169">Namespace</span></span><br/>                | <span data-ttu-id="0d044-170">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0d044-170">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0d044-171">MOF</span><span class="sxs-lookup"><span data-stu-id="0d044-171">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d044-172"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d044-172"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d044-173">DLL</span><span class="sxs-lookup"><span data-stu-id="0d044-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d044-174"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d044-174"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d044-175">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d044-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d044-176">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="0d044-176">CIM\_LogicalFile</span></span>](rename-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="0d044-177">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="0d044-177">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

