---
description: Метод Компрессекс сжимает логический файл (или каталог), указанный в пути объекта. Этот метод является расширенной версией метода сжатия. Этот метод наследуется от CIM \_ LogicalFile.
ms.assetid: a5f7b35b-5d52-4129-bf7e-6db5e0ff6852
ms.tgt_platform: multiple
title: Метод Компрессекс класса CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e607497a8bb49d0a5926e5b50eb3310c671d9f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895482"
---
# <a name="compressex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="99c27-105">Метод Компрессекс \_ класса CIM девицефиле</span><span class="sxs-lookup"><span data-stu-id="99c27-105">CompressEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="99c27-106">Метод **компрессекс** сжимает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="99c27-106">The **CompressEx** method compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="99c27-107">Этот метод является расширенной версией метода [**сжатия**](compress-method-in-class-cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="99c27-107">This method is an extended version of the [**Compress**](compress-method-in-class-cim-devicefile.md) method.</span></span> <span data-ttu-id="99c27-108">Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="99c27-108">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="99c27-109">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="99c27-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="99c27-110">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="99c27-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="99c27-111">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="99c27-111">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="99c27-112">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="99c27-112">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="99c27-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99c27-113">Syntax</span></span>


```mof
uint32 CompressEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="99c27-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="99c27-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99c27-115">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="99c27-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99c27-116">Строка, представляющая имя файла (или каталога), в котором произошел сбой метода.</span><span class="sxs-lookup"><span data-stu-id="99c27-116">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="99c27-117">Если метод выполнен, этот параметр имеет **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="99c27-117">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="99c27-118">*StartFileName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="99c27-118">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c27-119">Строка, представляющая дочерний файл (или каталог), используемый в качестве отправной точки для этого метода.</span><span class="sxs-lookup"><span data-stu-id="99c27-119">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="99c27-120">Как правило, параметр *StartFileName* — это параметр *стопфиленаме* , указывающий файл (или каталог), в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="99c27-120">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="99c27-121">Если этот параметр имеет **значение NULL**, операция выполняется над файлом (или каталогом), указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="99c27-121">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="99c27-122">*Рекурсивно* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="99c27-122">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99c27-123">Если **значение — true**, метод также применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ девицефиле**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="99c27-123">If **TRUE**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="99c27-124">Для экземпляров файлов этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="99c27-124">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99c27-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="99c27-125">Return value</span></span>

<span data-ttu-id="99c27-126">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="99c27-126">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="99c27-127">0</span><span class="sxs-lookup"><span data-stu-id="99c27-127">0</span></span>

<span data-ttu-id="99c27-128">Успешно.</span><span class="sxs-lookup"><span data-stu-id="99c27-128">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99c27-129">2</span><span class="sxs-lookup"><span data-stu-id="99c27-129">2</span></span>

<span data-ttu-id="99c27-130">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="99c27-130">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99c27-131">8</span><span class="sxs-lookup"><span data-stu-id="99c27-131">8</span></span>

<span data-ttu-id="99c27-132">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="99c27-132">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99c27-133">9</span><span class="sxs-lookup"><span data-stu-id="99c27-133">9</span></span>

<span data-ttu-id="99c27-134">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="99c27-134">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99c27-135">10</span><span class="sxs-lookup"><span data-stu-id="99c27-135">10</span></span>

<span data-ttu-id="99c27-136">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="99c27-136">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99c27-137">11</span><span class="sxs-lookup"><span data-stu-id="99c27-137">11</span></span>

<span data-ttu-id="99c27-138">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="99c27-138">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99c27-139">12</span><span class="sxs-lookup"><span data-stu-id="99c27-139">12</span></span>

<span data-ttu-id="99c27-140">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="99c27-140">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99c27-141">13</span><span class="sxs-lookup"><span data-stu-id="99c27-141">13</span></span>

<span data-ttu-id="99c27-142">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="99c27-142">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99c27-143">14</span><span class="sxs-lookup"><span data-stu-id="99c27-143">14</span></span>

<span data-ttu-id="99c27-144">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="99c27-144">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99c27-145">15</span><span class="sxs-lookup"><span data-stu-id="99c27-145">15</span></span>

<span data-ttu-id="99c27-146">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="99c27-146">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99c27-147">16</span><span class="sxs-lookup"><span data-stu-id="99c27-147">16</span></span>

<span data-ttu-id="99c27-148">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="99c27-148">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99c27-149">17</span><span class="sxs-lookup"><span data-stu-id="99c27-149">17</span></span>

<span data-ttu-id="99c27-150">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="99c27-150">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="99c27-151">21</span><span class="sxs-lookup"><span data-stu-id="99c27-151">21</span></span>

<span data-ttu-id="99c27-152">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="99c27-152">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99c27-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99c27-153">Remarks</span></span>

<span data-ttu-id="99c27-154">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="99c27-154">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="99c27-155">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="99c27-155">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="99c27-156">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="99c27-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="99c27-157">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="99c27-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="99c27-158">Требования</span><span class="sxs-lookup"><span data-stu-id="99c27-158">Requirements</span></span>



| <span data-ttu-id="99c27-159">Требование</span><span class="sxs-lookup"><span data-stu-id="99c27-159">Requirement</span></span> | <span data-ttu-id="99c27-160">Значение</span><span class="sxs-lookup"><span data-stu-id="99c27-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99c27-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="99c27-161">Minimum supported client</span></span><br/> | <span data-ttu-id="99c27-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99c27-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="99c27-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="99c27-163">Minimum supported server</span></span><br/> | <span data-ttu-id="99c27-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99c27-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="99c27-165">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="99c27-165">Namespace</span></span><br/>                | <span data-ttu-id="99c27-166">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="99c27-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="99c27-167">MOF</span><span class="sxs-lookup"><span data-stu-id="99c27-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99c27-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="99c27-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="99c27-169">DLL</span><span class="sxs-lookup"><span data-stu-id="99c27-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99c27-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99c27-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99c27-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99c27-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99c27-172">\_ДЕВИЦЕФИЛЕ CIM</span><span class="sxs-lookup"><span data-stu-id="99c27-172">CIM\_DeviceFile</span></span>](compressex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="99c27-173">**\_ДЕВИЦЕФИЛЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="99c27-173">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

