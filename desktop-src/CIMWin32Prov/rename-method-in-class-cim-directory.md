---
description: Переименовывает логический файл (или каталог), указанный в пути объекта. Переименование не поддерживается, если место назначения находится на другом диске или требуется перезапись существующего логического файла.
ms.assetid: 728737a7-7cb8-4237-be03-16c4dac530b2
ms.tgt_platform: multiple
title: Метод Rename класса CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83429f3a5248b1d3be24832b26bf99213d442ce5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496551"
---
# <a name="rename-method-of-the-cim_directory-class"></a><span data-ttu-id="d804c-104">Переименование метода \_ класса каталога CIM</span><span class="sxs-lookup"><span data-stu-id="d804c-104">Rename method of the CIM\_Directory class</span></span>

<span data-ttu-id="d804c-105">Метод **Rename** переименовывает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="d804c-105">The **Rename** method renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="d804c-106">Переименование не поддерживается, если место назначения находится на другом диске или требуется перезапись существующего логического файла.</span><span class="sxs-lookup"><span data-stu-id="d804c-106">Renaming is not supported if the destination is on another drive or overwriting an existing logical file is required.</span></span>

<span data-ttu-id="d804c-107">Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="d804c-107">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d804c-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="d804c-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d804c-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d804c-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d804c-110">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="d804c-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d804c-111">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d804c-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d804c-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d804c-112">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="d804c-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="d804c-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d804c-114">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d804c-114">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d804c-115">Полное новое имя файла (или каталога).</span><span class="sxs-lookup"><span data-stu-id="d804c-115">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="d804c-116">Пример: "c: \\ temp \\newname.txt"</span><span class="sxs-lookup"><span data-stu-id="d804c-116">Example: "c:\\temp\\newname.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d804c-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d804c-117">Return value</span></span>

<span data-ttu-id="d804c-118">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="d804c-118">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d804c-119">**0**</span><span class="sxs-lookup"><span data-stu-id="d804c-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d804c-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="d804c-120">Success.</span></span>

</dd> <dt>

<span data-ttu-id="d804c-121">**2**</span><span class="sxs-lookup"><span data-stu-id="d804c-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d804c-122">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="d804c-122">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="d804c-123">**8**</span><span class="sxs-lookup"><span data-stu-id="d804c-123">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d804c-124">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="d804c-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="d804c-125">**9**</span><span class="sxs-lookup"><span data-stu-id="d804c-125">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d804c-126">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="d804c-126">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="d804c-127">**10**</span><span class="sxs-lookup"><span data-stu-id="d804c-127">**10**</span></span>
</dt> <dd>

<span data-ttu-id="d804c-128">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="d804c-128">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d804c-129">**11**</span><span class="sxs-lookup"><span data-stu-id="d804c-129">**11**</span></span>
</dt> <dd>

<span data-ttu-id="d804c-130">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="d804c-130">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="d804c-131">**12**</span><span class="sxs-lookup"><span data-stu-id="d804c-131">**12**</span></span>
</dt> <dd>

<span data-ttu-id="d804c-132">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="d804c-132">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="d804c-133">**13**</span><span class="sxs-lookup"><span data-stu-id="d804c-133">**13**</span></span>
</dt> <dd>

<span data-ttu-id="d804c-134">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="d804c-134">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="d804c-135">**14**</span><span class="sxs-lookup"><span data-stu-id="d804c-135">**14**</span></span>
</dt> <dd>

<span data-ttu-id="d804c-136">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="d804c-136">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="d804c-137">**15**</span><span class="sxs-lookup"><span data-stu-id="d804c-137">**15**</span></span>
</dt> <dd>

<span data-ttu-id="d804c-138">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="d804c-138">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="d804c-139">**16**</span><span class="sxs-lookup"><span data-stu-id="d804c-139">**16**</span></span>
</dt> <dd>

<span data-ttu-id="d804c-140">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="d804c-140">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="d804c-141">**17**</span><span class="sxs-lookup"><span data-stu-id="d804c-141">**17**</span></span>
</dt> <dd>

<span data-ttu-id="d804c-142">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="d804c-142">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="d804c-143">**открыт**</span><span class="sxs-lookup"><span data-stu-id="d804c-143">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d804c-144">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="d804c-144">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d804c-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d804c-145">Remarks</span></span>

<span data-ttu-id="d804c-146">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="d804c-146">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="d804c-147">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="d804c-147">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="d804c-148">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="d804c-148">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d804c-149">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="d804c-149">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d804c-150">Требования</span><span class="sxs-lookup"><span data-stu-id="d804c-150">Requirements</span></span>



| <span data-ttu-id="d804c-151">Требование</span><span class="sxs-lookup"><span data-stu-id="d804c-151">Requirement</span></span> | <span data-ttu-id="d804c-152">Значение</span><span class="sxs-lookup"><span data-stu-id="d804c-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d804c-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d804c-153">Minimum supported client</span></span><br/> | <span data-ttu-id="d804c-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d804c-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d804c-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d804c-155">Minimum supported server</span></span><br/> | <span data-ttu-id="d804c-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d804c-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d804c-157">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d804c-157">Namespace</span></span><br/>                | <span data-ttu-id="d804c-158">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d804c-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d804c-159">MOF</span><span class="sxs-lookup"><span data-stu-id="d804c-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d804c-160"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d804c-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d804c-161">DLL</span><span class="sxs-lookup"><span data-stu-id="d804c-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d804c-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d804c-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d804c-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d804c-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d804c-164">\_Каталог CIM</span><span class="sxs-lookup"><span data-stu-id="d804c-164">CIM\_Directory</span></span>](rename-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="d804c-165">**\_Каталог CIM**</span><span class="sxs-lookup"><span data-stu-id="d804c-165">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

