---
description: Получает владение файлом записи логического каталога, указанным в пути объекта. Этот метод является расширенной версией метода Такеовнершип и наследуется от CIM \_ LogicalFile.
ms.assetid: a13acaa2-2203-470a-b989-15f8276e46c6
ms.tgt_platform: multiple
title: Метод Такеовнершипекс класса CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b02a6c40e99405c150a372f8eb15fe648f2df60a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140987"
---
# <a name="takeownershipex-method-of-the-cim_directory-class"></a><span data-ttu-id="8fa6c-104">Метод Такеовнершипекс \_ класса каталога CIM</span><span class="sxs-lookup"><span data-stu-id="8fa6c-104">TakeOwnerShipEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="8fa6c-105">Метод **такеовнершипекс** получает владение файлом записи логического каталога, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-105">The **TakeOwnerShipEx** method obtains ownership of the logical directory entry file specified in the object path.</span></span> <span data-ttu-id="8fa6c-106">Этот метод является расширенной версией метода [**такеовнершип**](takeownership-method-in-class-cim-directory.md) и наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="8fa6c-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="8fa6c-107">Если логический файл является каталогом, этот метод работает рекурсивно, принимая во внимание владение всеми файлами и подкаталогами, которые содержит каталог.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-107">If the logical file is a directory, then this method acts recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8fa6c-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8fa6c-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8fa6c-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8fa6c-110">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="8fa6c-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8fa6c-111">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8fa6c-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8fa6c-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fa6c-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="8fa6c-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="8fa6c-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fa6c-114">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8fa6c-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fa6c-115">Строка, представляющая имя файла (или каталога), в котором произошел сбой метода.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="8fa6c-116">Если метод выполнен, этот параметр имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-116">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="8fa6c-117">*StartFileName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8fa6c-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fa6c-118">Строка, представляющая дочерний файл (или каталог), используемый в качестве отправной точки для этого метода.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-118">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="8fa6c-119">Как правило, этот параметр представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-119">Typically, this parameter is the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="8fa6c-120">Если этот параметр имеет значение null, операция выполняется над файлом (или каталогом), указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="8fa6c-120">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="8fa6c-121">*Рекурсивно* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8fa6c-121">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fa6c-122">Если **значение — true**, метод применяется рекурсивно к файлам и каталогам в каталоге, указанном экземпляром [**\_ каталога CIM**](cim-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="8fa6c-122">If **True**, the method is applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="8fa6c-123">Для экземпляров файлов этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fa6c-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8fa6c-124">Return value</span></span>

<span data-ttu-id="8fa6c-125">Возвращает значение 0 в случае успешного выполнения и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-125">Returns a value of 0 on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="8fa6c-126">0</span><span class="sxs-lookup"><span data-stu-id="8fa6c-126">0</span></span>

<span data-ttu-id="8fa6c-127">Успешно.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-127">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8fa6c-128">2</span><span class="sxs-lookup"><span data-stu-id="8fa6c-128">2</span></span>

<span data-ttu-id="8fa6c-129">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-129">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8fa6c-130">8</span><span class="sxs-lookup"><span data-stu-id="8fa6c-130">8</span></span>

<span data-ttu-id="8fa6c-131">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-131">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8fa6c-132">9</span><span class="sxs-lookup"><span data-stu-id="8fa6c-132">9</span></span>

<span data-ttu-id="8fa6c-133">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-133">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8fa6c-134">10</span><span class="sxs-lookup"><span data-stu-id="8fa6c-134">10</span></span>

<span data-ttu-id="8fa6c-135">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-135">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8fa6c-136">11</span><span class="sxs-lookup"><span data-stu-id="8fa6c-136">11</span></span>

<span data-ttu-id="8fa6c-137">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-137">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8fa6c-138">12</span><span class="sxs-lookup"><span data-stu-id="8fa6c-138">12</span></span>

<span data-ttu-id="8fa6c-139">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-139">The platform is not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8fa6c-140">13</span><span class="sxs-lookup"><span data-stu-id="8fa6c-140">13</span></span>

<span data-ttu-id="8fa6c-141">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-141">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8fa6c-142">14</span><span class="sxs-lookup"><span data-stu-id="8fa6c-142">14</span></span>

<span data-ttu-id="8fa6c-143">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-143">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8fa6c-144">15</span><span class="sxs-lookup"><span data-stu-id="8fa6c-144">15</span></span>

<span data-ttu-id="8fa6c-145">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-145">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8fa6c-146">16</span><span class="sxs-lookup"><span data-stu-id="8fa6c-146">16</span></span>

<span data-ttu-id="8fa6c-147">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-147">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8fa6c-148">17</span><span class="sxs-lookup"><span data-stu-id="8fa6c-148">17</span></span>

<span data-ttu-id="8fa6c-149">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-149">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="8fa6c-150">21</span><span class="sxs-lookup"><span data-stu-id="8fa6c-150">21</span></span>

<span data-ttu-id="8fa6c-151">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-151">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8fa6c-152">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8fa6c-152">Remarks</span></span>

<span data-ttu-id="8fa6c-153">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-153">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="8fa6c-154">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-154">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="8fa6c-155">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-155">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8fa6c-156">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-156">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="examples"></a><span data-ttu-id="8fa6c-157">Примеры</span><span class="sxs-lookup"><span data-stu-id="8fa6c-157">Examples</span></span>

<span data-ttu-id="8fa6c-158">Следующий код скрипта Visual Basic вызывает метод **такеовнершипекс** , чтобы стать владельцем папки C: \\ TEMP.</span><span class="sxs-lookup"><span data-stu-id="8fa6c-158">The following Visual Basic Script code calls the **TakeOwnerShipEx** method to take ownership of the C:\\temp folder.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx"). _
    inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
wscript.echo objOutParams.ReturnValue
```



## <a name="requirements"></a><span data-ttu-id="8fa6c-159">Требования</span><span class="sxs-lookup"><span data-stu-id="8fa6c-159">Requirements</span></span>



| <span data-ttu-id="8fa6c-160">Требование</span><span class="sxs-lookup"><span data-stu-id="8fa6c-160">Requirement</span></span> | <span data-ttu-id="8fa6c-161">Значение</span><span class="sxs-lookup"><span data-stu-id="8fa6c-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fa6c-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8fa6c-162">Minimum supported client</span></span><br/> | <span data-ttu-id="8fa6c-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8fa6c-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8fa6c-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8fa6c-164">Minimum supported server</span></span><br/> | <span data-ttu-id="8fa6c-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fa6c-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8fa6c-166">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8fa6c-166">Namespace</span></span><br/>                | <span data-ttu-id="8fa6c-167">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8fa6c-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8fa6c-168">MOF</span><span class="sxs-lookup"><span data-stu-id="8fa6c-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fa6c-169"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fa6c-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8fa6c-170">DLL</span><span class="sxs-lookup"><span data-stu-id="8fa6c-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fa6c-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fa6c-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fa6c-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8fa6c-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fa6c-173">\_Каталог CIM</span><span class="sxs-lookup"><span data-stu-id="8fa6c-173">CIM\_Directory</span></span>](takeownershipex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="8fa6c-174">**\_Каталог CIM**</span><span class="sxs-lookup"><span data-stu-id="8fa6c-174">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

