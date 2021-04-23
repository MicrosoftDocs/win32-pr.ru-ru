---
description: Метод сжатия сжимает логический файл (или каталог), указанный в пути объекта.
ms.assetid: 4a26beaf-388b-4f37-b4ee-ef3a7d15d2b6
ms.tgt_platform: multiple
title: Метод сжатия класса CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12938001d62920916e75d70ad632170c3e92bd51
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895497"
---
# <a name="compress-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="03b2f-103">Метод сжатия \_ класса CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="03b2f-103">Compress method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="03b2f-104">Метод **сжатия** сжимает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="03b2f-104">The **Compress** method compresses the logical file (or directory) specified in the object path.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03b2f-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="03b2f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="03b2f-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="03b2f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="03b2f-107">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="03b2f-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="03b2f-108">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="03b2f-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="03b2f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03b2f-109">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="03b2f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="03b2f-110">Parameters</span></span>

<span data-ttu-id="03b2f-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="03b2f-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="03b2f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03b2f-112">Return value</span></span>

<span data-ttu-id="03b2f-113">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="03b2f-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="03b2f-114">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="03b2f-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="03b2f-115">0</span><span class="sxs-lookup"><span data-stu-id="03b2f-115">0</span></span>

<span data-ttu-id="03b2f-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="03b2f-116">Success.</span></span>

</dd> <dt>

<span data-ttu-id="03b2f-117">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="03b2f-117">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="03b2f-118">2</span><span class="sxs-lookup"><span data-stu-id="03b2f-118">2</span></span>

<span data-ttu-id="03b2f-119">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="03b2f-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="03b2f-120">**Неопределенный сбой**</span><span class="sxs-lookup"><span data-stu-id="03b2f-120">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="03b2f-121">8</span><span class="sxs-lookup"><span data-stu-id="03b2f-121">8</span></span>

<span data-ttu-id="03b2f-122">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="03b2f-122">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="03b2f-123">**Недопустимый объект**</span><span class="sxs-lookup"><span data-stu-id="03b2f-123">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="03b2f-124">9</span><span class="sxs-lookup"><span data-stu-id="03b2f-124">9</span></span>

<span data-ttu-id="03b2f-125">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="03b2f-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="03b2f-126">**Объект уже существует**</span><span class="sxs-lookup"><span data-stu-id="03b2f-126">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="03b2f-127">10</span><span class="sxs-lookup"><span data-stu-id="03b2f-127">10</span></span>

<span data-ttu-id="03b2f-128">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="03b2f-128">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="03b2f-129">**Файловая система не NTFS**</span><span class="sxs-lookup"><span data-stu-id="03b2f-129">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="03b2f-130">11</span><span class="sxs-lookup"><span data-stu-id="03b2f-130">11</span></span>

<span data-ttu-id="03b2f-131">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="03b2f-131">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="03b2f-132">**Платформа не NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="03b2f-132">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="03b2f-133">12</span><span class="sxs-lookup"><span data-stu-id="03b2f-133">12</span></span>

<span data-ttu-id="03b2f-134">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="03b2f-134">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="03b2f-135">**Диск не совпадает**</span><span class="sxs-lookup"><span data-stu-id="03b2f-135">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="03b2f-136">13</span><span class="sxs-lookup"><span data-stu-id="03b2f-136">13</span></span>

<span data-ttu-id="03b2f-137">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="03b2f-137">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="03b2f-138">**Каталог не пуст**</span><span class="sxs-lookup"><span data-stu-id="03b2f-138">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="03b2f-139">14</span><span class="sxs-lookup"><span data-stu-id="03b2f-139">14</span></span>

<span data-ttu-id="03b2f-140">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="03b2f-140">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="03b2f-141">**Нарушение общего доступа**</span><span class="sxs-lookup"><span data-stu-id="03b2f-141">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="03b2f-142">15</span><span class="sxs-lookup"><span data-stu-id="03b2f-142">15</span></span>

<span data-ttu-id="03b2f-143">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="03b2f-143">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="03b2f-144">**Недопустимый файл запуска**</span><span class="sxs-lookup"><span data-stu-id="03b2f-144">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="03b2f-145">16</span><span class="sxs-lookup"><span data-stu-id="03b2f-145">16</span></span>

<span data-ttu-id="03b2f-146">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="03b2f-146">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="03b2f-147">**Привилегия не удерживается**</span><span class="sxs-lookup"><span data-stu-id="03b2f-147">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="03b2f-148">17</span><span class="sxs-lookup"><span data-stu-id="03b2f-148">17</span></span>

<span data-ttu-id="03b2f-149">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="03b2f-149">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="03b2f-150">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="03b2f-150">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="03b2f-151">21</span><span class="sxs-lookup"><span data-stu-id="03b2f-151">21</span></span>

<span data-ttu-id="03b2f-152">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="03b2f-152">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03b2f-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03b2f-153">Remarks</span></span>

<span data-ttu-id="03b2f-154">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="03b2f-154">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="03b2f-155">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="03b2f-155">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="03b2f-156">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="03b2f-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="03b2f-157">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="03b2f-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="03b2f-158">Требования</span><span class="sxs-lookup"><span data-stu-id="03b2f-158">Requirements</span></span>



| <span data-ttu-id="03b2f-159">Требование</span><span class="sxs-lookup"><span data-stu-id="03b2f-159">Requirement</span></span> | <span data-ttu-id="03b2f-160">Значение</span><span class="sxs-lookup"><span data-stu-id="03b2f-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03b2f-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="03b2f-161">Minimum supported client</span></span><br/> | <span data-ttu-id="03b2f-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03b2f-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="03b2f-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="03b2f-163">Minimum supported server</span></span><br/> | <span data-ttu-id="03b2f-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03b2f-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="03b2f-165">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="03b2f-165">Namespace</span></span><br/>                | <span data-ttu-id="03b2f-166">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="03b2f-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="03b2f-167">MOF</span><span class="sxs-lookup"><span data-stu-id="03b2f-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03b2f-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03b2f-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="03b2f-169">DLL</span><span class="sxs-lookup"><span data-stu-id="03b2f-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03b2f-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03b2f-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03b2f-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03b2f-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03b2f-172">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="03b2f-172">CIM\_LogicalFile</span></span>](compress-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="03b2f-173">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="03b2f-173">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

