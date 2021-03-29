---
description: Переименовывает файл устройства (или каталог), указанный в пути объекта.
ms.assetid: 48c2eab3-c76d-4e4b-927e-dbb17584cccd
ms.tgt_platform: multiple
title: Метод Rename класса CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 484d66a1b98ea58b7cb5de25c8f7d15065ce905b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142331"
---
# <a name="rename-method-of-the-cim_devicefile-class"></a><span data-ttu-id="29570-103">Метод Rename класса CIM \_ девицефиле</span><span class="sxs-lookup"><span data-stu-id="29570-103">Rename method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="29570-104">Метод **Rename** переименовывает файл устройства (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="29570-104">The **Rename** method renames the device file (or directory) specified in the object path.</span></span> <span data-ttu-id="29570-105">Переименование не поддерживается, если место назначения находится на другом диске или требуется перезапись существующего логического файла.</span><span class="sxs-lookup"><span data-stu-id="29570-105">Renaming is not supported if the destination is on another drive or overwriting an existing logical file is required.</span></span> <span data-ttu-id="29570-106">Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="29570-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="29570-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="29570-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="29570-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="29570-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="29570-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="29570-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="29570-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="29570-110">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="29570-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29570-111">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="29570-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="29570-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29570-113">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="29570-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29570-114">Полное новое имя файла (или каталога).</span><span class="sxs-lookup"><span data-stu-id="29570-114">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="29570-115">Пример: "c: \\ temp \\newfile.txt"</span><span class="sxs-lookup"><span data-stu-id="29570-115">Example: "c:\\temp\\newfile.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29570-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="29570-116">Return value</span></span>

<span data-ttu-id="29570-117">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="29570-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="29570-118">**0**</span><span class="sxs-lookup"><span data-stu-id="29570-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="29570-119">Успешно.</span><span class="sxs-lookup"><span data-stu-id="29570-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="29570-120">**2**</span><span class="sxs-lookup"><span data-stu-id="29570-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="29570-121">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="29570-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="29570-122">**8**</span><span class="sxs-lookup"><span data-stu-id="29570-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="29570-123">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="29570-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="29570-124">**9**</span><span class="sxs-lookup"><span data-stu-id="29570-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="29570-125">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="29570-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="29570-126">**10**</span><span class="sxs-lookup"><span data-stu-id="29570-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="29570-127">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="29570-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="29570-128">**11**</span><span class="sxs-lookup"><span data-stu-id="29570-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="29570-129">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="29570-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="29570-130">**12**</span><span class="sxs-lookup"><span data-stu-id="29570-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="29570-131">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="29570-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="29570-132">**13**</span><span class="sxs-lookup"><span data-stu-id="29570-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="29570-133">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="29570-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="29570-134">**14**</span><span class="sxs-lookup"><span data-stu-id="29570-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="29570-135">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="29570-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="29570-136">**15**</span><span class="sxs-lookup"><span data-stu-id="29570-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="29570-137">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="29570-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="29570-138">**16**</span><span class="sxs-lookup"><span data-stu-id="29570-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="29570-139">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="29570-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="29570-140">**17**</span><span class="sxs-lookup"><span data-stu-id="29570-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="29570-141">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="29570-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="29570-142">**открыт**</span><span class="sxs-lookup"><span data-stu-id="29570-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="29570-143">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="29570-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29570-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29570-144">Remarks</span></span>

<span data-ttu-id="29570-145">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="29570-145">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="29570-146">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="29570-146">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="29570-147">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="29570-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="29570-148">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="29570-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="29570-149">Требования</span><span class="sxs-lookup"><span data-stu-id="29570-149">Requirements</span></span>



| <span data-ttu-id="29570-150">Требование</span><span class="sxs-lookup"><span data-stu-id="29570-150">Requirement</span></span> | <span data-ttu-id="29570-151">Значение</span><span class="sxs-lookup"><span data-stu-id="29570-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29570-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="29570-152">Minimum supported client</span></span><br/> | <span data-ttu-id="29570-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29570-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="29570-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="29570-154">Minimum supported server</span></span><br/> | <span data-ttu-id="29570-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29570-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="29570-156">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="29570-156">Namespace</span></span><br/>                | <span data-ttu-id="29570-157">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="29570-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="29570-158">MOF</span><span class="sxs-lookup"><span data-stu-id="29570-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29570-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29570-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="29570-160">DLL</span><span class="sxs-lookup"><span data-stu-id="29570-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29570-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29570-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29570-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29570-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29570-163">\_ДЕВИЦЕФИЛЕ CIM</span><span class="sxs-lookup"><span data-stu-id="29570-163">CIM\_DeviceFile</span></span>](rename-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="29570-164">**\_ДЕВИЦЕФИЛЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="29570-164">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

