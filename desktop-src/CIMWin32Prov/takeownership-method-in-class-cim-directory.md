---
description: Метод Такеовнершип получает владение логическим файлом, указанным в пути объекта.
ms.assetid: 053647d0-3ba0-4cd4-a84a-a1a96ef7151c
ms.tgt_platform: multiple
title: Метод Такеовнершип класса CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc68e974c98405f03c4bbfb45f02fdf78bf65127
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262773"
---
# <a name="takeownership-method-of-the-cim_directory-class"></a><span data-ttu-id="5ea83-103">Метод Такеовнершип \_ класса каталога CIM</span><span class="sxs-lookup"><span data-stu-id="5ea83-103">TakeOwnerShip method of the CIM\_Directory class</span></span>

<span data-ttu-id="5ea83-104">Метод **такеовнершип** получает владение логическим файлом, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="5ea83-104">The **TakeOwnerShip** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="5ea83-105">Если логический файл является каталогом, этот метод работает рекурсивно, принимая во внимание владение всеми файлами и подкаталогами, которые содержит каталог.</span><span class="sxs-lookup"><span data-stu-id="5ea83-105">If the logical file is a directory, this method acts recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span> <span data-ttu-id="5ea83-106">Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="5ea83-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5ea83-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="5ea83-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5ea83-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5ea83-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5ea83-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="5ea83-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5ea83-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5ea83-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5ea83-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ea83-111">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="5ea83-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ea83-112">Parameters</span></span>

<span data-ttu-id="5ea83-113">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="5ea83-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5ea83-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ea83-114">Return value</span></span>

<span data-ttu-id="5ea83-115">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="5ea83-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="5ea83-116">**0**</span><span class="sxs-lookup"><span data-stu-id="5ea83-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="5ea83-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="5ea83-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="5ea83-118">**2**</span><span class="sxs-lookup"><span data-stu-id="5ea83-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="5ea83-119">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="5ea83-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="5ea83-120">**8**</span><span class="sxs-lookup"><span data-stu-id="5ea83-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="5ea83-121">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="5ea83-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="5ea83-122">**9**</span><span class="sxs-lookup"><span data-stu-id="5ea83-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="5ea83-123">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="5ea83-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="5ea83-124">**10**</span><span class="sxs-lookup"><span data-stu-id="5ea83-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="5ea83-125">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="5ea83-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5ea83-126">**11**</span><span class="sxs-lookup"><span data-stu-id="5ea83-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="5ea83-127">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="5ea83-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="5ea83-128">**12**</span><span class="sxs-lookup"><span data-stu-id="5ea83-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="5ea83-129">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="5ea83-129">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="5ea83-130">**13**</span><span class="sxs-lookup"><span data-stu-id="5ea83-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="5ea83-131">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="5ea83-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="5ea83-132">**14**</span><span class="sxs-lookup"><span data-stu-id="5ea83-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="5ea83-133">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="5ea83-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="5ea83-134">**15**</span><span class="sxs-lookup"><span data-stu-id="5ea83-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="5ea83-135">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="5ea83-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="5ea83-136">**16**</span><span class="sxs-lookup"><span data-stu-id="5ea83-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="5ea83-137">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="5ea83-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="5ea83-138">**17**</span><span class="sxs-lookup"><span data-stu-id="5ea83-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="5ea83-139">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="5ea83-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="5ea83-140">**открыт**</span><span class="sxs-lookup"><span data-stu-id="5ea83-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="5ea83-141">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="5ea83-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ea83-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ea83-142">Remarks</span></span>

<span data-ttu-id="5ea83-143">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="5ea83-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="5ea83-144">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="5ea83-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="5ea83-145">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="5ea83-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5ea83-146">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="5ea83-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="examples"></a><span data-ttu-id="5ea83-147">Примеры</span><span class="sxs-lookup"><span data-stu-id="5ea83-147">Examples</span></span>

<span data-ttu-id="5ea83-148">Следующий код скрипта Visual Basic вызывает метод **такеовнершип** , чтобы стать владельцем папки C: \\ TEMP.</span><span class="sxs-lookup"><span data-stu-id="5ea83-148">The following Visual Basic Script code calls the **TakeOwnerShip** method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 

Set objWMIService = _
    GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 

' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\\temp'", "TakeOwnerShip")

wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="5ea83-149">Требования</span><span class="sxs-lookup"><span data-stu-id="5ea83-149">Requirements</span></span>



| <span data-ttu-id="5ea83-150">Требование</span><span class="sxs-lookup"><span data-stu-id="5ea83-150">Requirement</span></span> | <span data-ttu-id="5ea83-151">Значение</span><span class="sxs-lookup"><span data-stu-id="5ea83-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea83-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ea83-152">Minimum supported client</span></span><br/> | <span data-ttu-id="5ea83-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ea83-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5ea83-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ea83-154">Minimum supported server</span></span><br/> | <span data-ttu-id="5ea83-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ea83-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5ea83-156">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5ea83-156">Namespace</span></span><br/>                | <span data-ttu-id="5ea83-157">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5ea83-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5ea83-158">MOF</span><span class="sxs-lookup"><span data-stu-id="5ea83-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ea83-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ea83-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ea83-160">DLL</span><span class="sxs-lookup"><span data-stu-id="5ea83-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ea83-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ea83-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ea83-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ea83-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ea83-163">\_Каталог CIM</span><span class="sxs-lookup"><span data-stu-id="5ea83-163">CIM\_Directory</span></span>](takeownership-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="5ea83-164">**\_Каталог CIM**</span><span class="sxs-lookup"><span data-stu-id="5ea83-164">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

