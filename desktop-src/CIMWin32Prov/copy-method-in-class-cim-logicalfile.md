---
description: Метод Copy класса CIM_LogicalFile. метод Copy копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное входным параметром.
ms.assetid: 643946e4-5d32-4839-ae1f-80ec7cede429
ms.tgt_platform: multiple
title: Метод Copy класса CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10ba9c28bde9d909d947e5a73241ce1aa8f1e956
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089732"
---
# <a name="copy-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="906e4-103">Метод Copy \_ класса CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="906e4-103">Copy method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="906e4-104">Метод **Copy** копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное входным параметром.</span><span class="sxs-lookup"><span data-stu-id="906e4-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="906e4-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="906e4-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="906e4-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="906e4-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="906e4-107">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="906e4-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="906e4-108">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="906e4-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="906e4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="906e4-109">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="906e4-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="906e4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="906e4-111">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="906e4-111">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="906e4-112">Полное имя целевого файла (или каталога).</span><span class="sxs-lookup"><span data-stu-id="906e4-112">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="906e4-113">Пример: "c: \\ temp \\ невдиректори"</span><span class="sxs-lookup"><span data-stu-id="906e4-113">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="906e4-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="906e4-114">Return value</span></span>

<span data-ttu-id="906e4-115">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="906e4-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="906e4-116">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="906e4-116">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="906e4-117">0</span><span class="sxs-lookup"><span data-stu-id="906e4-117">0</span></span>

<span data-ttu-id="906e4-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="906e4-118">Success.</span></span>

</dd> <dt>

<span data-ttu-id="906e4-119">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="906e4-119">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="906e4-120">2</span><span class="sxs-lookup"><span data-stu-id="906e4-120">2</span></span>

<span data-ttu-id="906e4-121">Access denied. (Недопустимое значение {значение_утверждения} для утверждения {имя_утверждения}. Доступ запрещен.)</span><span class="sxs-lookup"><span data-stu-id="906e4-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="906e4-122">**Неопределенный сбой**</span><span class="sxs-lookup"><span data-stu-id="906e4-122">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="906e4-123">8</span><span class="sxs-lookup"><span data-stu-id="906e4-123">8</span></span>

<span data-ttu-id="906e4-124">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="906e4-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="906e4-125">**Недопустимый объект**</span><span class="sxs-lookup"><span data-stu-id="906e4-125">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="906e4-126">9</span><span class="sxs-lookup"><span data-stu-id="906e4-126">9</span></span>

<span data-ttu-id="906e4-127">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="906e4-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="906e4-128">**Объект уже существует**</span><span class="sxs-lookup"><span data-stu-id="906e4-128">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="906e4-129">10</span><span class="sxs-lookup"><span data-stu-id="906e4-129">10</span></span>

<span data-ttu-id="906e4-130">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="906e4-130">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="906e4-131">**Файловая система не NTFS**</span><span class="sxs-lookup"><span data-stu-id="906e4-131">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="906e4-132">11</span><span class="sxs-lookup"><span data-stu-id="906e4-132">11</span></span>

<span data-ttu-id="906e4-133">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="906e4-133">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="906e4-134">**Платформа не NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="906e4-134">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="906e4-135">12</span><span class="sxs-lookup"><span data-stu-id="906e4-135">12</span></span>

<span data-ttu-id="906e4-136">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="906e4-136">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="906e4-137">**Диск не совпадает**</span><span class="sxs-lookup"><span data-stu-id="906e4-137">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="906e4-138">13</span><span class="sxs-lookup"><span data-stu-id="906e4-138">13</span></span>

<span data-ttu-id="906e4-139">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="906e4-139">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="906e4-140">**Каталог не пуст**</span><span class="sxs-lookup"><span data-stu-id="906e4-140">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="906e4-141">14</span><span class="sxs-lookup"><span data-stu-id="906e4-141">14</span></span>

<span data-ttu-id="906e4-142">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="906e4-142">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="906e4-143">**Нарушение общего доступа**</span><span class="sxs-lookup"><span data-stu-id="906e4-143">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="906e4-144">15</span><span class="sxs-lookup"><span data-stu-id="906e4-144">15</span></span>

<span data-ttu-id="906e4-145">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="906e4-145">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="906e4-146">**Недопустимый файл запуска**</span><span class="sxs-lookup"><span data-stu-id="906e4-146">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="906e4-147">16</span><span class="sxs-lookup"><span data-stu-id="906e4-147">16</span></span>

<span data-ttu-id="906e4-148">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="906e4-148">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="906e4-149">**Привилегия не удерживается**</span><span class="sxs-lookup"><span data-stu-id="906e4-149">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="906e4-150">17</span><span class="sxs-lookup"><span data-stu-id="906e4-150">17</span></span>

<span data-ttu-id="906e4-151">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="906e4-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="906e4-152">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="906e4-152">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="906e4-153">21</span><span class="sxs-lookup"><span data-stu-id="906e4-153">21</span></span>

<span data-ttu-id="906e4-154">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="906e4-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="906e4-155">Remarks</span><span class="sxs-lookup"><span data-stu-id="906e4-155">Remarks</span></span>

<span data-ttu-id="906e4-156">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="906e4-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="906e4-157">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="906e4-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="906e4-158">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="906e4-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="906e4-159">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="906e4-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="906e4-160">Требования</span><span class="sxs-lookup"><span data-stu-id="906e4-160">Requirements</span></span>



| <span data-ttu-id="906e4-161">Требование</span><span class="sxs-lookup"><span data-stu-id="906e4-161">Requirement</span></span> | <span data-ttu-id="906e4-162">Значение</span><span class="sxs-lookup"><span data-stu-id="906e4-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="906e4-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="906e4-163">Minimum supported client</span></span><br/> | <span data-ttu-id="906e4-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="906e4-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="906e4-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="906e4-165">Minimum supported server</span></span><br/> | <span data-ttu-id="906e4-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="906e4-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="906e4-167">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="906e4-167">Namespace</span></span><br/>                | <span data-ttu-id="906e4-168">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="906e4-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="906e4-169">MOF</span><span class="sxs-lookup"><span data-stu-id="906e4-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="906e4-170"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="906e4-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="906e4-171">DLL</span><span class="sxs-lookup"><span data-stu-id="906e4-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="906e4-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="906e4-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="906e4-173">См. также</span><span class="sxs-lookup"><span data-stu-id="906e4-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="906e4-174">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="906e4-174">CIM\_LogicalFile</span></span>](copy-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="906e4-175">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="906e4-175">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

