---
description: Метод Копекс копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное параметром FileName. Этот метод является расширенной версией метода Copy и наследуется от CIM \_ LogicalFile.
ms.assetid: e207cc80-055e-41bc-ab80-dc50131b544d
ms.tgt_platform: multiple
title: Метод Копекс класса CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d7502c46c616d9b8e1fffeebf5aefcd022dd4cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990423"
---
# <a name="copyex-method-of-the-cim_directory-class"></a><span data-ttu-id="b0131-104">Метод Копекс \_ класса каталога CIM</span><span class="sxs-lookup"><span data-stu-id="b0131-104">CopyEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="b0131-105">Метод **копекс** копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное параметром *filename* .</span><span class="sxs-lookup"><span data-stu-id="b0131-105">The **CopyEx** method copies the logical file (or directory) specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="b0131-106">Этот метод является расширенной версией метода [**Copy**](copy-method-in-class-cim-directory.md) и наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b0131-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b0131-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="b0131-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b0131-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b0131-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b0131-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="b0131-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b0131-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b0131-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b0131-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0131-111">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]  string REF FileName,
  [out] string     StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="b0131-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0131-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0131-113">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0131-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0131-114">Полное имя копии целевого файла (или каталога).</span><span class="sxs-lookup"><span data-stu-id="b0131-114">Fully qualified name of the copy of the destination file (or directory).</span></span>

<span data-ttu-id="b0131-115">Пример: "c: \\ temp \\ невдиректори"</span><span class="sxs-lookup"><span data-stu-id="b0131-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="b0131-116">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b0131-116">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0131-117">Строка, представляющая имя файла (или каталога), в котором произошел сбой метода.</span><span class="sxs-lookup"><span data-stu-id="b0131-117">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="b0131-118">Если метод выполнен, этот параметр имеет **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="b0131-118">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="b0131-119">*StartFileName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0131-119">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0131-120">Строка, представляющая дочерний файл (или каталог), используемый в качестве отправной точки для этого метода.</span><span class="sxs-lookup"><span data-stu-id="b0131-120">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="b0131-121">Как правило, этот параметр представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="b0131-121">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="b0131-122">Если этот параметр имеет **значение NULL**, операция выполняется над файлом (или каталогом), указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="b0131-122">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="b0131-123">*Рекурсивно* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b0131-123">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0131-124">Если значение — TRUE, метод также применяется рекурсивно к файлам и каталогам в каталоге, указанном экземпляром [**\_ каталога CIM**](cim-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="b0131-124">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="b0131-125">Для экземпляров файлов этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b0131-125">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0131-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0131-126">Return value</span></span>

<span data-ttu-id="b0131-127">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="b0131-127">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="b0131-128">0</span><span class="sxs-lookup"><span data-stu-id="b0131-128">0</span></span>

<span data-ttu-id="b0131-129">Успешно.</span><span class="sxs-lookup"><span data-stu-id="b0131-129">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b0131-130">2</span><span class="sxs-lookup"><span data-stu-id="b0131-130">2</span></span>

<span data-ttu-id="b0131-131">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="b0131-131">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b0131-132">8</span><span class="sxs-lookup"><span data-stu-id="b0131-132">8</span></span>

<span data-ttu-id="b0131-133">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="b0131-133">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b0131-134">9</span><span class="sxs-lookup"><span data-stu-id="b0131-134">9</span></span>

<span data-ttu-id="b0131-135">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="b0131-135">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b0131-136">10</span><span class="sxs-lookup"><span data-stu-id="b0131-136">10</span></span>

<span data-ttu-id="b0131-137">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="b0131-137">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b0131-138">11</span><span class="sxs-lookup"><span data-stu-id="b0131-138">11</span></span>

<span data-ttu-id="b0131-139">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="b0131-139">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b0131-140">12</span><span class="sxs-lookup"><span data-stu-id="b0131-140">12</span></span>

<span data-ttu-id="b0131-141">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="b0131-141">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b0131-142">13</span><span class="sxs-lookup"><span data-stu-id="b0131-142">13</span></span>

<span data-ttu-id="b0131-143">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="b0131-143">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b0131-144">14</span><span class="sxs-lookup"><span data-stu-id="b0131-144">14</span></span>

<span data-ttu-id="b0131-145">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="b0131-145">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b0131-146">15</span><span class="sxs-lookup"><span data-stu-id="b0131-146">15</span></span>

<span data-ttu-id="b0131-147">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="b0131-147">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b0131-148">16</span><span class="sxs-lookup"><span data-stu-id="b0131-148">16</span></span>

<span data-ttu-id="b0131-149">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="b0131-149">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b0131-150">17</span><span class="sxs-lookup"><span data-stu-id="b0131-150">17</span></span>

<span data-ttu-id="b0131-151">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="b0131-151">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b0131-152">21</span><span class="sxs-lookup"><span data-stu-id="b0131-152">21</span></span>

<span data-ttu-id="b0131-153">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="b0131-153">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0131-154">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0131-154">Remarks</span></span>

<span data-ttu-id="b0131-155">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="b0131-155">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="b0131-156">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="b0131-156">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="b0131-157">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="b0131-157">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b0131-158">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="b0131-158">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0131-159">Требования</span><span class="sxs-lookup"><span data-stu-id="b0131-159">Requirements</span></span>



| <span data-ttu-id="b0131-160">Требование</span><span class="sxs-lookup"><span data-stu-id="b0131-160">Requirement</span></span> | <span data-ttu-id="b0131-161">Значение</span><span class="sxs-lookup"><span data-stu-id="b0131-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0131-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0131-162">Minimum supported client</span></span><br/> | <span data-ttu-id="b0131-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0131-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b0131-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0131-164">Minimum supported server</span></span><br/> | <span data-ttu-id="b0131-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0131-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b0131-166">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b0131-166">Namespace</span></span><br/>                | <span data-ttu-id="b0131-167">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b0131-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b0131-168">MOF</span><span class="sxs-lookup"><span data-stu-id="b0131-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0131-169"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0131-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0131-170">DLL</span><span class="sxs-lookup"><span data-stu-id="b0131-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0131-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0131-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0131-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0131-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0131-173">\_Каталог CIM</span><span class="sxs-lookup"><span data-stu-id="b0131-173">CIM\_Directory</span></span>](copyex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="b0131-174">**\_Каталог CIM**</span><span class="sxs-lookup"><span data-stu-id="b0131-174">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

