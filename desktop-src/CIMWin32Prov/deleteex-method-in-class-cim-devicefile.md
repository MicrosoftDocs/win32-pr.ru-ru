---
description: Метод Делетикс удаляет логический файл (или каталог), указанный в пути объекта. Этот метод является расширенной версией метода Delete и наследуется от CIM \_ LogicalFile.
ms.assetid: ef4d08cd-7287-47be-bcfc-edc248ac5c9b
ms.tgt_platform: multiple
title: Метод Делетикс класса CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4e68e7118088b9da1f1a1e2990c0a253ac85714
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807265"
---
# <a name="deleteex-method-of-the-cim_devicefile-class"></a><span data-ttu-id="fce17-104">Метод Делетикс \_ класса CIM девицефиле</span><span class="sxs-lookup"><span data-stu-id="fce17-104">DeleteEx method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="fce17-105">Метод **делетикс** удаляет логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="fce17-105">The **DeleteEx** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="fce17-106">Этот метод является расширенной версией метода [**Delete**](delete-method-in-class-cim-devicefile.md) и наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="fce17-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-devicefile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fce17-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="fce17-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fce17-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fce17-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fce17-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="fce17-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fce17-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fce17-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fce17-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fce17-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="fce17-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="fce17-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fce17-113">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fce17-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fce17-114">Строка, представляющая имя файла (или каталога), в котором произошел сбой метода.</span><span class="sxs-lookup"><span data-stu-id="fce17-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="fce17-115">Если метод выполнен, этот параметр имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="fce17-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="fce17-116">*StartFileName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fce17-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fce17-117">Строка, представляющая дочерний файл (или каталог), используемый в качестве отправной точки для этого метода.</span><span class="sxs-lookup"><span data-stu-id="fce17-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="fce17-118">Как правило, параметр **StartFileName** — это параметр **стопфиленаме** , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="fce17-118">Typically, the **StartFileName** parameter is the **StopFileName** parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="fce17-119">Если этот параметр имеет значение null, операция выполняется над файлом или каталогом, указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="fce17-119">If this parameter is null, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fce17-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fce17-120">Return value</span></span>

<span data-ttu-id="fce17-121">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="fce17-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="fce17-122">0</span><span class="sxs-lookup"><span data-stu-id="fce17-122">0</span></span>

<span data-ttu-id="fce17-123">Успешно.</span><span class="sxs-lookup"><span data-stu-id="fce17-123">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="fce17-124">2</span><span class="sxs-lookup"><span data-stu-id="fce17-124">2</span></span>

<span data-ttu-id="fce17-125">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="fce17-125">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="fce17-126">8</span><span class="sxs-lookup"><span data-stu-id="fce17-126">8</span></span>

<span data-ttu-id="fce17-127">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="fce17-127">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="fce17-128">9</span><span class="sxs-lookup"><span data-stu-id="fce17-128">9</span></span>

<span data-ttu-id="fce17-129">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="fce17-129">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="fce17-130">10</span><span class="sxs-lookup"><span data-stu-id="fce17-130">10</span></span>

<span data-ttu-id="fce17-131">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="fce17-131">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="fce17-132">11</span><span class="sxs-lookup"><span data-stu-id="fce17-132">11</span></span>

<span data-ttu-id="fce17-133">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="fce17-133">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="fce17-134">12</span><span class="sxs-lookup"><span data-stu-id="fce17-134">12</span></span>

<span data-ttu-id="fce17-135">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="fce17-135">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="fce17-136">13</span><span class="sxs-lookup"><span data-stu-id="fce17-136">13</span></span>

<span data-ttu-id="fce17-137">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="fce17-137">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="fce17-138">14</span><span class="sxs-lookup"><span data-stu-id="fce17-138">14</span></span>

<span data-ttu-id="fce17-139">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="fce17-139">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="fce17-140">15</span><span class="sxs-lookup"><span data-stu-id="fce17-140">15</span></span>

<span data-ttu-id="fce17-141">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="fce17-141">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="fce17-142">16</span><span class="sxs-lookup"><span data-stu-id="fce17-142">16</span></span>

<span data-ttu-id="fce17-143">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="fce17-143">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="fce17-144">17</span><span class="sxs-lookup"><span data-stu-id="fce17-144">17</span></span>

<span data-ttu-id="fce17-145">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="fce17-145">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="fce17-146">21</span><span class="sxs-lookup"><span data-stu-id="fce17-146">21</span></span>

<span data-ttu-id="fce17-147">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="fce17-147">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fce17-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fce17-148">Remarks</span></span>

<span data-ttu-id="fce17-149">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="fce17-149">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="fce17-150">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="fce17-150">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="fce17-151">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="fce17-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fce17-152">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="fce17-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fce17-153">Требования</span><span class="sxs-lookup"><span data-stu-id="fce17-153">Requirements</span></span>



| <span data-ttu-id="fce17-154">Требование</span><span class="sxs-lookup"><span data-stu-id="fce17-154">Requirement</span></span> | <span data-ttu-id="fce17-155">Значение</span><span class="sxs-lookup"><span data-stu-id="fce17-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fce17-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fce17-156">Minimum supported client</span></span><br/> | <span data-ttu-id="fce17-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fce17-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fce17-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fce17-158">Minimum supported server</span></span><br/> | <span data-ttu-id="fce17-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fce17-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fce17-160">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fce17-160">Namespace</span></span><br/>                | <span data-ttu-id="fce17-161">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fce17-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fce17-162">MOF</span><span class="sxs-lookup"><span data-stu-id="fce17-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fce17-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fce17-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fce17-164">DLL</span><span class="sxs-lookup"><span data-stu-id="fce17-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fce17-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fce17-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fce17-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fce17-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce17-167">\_ДЕВИЦЕФИЛЕ CIM</span><span class="sxs-lookup"><span data-stu-id="fce17-167">CIM\_DeviceFile</span></span>](deleteex-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="fce17-168">**\_ДЕВИЦЕФИЛЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="fce17-168">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

