---
description: Метод Делетикс удаляет логический файл (или каталог), указанный в пути объекта. Этот метод является расширенной версией метода Delete.
ms.assetid: 53785f2e-8796-446c-8228-9abc2d9a0d68
ms.tgt_platform: multiple
title: Метод Делетикс класса CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4f9799513111ff53bb97c14feaf70c922dfb085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538702"
---
# <a name="deleteex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="0f28f-104">Метод Делетикс \_ класса CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="0f28f-104">DeleteEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="0f28f-105">Метод **делетикс** удаляет логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="0f28f-105">The **DeleteEx** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="0f28f-106">Этот метод является расширенной версией метода [**Delete**](delete-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="0f28f-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0f28f-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="0f28f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0f28f-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0f28f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0f28f-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="0f28f-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0f28f-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0f28f-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f28f-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f28f-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="0f28f-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f28f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f28f-113">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0f28f-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f28f-114">Строка, представляющая имя файла (или каталога), в котором произошел сбой метода.</span><span class="sxs-lookup"><span data-stu-id="0f28f-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="0f28f-115">Если метод выполнен, этот параметр имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="0f28f-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="0f28f-116">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="0f28f-116">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0f28f-117">Строка, которая присваивает имя дочернему файлу (или каталогу), используемому в качестве отправной точки для метода.</span><span class="sxs-lookup"><span data-stu-id="0f28f-117">String that names the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="0f28f-118">Как правило, этот параметр представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="0f28f-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="0f28f-119">Если этот параметр имеет значение null, операция выполняется над файлом или каталогом, указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="0f28f-119">If this parameter is null, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f28f-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f28f-120">Return value</span></span>

<span data-ttu-id="0f28f-121">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="0f28f-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="0f28f-122">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="0f28f-122">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="0f28f-123">0</span><span class="sxs-lookup"><span data-stu-id="0f28f-123">0</span></span>

<span data-ttu-id="0f28f-124">Успешно.</span><span class="sxs-lookup"><span data-stu-id="0f28f-124">Success.</span></span>

</dd> <dt>

<span data-ttu-id="0f28f-125">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="0f28f-125">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="0f28f-126">2</span><span class="sxs-lookup"><span data-stu-id="0f28f-126">2</span></span>

<span data-ttu-id="0f28f-127">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="0f28f-127">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="0f28f-128">**Неопределенный сбой**</span><span class="sxs-lookup"><span data-stu-id="0f28f-128">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="0f28f-129">8</span><span class="sxs-lookup"><span data-stu-id="0f28f-129">8</span></span>

<span data-ttu-id="0f28f-130">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="0f28f-130">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="0f28f-131">**Недопустимый объект**</span><span class="sxs-lookup"><span data-stu-id="0f28f-131">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="0f28f-132">9</span><span class="sxs-lookup"><span data-stu-id="0f28f-132">9</span></span>

<span data-ttu-id="0f28f-133">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="0f28f-133">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="0f28f-134">**Объект уже существует**</span><span class="sxs-lookup"><span data-stu-id="0f28f-134">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="0f28f-135">10</span><span class="sxs-lookup"><span data-stu-id="0f28f-135">10</span></span>

<span data-ttu-id="0f28f-136">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="0f28f-136">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="0f28f-137">**Файловая система не NTFS**</span><span class="sxs-lookup"><span data-stu-id="0f28f-137">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="0f28f-138">11</span><span class="sxs-lookup"><span data-stu-id="0f28f-138">11</span></span>

<span data-ttu-id="0f28f-139">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="0f28f-139">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="0f28f-140">**Платформа не NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="0f28f-140">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="0f28f-141">12</span><span class="sxs-lookup"><span data-stu-id="0f28f-141">12</span></span>

<span data-ttu-id="0f28f-142">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="0f28f-142">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="0f28f-143">**Диск не совпадает**</span><span class="sxs-lookup"><span data-stu-id="0f28f-143">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="0f28f-144">13</span><span class="sxs-lookup"><span data-stu-id="0f28f-144">13</span></span>

<span data-ttu-id="0f28f-145">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="0f28f-145">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="0f28f-146">**Каталог не пуст**</span><span class="sxs-lookup"><span data-stu-id="0f28f-146">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="0f28f-147">14</span><span class="sxs-lookup"><span data-stu-id="0f28f-147">14</span></span>

<span data-ttu-id="0f28f-148">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="0f28f-148">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="0f28f-149">**Нарушение общего доступа**</span><span class="sxs-lookup"><span data-stu-id="0f28f-149">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="0f28f-150">15</span><span class="sxs-lookup"><span data-stu-id="0f28f-150">15</span></span>

<span data-ttu-id="0f28f-151">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="0f28f-151">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="0f28f-152">**Недопустимый файл запуска**</span><span class="sxs-lookup"><span data-stu-id="0f28f-152">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="0f28f-153">16</span><span class="sxs-lookup"><span data-stu-id="0f28f-153">16</span></span>

<span data-ttu-id="0f28f-154">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="0f28f-154">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="0f28f-155">**Привилегия не удерживается**</span><span class="sxs-lookup"><span data-stu-id="0f28f-155">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="0f28f-156">17</span><span class="sxs-lookup"><span data-stu-id="0f28f-156">17</span></span>

<span data-ttu-id="0f28f-157">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="0f28f-157">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="0f28f-158">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="0f28f-158">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="0f28f-159">21</span><span class="sxs-lookup"><span data-stu-id="0f28f-159">21</span></span>

<span data-ttu-id="0f28f-160">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="0f28f-160">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f28f-161">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f28f-161">Remarks</span></span>

<span data-ttu-id="0f28f-162">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="0f28f-162">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="0f28f-163">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="0f28f-163">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="0f28f-164">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="0f28f-164">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0f28f-165">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0f28f-165">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f28f-166">Требования</span><span class="sxs-lookup"><span data-stu-id="0f28f-166">Requirements</span></span>



| <span data-ttu-id="0f28f-167">Требование</span><span class="sxs-lookup"><span data-stu-id="0f28f-167">Requirement</span></span> | <span data-ttu-id="0f28f-168">Значение</span><span class="sxs-lookup"><span data-stu-id="0f28f-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f28f-169">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f28f-169">Minimum supported client</span></span><br/> | <span data-ttu-id="0f28f-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f28f-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0f28f-171">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f28f-171">Minimum supported server</span></span><br/> | <span data-ttu-id="0f28f-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f28f-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0f28f-173">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0f28f-173">Namespace</span></span><br/>                | <span data-ttu-id="0f28f-174">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0f28f-174">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0f28f-175">MOF</span><span class="sxs-lookup"><span data-stu-id="0f28f-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f28f-176"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f28f-176"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f28f-177">DLL</span><span class="sxs-lookup"><span data-stu-id="0f28f-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f28f-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f28f-178"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f28f-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f28f-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f28f-180">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="0f28f-180">CIM\_LogicalFile</span></span>](deleteex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="0f28f-181">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="0f28f-181">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

