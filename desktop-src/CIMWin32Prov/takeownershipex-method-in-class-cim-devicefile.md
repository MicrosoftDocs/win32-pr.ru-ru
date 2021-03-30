---
description: Получает владение файлом логического устройства, указанным в пути объекта. Этот метод является расширенной версией метода Такеовнершип и наследуется от CIM \_ LogicalFile.
ms.assetid: 084f755a-e837-4d21-8bd2-0f63f80302fc
ms.tgt_platform: multiple
title: Метод Такеовнершипекс класса CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3c36239d7d0ea6b0bf3bfa67bfb2f59617ab209a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895398"
---
# <a name="takeownershipex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="29d98-104">Метод Такеовнершипекс \_ класса CIM девицефиле</span><span class="sxs-lookup"><span data-stu-id="29d98-104">TakeOwnerShipEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="29d98-105">Метод **такеовнершипекс** получает владение файлом логического устройства, указанным в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="29d98-105">The **TakeOwnerShipEx** method obtains ownership of the logical device file specified in the object path.</span></span> <span data-ttu-id="29d98-106">Этот метод является расширенной версией метода [**такеовнершип**](takeownership-method-in-class-cim-devicefile.md) и наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="29d98-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-cim-devicefile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="29d98-107">Если логический файл является каталогом, этот метод работает рекурсивно, принимая во внимание владение всеми файлами и подкаталогами, которые содержит каталог.</span><span class="sxs-lookup"><span data-stu-id="29d98-107">If the logical file is a directory, then this method acts recursively, taking ownership of all of the files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="29d98-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="29d98-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="29d98-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="29d98-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="29d98-110">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="29d98-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="29d98-111">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="29d98-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="29d98-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29d98-112">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="29d98-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="29d98-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29d98-114">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="29d98-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29d98-115">Строка, представляющая имя файла (или каталога), в котором произошел сбой метода.</span><span class="sxs-lookup"><span data-stu-id="29d98-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="29d98-116">Если метод выполнен, этот параметр имеет **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="29d98-116">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="29d98-117">*StartFileName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="29d98-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29d98-118">Строка, представляющая дочерний файл (или каталог), используемый в качестве отправной точки для этого метода.</span><span class="sxs-lookup"><span data-stu-id="29d98-118">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="29d98-119">Как правило, параметр *StartFileName* — это параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="29d98-119">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="29d98-120">Если этот параметр имеет **значение NULL**, операция выполняется над файлом или каталогом, указанным в вызове метода **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="29d98-120">If this parameter is **null**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="29d98-121">*Рекурсивно* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="29d98-121">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29d98-122">Если **значение — true**, метод также применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ девицефиле**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="29d98-122">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DeviceFile**](cim-devicefile.md) instance.</span></span> <span data-ttu-id="29d98-123">Для экземпляров файлов этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="29d98-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29d98-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="29d98-124">Return value</span></span>

<span data-ttu-id="29d98-125">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="29d98-125">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="29d98-126">0</span><span class="sxs-lookup"><span data-stu-id="29d98-126">0</span></span>

<span data-ttu-id="29d98-127">Успешно.</span><span class="sxs-lookup"><span data-stu-id="29d98-127">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="29d98-128">2</span><span class="sxs-lookup"><span data-stu-id="29d98-128">2</span></span>

<span data-ttu-id="29d98-129">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="29d98-129">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="29d98-130">8</span><span class="sxs-lookup"><span data-stu-id="29d98-130">8</span></span>

<span data-ttu-id="29d98-131">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="29d98-131">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="29d98-132">9</span><span class="sxs-lookup"><span data-stu-id="29d98-132">9</span></span>

<span data-ttu-id="29d98-133">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="29d98-133">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="29d98-134">10</span><span class="sxs-lookup"><span data-stu-id="29d98-134">10</span></span>

<span data-ttu-id="29d98-135">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="29d98-135">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="29d98-136">11</span><span class="sxs-lookup"><span data-stu-id="29d98-136">11</span></span>

<span data-ttu-id="29d98-137">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="29d98-137">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="29d98-138">12</span><span class="sxs-lookup"><span data-stu-id="29d98-138">12</span></span>

<span data-ttu-id="29d98-139">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="29d98-139">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="29d98-140">13</span><span class="sxs-lookup"><span data-stu-id="29d98-140">13</span></span>

<span data-ttu-id="29d98-141">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="29d98-141">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="29d98-142">14</span><span class="sxs-lookup"><span data-stu-id="29d98-142">14</span></span>

<span data-ttu-id="29d98-143">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="29d98-143">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="29d98-144">15</span><span class="sxs-lookup"><span data-stu-id="29d98-144">15</span></span>

<span data-ttu-id="29d98-145">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="29d98-145">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="29d98-146">16</span><span class="sxs-lookup"><span data-stu-id="29d98-146">16</span></span>

<span data-ttu-id="29d98-147">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="29d98-147">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="29d98-148">17</span><span class="sxs-lookup"><span data-stu-id="29d98-148">17</span></span>

<span data-ttu-id="29d98-149">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="29d98-149">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="29d98-150">21</span><span class="sxs-lookup"><span data-stu-id="29d98-150">21</span></span>

<span data-ttu-id="29d98-151">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="29d98-151">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29d98-152">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29d98-152">Remarks</span></span>

<span data-ttu-id="29d98-153">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="29d98-153">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="29d98-154">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="29d98-154">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="29d98-155">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="29d98-155">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="29d98-156">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="29d98-156">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="29d98-157">Требования</span><span class="sxs-lookup"><span data-stu-id="29d98-157">Requirements</span></span>



| <span data-ttu-id="29d98-158">Требование</span><span class="sxs-lookup"><span data-stu-id="29d98-158">Requirement</span></span> | <span data-ttu-id="29d98-159">Значение</span><span class="sxs-lookup"><span data-stu-id="29d98-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29d98-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="29d98-160">Minimum supported client</span></span><br/> | <span data-ttu-id="29d98-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29d98-161">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="29d98-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="29d98-162">Minimum supported server</span></span><br/> | <span data-ttu-id="29d98-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29d98-163">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="29d98-164">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="29d98-164">Namespace</span></span><br/>                | <span data-ttu-id="29d98-165">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="29d98-165">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="29d98-166">MOF</span><span class="sxs-lookup"><span data-stu-id="29d98-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29d98-167"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29d98-167"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="29d98-168">DLL</span><span class="sxs-lookup"><span data-stu-id="29d98-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29d98-169"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29d98-169"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29d98-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29d98-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29d98-171">\_ДЕВИЦЕФИЛЕ CIM</span><span class="sxs-lookup"><span data-stu-id="29d98-171">CIM\_DeviceFile</span></span>](takeownershipex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="29d98-172">**\_ДЕВИЦЕФИЛЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="29d98-172">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

