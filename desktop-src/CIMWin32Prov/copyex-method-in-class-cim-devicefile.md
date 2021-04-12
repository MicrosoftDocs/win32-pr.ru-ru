---
description: Копирует файл логического устройства (или каталог), указанный в пути к объекту, в расположение, указанное параметром FileName.
ms.assetid: 42cdb880-2431-4dcc-abdb-f271e2cd81a4
ms.tgt_platform: multiple
title: Метод Копекс класса CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0e9519155accadc1a41a1c91492755db90eec696
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423365"
---
# <a name="copyex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="89fb6-103">Метод Копекс \_ класса CIM девицефиле</span><span class="sxs-lookup"><span data-stu-id="89fb6-103">CopyEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="89fb6-104">Метод **копекс** копирует файл логического устройства (или каталог), указанный в пути к объекту, в расположение, указанное параметром *filename* .</span><span class="sxs-lookup"><span data-stu-id="89fb6-104">The **CopyEx** method copies the logical device file (or directory) specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="89fb6-105">Копирование не поддерживается, если требуется перезапись существующего логического файла.</span><span class="sxs-lookup"><span data-stu-id="89fb6-105">A copy is not supported if overwriting an existing logical file is required.</span></span> <span data-ttu-id="89fb6-106">Этот метод является расширенной версией метода [**Copy**](copy-method-in-class-cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="89fb6-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-devicefile.md) method.</span></span> <span data-ttu-id="89fb6-107">Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="89fb6-107">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="89fb6-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="89fb6-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="89fb6-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="89fb6-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="89fb6-110">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="89fb6-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="89fb6-111">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="89fb6-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="89fb6-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89fb6-112">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]  string     FileName,
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="89fb6-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="89fb6-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89fb6-114">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="89fb6-114">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89fb6-115">Полное имя целевого файла (или каталога).</span><span class="sxs-lookup"><span data-stu-id="89fb6-115">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="89fb6-116">Пример: "c: \\ temp \\ невдиректори"</span><span class="sxs-lookup"><span data-stu-id="89fb6-116">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="89fb6-117">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="89fb6-117">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89fb6-118">Строка, представляющая имя файла (или каталога), в котором произошел сбой метода.</span><span class="sxs-lookup"><span data-stu-id="89fb6-118">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="89fb6-119">Если метод выполнен, этот параметр имеет **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="89fb6-119">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="89fb6-120">*StartFileName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="89fb6-120">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89fb6-121">Строка, представляющая дочерний файл (или каталог), используемый в качестве отправной точки для этого метода.</span><span class="sxs-lookup"><span data-stu-id="89fb6-121">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="89fb6-122">Как правило, параметр *StartFileName* — это параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="89fb6-122">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="89fb6-123">Если этот параметр имеет **значение NULL**, операция выполняется над файлом (или каталогом), указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="89fb6-123">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="89fb6-124">*Рекурсивно* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="89fb6-124">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89fb6-125">Если значение — TRUE, метод также применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ девицефиле**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="89fb6-125">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="89fb6-126">Для экземпляров файлов этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="89fb6-126">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89fb6-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89fb6-127">Return value</span></span>

<span data-ttu-id="89fb6-128">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="89fb6-128">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="89fb6-129">0</span><span class="sxs-lookup"><span data-stu-id="89fb6-129">0</span></span>

<span data-ttu-id="89fb6-130">Успешно.</span><span class="sxs-lookup"><span data-stu-id="89fb6-130">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="89fb6-131">2</span><span class="sxs-lookup"><span data-stu-id="89fb6-131">2</span></span>

<span data-ttu-id="89fb6-132">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="89fb6-132">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="89fb6-133">8</span><span class="sxs-lookup"><span data-stu-id="89fb6-133">8</span></span>

<span data-ttu-id="89fb6-134">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="89fb6-134">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="89fb6-135">9</span><span class="sxs-lookup"><span data-stu-id="89fb6-135">9</span></span>

<span data-ttu-id="89fb6-136">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="89fb6-136">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="89fb6-137">10</span><span class="sxs-lookup"><span data-stu-id="89fb6-137">10</span></span>

<span data-ttu-id="89fb6-138">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="89fb6-138">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="89fb6-139">11</span><span class="sxs-lookup"><span data-stu-id="89fb6-139">11</span></span>

<span data-ttu-id="89fb6-140">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="89fb6-140">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="89fb6-141">12</span><span class="sxs-lookup"><span data-stu-id="89fb6-141">12</span></span>

<span data-ttu-id="89fb6-142">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="89fb6-142">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="89fb6-143">13</span><span class="sxs-lookup"><span data-stu-id="89fb6-143">13</span></span>

<span data-ttu-id="89fb6-144">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="89fb6-144">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="89fb6-145">14</span><span class="sxs-lookup"><span data-stu-id="89fb6-145">14</span></span>

<span data-ttu-id="89fb6-146">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="89fb6-146">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="89fb6-147">15</span><span class="sxs-lookup"><span data-stu-id="89fb6-147">15</span></span>

<span data-ttu-id="89fb6-148">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="89fb6-148">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="89fb6-149">16</span><span class="sxs-lookup"><span data-stu-id="89fb6-149">16</span></span>

<span data-ttu-id="89fb6-150">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="89fb6-150">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="89fb6-151">17</span><span class="sxs-lookup"><span data-stu-id="89fb6-151">17</span></span>

<span data-ttu-id="89fb6-152">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="89fb6-152">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="89fb6-153">21</span><span class="sxs-lookup"><span data-stu-id="89fb6-153">21</span></span>

<span data-ttu-id="89fb6-154">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="89fb6-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89fb6-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89fb6-155">Remarks</span></span>

<span data-ttu-id="89fb6-156">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="89fb6-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="89fb6-157">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="89fb6-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="89fb6-158">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="89fb6-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="89fb6-159">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="89fb6-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="89fb6-160">Требования</span><span class="sxs-lookup"><span data-stu-id="89fb6-160">Requirements</span></span>



| <span data-ttu-id="89fb6-161">Требование</span><span class="sxs-lookup"><span data-stu-id="89fb6-161">Requirement</span></span> | <span data-ttu-id="89fb6-162">Значение</span><span class="sxs-lookup"><span data-stu-id="89fb6-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89fb6-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89fb6-163">Minimum supported client</span></span><br/> | <span data-ttu-id="89fb6-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89fb6-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89fb6-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89fb6-165">Minimum supported server</span></span><br/> | <span data-ttu-id="89fb6-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89fb6-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89fb6-167">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="89fb6-167">Namespace</span></span><br/>                | <span data-ttu-id="89fb6-168">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="89fb6-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="89fb6-169">MOF</span><span class="sxs-lookup"><span data-stu-id="89fb6-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89fb6-170"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89fb6-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="89fb6-171">DLL</span><span class="sxs-lookup"><span data-stu-id="89fb6-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89fb6-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89fb6-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89fb6-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89fb6-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89fb6-174">\_ДЕВИЦЕФИЛЕ CIM</span><span class="sxs-lookup"><span data-stu-id="89fb6-174">CIM\_DeviceFile</span></span>](copyex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="89fb6-175">**\_ДЕВИЦЕФИЛЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="89fb6-175">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

