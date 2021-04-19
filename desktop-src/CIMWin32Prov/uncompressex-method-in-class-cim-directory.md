---
description: Распаковывает логический файл записи каталога (или каталог), указанный в пути к объекту. Этот метод является расширенной версией метода uncompressия и наследуется от CIM \_ LogicalFile.
ms.assetid: ef5b7c90-5013-4ec0-bfa6-c32428ffb501
ms.tgt_platform: multiple
title: Метод Ункомпрессекс класса CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9af74132ceeb67e48d39c22bd0172954f26707f1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539245"
---
# <a name="uncompressex-method-of-the-cim_directory-class"></a><span data-ttu-id="65872-104">Метод Ункомпрессекс \_ класса каталога CIM</span><span class="sxs-lookup"><span data-stu-id="65872-104">UncompressEx method of the CIM\_Directory class</span></span>

<span data-ttu-id="65872-105">Метод **ункомпрессекс** распаковывает логический файл записи каталога (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="65872-105">The **UncompressEx** method uncompresses the logical directory entry file (or directory) specified in the object path.</span></span> <span data-ttu-id="65872-106">Этот метод является расширенной версией метода [**uncompressия**](uncompress-method-in-class-cim-directory.md) и наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="65872-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-cim-directory.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65872-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="65872-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="65872-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="65872-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="65872-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="65872-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="65872-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="65872-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="65872-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="65872-111">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="65872-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="65872-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65872-113">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="65872-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65872-114">Строка, представляющая имя файла (или каталога), в котором произошел сбой метода.</span><span class="sxs-lookup"><span data-stu-id="65872-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="65872-115">Если метод выполнен, этот параметр имеет **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="65872-115">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="65872-116">*StartFileName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="65872-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65872-117">Строка, представляющая дочерний файл (или каталог), используемый в качестве отправной точки для этого метода.</span><span class="sxs-lookup"><span data-stu-id="65872-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="65872-118">Как правило, этот параметр представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="65872-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="65872-119">Если этот параметр имеет **значение NULL**, операция выполняется над файлом или каталогом, указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="65872-119">If this parameter is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="65872-120">*Рекурсивно* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="65872-120">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65872-121">Если **значение — true**, метод применяется рекурсивно к файлам и каталогам в каталоге, указанном экземпляром [**\_ каталога CIM**](cim-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="65872-121">If **TRUE**, the method is applied recursively to files and directories within the directory specified by the [**CIM\_Directory**](cim-directory.md) instance.</span></span> <span data-ttu-id="65872-122">Для экземпляров файлов этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="65872-122">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65872-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65872-123">Return value</span></span>

<span data-ttu-id="65872-124">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="65872-124">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="65872-125">0</span><span class="sxs-lookup"><span data-stu-id="65872-125">0</span></span>

<span data-ttu-id="65872-126">Успешно.</span><span class="sxs-lookup"><span data-stu-id="65872-126">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="65872-127">2</span><span class="sxs-lookup"><span data-stu-id="65872-127">2</span></span>

<span data-ttu-id="65872-128">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="65872-128">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="65872-129">8</span><span class="sxs-lookup"><span data-stu-id="65872-129">8</span></span>

<span data-ttu-id="65872-130">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="65872-130">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="65872-131">9</span><span class="sxs-lookup"><span data-stu-id="65872-131">9</span></span>

<span data-ttu-id="65872-132">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="65872-132">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="65872-133">10</span><span class="sxs-lookup"><span data-stu-id="65872-133">10</span></span>

<span data-ttu-id="65872-134">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="65872-134">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="65872-135">11</span><span class="sxs-lookup"><span data-stu-id="65872-135">11</span></span>

<span data-ttu-id="65872-136">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="65872-136">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="65872-137">12</span><span class="sxs-lookup"><span data-stu-id="65872-137">12</span></span>

<span data-ttu-id="65872-138">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="65872-138">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="65872-139">13</span><span class="sxs-lookup"><span data-stu-id="65872-139">13</span></span>

<span data-ttu-id="65872-140">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="65872-140">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="65872-141">14</span><span class="sxs-lookup"><span data-stu-id="65872-141">14</span></span>

<span data-ttu-id="65872-142">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="65872-142">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="65872-143">15</span><span class="sxs-lookup"><span data-stu-id="65872-143">15</span></span>

<span data-ttu-id="65872-144">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="65872-144">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="65872-145">16</span><span class="sxs-lookup"><span data-stu-id="65872-145">16</span></span>

<span data-ttu-id="65872-146">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="65872-146">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="65872-147">17</span><span class="sxs-lookup"><span data-stu-id="65872-147">17</span></span>

<span data-ttu-id="65872-148">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="65872-148">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="65872-149">21</span><span class="sxs-lookup"><span data-stu-id="65872-149">21</span></span>

<span data-ttu-id="65872-150">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="65872-150">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65872-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65872-151">Remarks</span></span>

<span data-ttu-id="65872-152">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="65872-152">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="65872-153">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="65872-153">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="65872-154">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="65872-154">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="65872-155">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="65872-155">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="65872-156">Требования</span><span class="sxs-lookup"><span data-stu-id="65872-156">Requirements</span></span>



| <span data-ttu-id="65872-157">Требование</span><span class="sxs-lookup"><span data-stu-id="65872-157">Requirement</span></span> | <span data-ttu-id="65872-158">Значение</span><span class="sxs-lookup"><span data-stu-id="65872-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65872-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65872-159">Minimum supported client</span></span><br/> | <span data-ttu-id="65872-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65872-160">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="65872-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65872-161">Minimum supported server</span></span><br/> | <span data-ttu-id="65872-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65872-162">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="65872-163">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="65872-163">Namespace</span></span><br/>                | <span data-ttu-id="65872-164">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="65872-164">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="65872-165">MOF</span><span class="sxs-lookup"><span data-stu-id="65872-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65872-166"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65872-166"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="65872-167">DLL</span><span class="sxs-lookup"><span data-stu-id="65872-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65872-168"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65872-168"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65872-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65872-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65872-170">**\_Каталог CIM**</span><span class="sxs-lookup"><span data-stu-id="65872-170">**CIM\_Directory**</span></span>](uncompressex-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="65872-171">**\_Каталог CIM**</span><span class="sxs-lookup"><span data-stu-id="65872-171">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

