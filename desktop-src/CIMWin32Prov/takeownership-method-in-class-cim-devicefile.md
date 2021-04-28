---
description: Метод Такеовнершип класса CIM_DeviceFile — метод Такеовнершип получает владение логическим файлом, указанным в пути объекта.
ms.assetid: ef7d5ce7-99fb-464f-9739-ec9189148f94
ms.tgt_platform: multiple
title: Метод Такеовнершип класса CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e7c745df18e1725199c4027d22882a00f6143a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086052"
---
# <a name="takeownership-method-of-the-cim_devicefile-class"></a><span data-ttu-id="120bd-103">Метод Такеовнершип \_ класса CIM девицефиле</span><span class="sxs-lookup"><span data-stu-id="120bd-103">TakeOwnerShip method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="120bd-104">Метод **такеовнершип** получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="120bd-104">The **TakeOwnerShip** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="120bd-105">Если логический файл является каталогом, этот метод будет выполняться рекурсивно, при этом становится владельцем всех файлов и подкаталогов, содержащихся в каталоге.</span><span class="sxs-lookup"><span data-stu-id="120bd-105">If the logical file is a directory, then this method will act recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="120bd-106">Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="120bd-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="120bd-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="120bd-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="120bd-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="120bd-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="120bd-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="120bd-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="120bd-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="120bd-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="120bd-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="120bd-111">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="120bd-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="120bd-112">Parameters</span></span>

<span data-ttu-id="120bd-113">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="120bd-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="120bd-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="120bd-114">Return value</span></span>

<span data-ttu-id="120bd-115">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="120bd-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="120bd-116">**0**</span><span class="sxs-lookup"><span data-stu-id="120bd-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="120bd-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="120bd-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="120bd-118">**2**</span><span class="sxs-lookup"><span data-stu-id="120bd-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="120bd-119">Access denied. (Недопустимое значение {значение_утверждения} для утверждения {имя_утверждения}. Доступ запрещен.)</span><span class="sxs-lookup"><span data-stu-id="120bd-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="120bd-120">**8**</span><span class="sxs-lookup"><span data-stu-id="120bd-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="120bd-121">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="120bd-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="120bd-122">**9**</span><span class="sxs-lookup"><span data-stu-id="120bd-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="120bd-123">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="120bd-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="120bd-124">**10**</span><span class="sxs-lookup"><span data-stu-id="120bd-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="120bd-125">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="120bd-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="120bd-126">**11**</span><span class="sxs-lookup"><span data-stu-id="120bd-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="120bd-127">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="120bd-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="120bd-128">**12**</span><span class="sxs-lookup"><span data-stu-id="120bd-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="120bd-129">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="120bd-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="120bd-130">**13**</span><span class="sxs-lookup"><span data-stu-id="120bd-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="120bd-131">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="120bd-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="120bd-132">**14**</span><span class="sxs-lookup"><span data-stu-id="120bd-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="120bd-133">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="120bd-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="120bd-134">**15**</span><span class="sxs-lookup"><span data-stu-id="120bd-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="120bd-135">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="120bd-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="120bd-136">**16**</span><span class="sxs-lookup"><span data-stu-id="120bd-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="120bd-137">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="120bd-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="120bd-138">**17**</span><span class="sxs-lookup"><span data-stu-id="120bd-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="120bd-139">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="120bd-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="120bd-140">**открыт**</span><span class="sxs-lookup"><span data-stu-id="120bd-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="120bd-141">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="120bd-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="120bd-142">Remarks</span><span class="sxs-lookup"><span data-stu-id="120bd-142">Remarks</span></span>

<span data-ttu-id="120bd-143">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="120bd-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="120bd-144">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="120bd-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="120bd-145">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="120bd-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="120bd-146">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="120bd-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="120bd-147">Требования</span><span class="sxs-lookup"><span data-stu-id="120bd-147">Requirements</span></span>



| <span data-ttu-id="120bd-148">Требование</span><span class="sxs-lookup"><span data-stu-id="120bd-148">Requirement</span></span> | <span data-ttu-id="120bd-149">Значение</span><span class="sxs-lookup"><span data-stu-id="120bd-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="120bd-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="120bd-150">Minimum supported client</span></span><br/> | <span data-ttu-id="120bd-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="120bd-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="120bd-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="120bd-152">Minimum supported server</span></span><br/> | <span data-ttu-id="120bd-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="120bd-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="120bd-154">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="120bd-154">Namespace</span></span><br/>                | <span data-ttu-id="120bd-155">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="120bd-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="120bd-156">MOF</span><span class="sxs-lookup"><span data-stu-id="120bd-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="120bd-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="120bd-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="120bd-158">DLL</span><span class="sxs-lookup"><span data-stu-id="120bd-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="120bd-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="120bd-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="120bd-160">См. также</span><span class="sxs-lookup"><span data-stu-id="120bd-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="120bd-161">\_ДЕВИЦЕФИЛЕ CIM</span><span class="sxs-lookup"><span data-stu-id="120bd-161">CIM\_DeviceFile</span></span>](takeownership-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="120bd-162">**\_ДЕВИЦЕФИЛЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="120bd-162">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

