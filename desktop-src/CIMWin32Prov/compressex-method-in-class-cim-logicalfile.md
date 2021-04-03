---
description: Метод Компрессекс сжимает логический файл (или каталог), указанный в пути объекта. Этот метод является расширенной версией метода сжатия.
ms.assetid: 7d119865-c246-4cb5-9de4-48a4c42efd90
ms.tgt_platform: multiple
title: Метод Компрессекс класса CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7570cbe3ebc00708023a18da42ef35ff3306d3b0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895485"
---
# <a name="compressex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="4cb38-104">Метод Компрессекс \_ класса CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="4cb38-104">CompressEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="4cb38-105">Метод **компрессекс** сжимает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="4cb38-105">The **CompressEx** method compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="4cb38-106">Этот метод является расширенной версией метода [**сжатия**](compress-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="4cb38-106">This method is an extended version of the [**Compress**](compress-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4cb38-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="4cb38-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4cb38-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4cb38-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4cb38-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="4cb38-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4cb38-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="4cb38-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4cb38-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4cb38-111">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="4cb38-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="4cb38-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cb38-113">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4cb38-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb38-114">Имя файла (или каталога), в котором произошел сбой метода.</span><span class="sxs-lookup"><span data-stu-id="4cb38-114">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="4cb38-115">Если метод выполнен, этот параметр имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="4cb38-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="4cb38-116">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="4cb38-116">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb38-117">Дочерний файл (или каталог) для использования в качестве отправной точки для метода.</span><span class="sxs-lookup"><span data-stu-id="4cb38-117">Child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="4cb38-118">Как правило, этот параметр представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="4cb38-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="4cb38-119">Если этот параметр имеет значение null, операция выполняется над файлом (или каталогом), указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="4cb38-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="4cb38-120">*Рекурсивно* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="4cb38-120">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4cb38-121">Если **значение — true**, метод также применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="4cb38-121">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="4cb38-122">Для экземпляров файлов этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="4cb38-122">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cb38-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4cb38-123">Return value</span></span>

<span data-ttu-id="4cb38-124">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="4cb38-124">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="4cb38-125">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="4cb38-125">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="4cb38-126">0</span><span class="sxs-lookup"><span data-stu-id="4cb38-126">0</span></span>

<span data-ttu-id="4cb38-127">Успешно.</span><span class="sxs-lookup"><span data-stu-id="4cb38-127">Success.</span></span>

</dd> <dt>

<span data-ttu-id="4cb38-128">**Доступ запрещен**</span><span class="sxs-lookup"><span data-stu-id="4cb38-128">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="4cb38-129">2</span><span class="sxs-lookup"><span data-stu-id="4cb38-129">2</span></span>

<span data-ttu-id="4cb38-130">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="4cb38-130">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="4cb38-131">**Неопределенный сбой**</span><span class="sxs-lookup"><span data-stu-id="4cb38-131">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="4cb38-132">8</span><span class="sxs-lookup"><span data-stu-id="4cb38-132">8</span></span>

<span data-ttu-id="4cb38-133">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="4cb38-133">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="4cb38-134">**Недопустимый объект**</span><span class="sxs-lookup"><span data-stu-id="4cb38-134">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="4cb38-135">9</span><span class="sxs-lookup"><span data-stu-id="4cb38-135">9</span></span>

<span data-ttu-id="4cb38-136">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="4cb38-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="4cb38-137">**Объект уже существует**</span><span class="sxs-lookup"><span data-stu-id="4cb38-137">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="4cb38-138">10</span><span class="sxs-lookup"><span data-stu-id="4cb38-138">10</span></span>

<span data-ttu-id="4cb38-139">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="4cb38-139">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="4cb38-140">**Файловая система не NTFS**</span><span class="sxs-lookup"><span data-stu-id="4cb38-140">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="4cb38-141">11</span><span class="sxs-lookup"><span data-stu-id="4cb38-141">11</span></span>

<span data-ttu-id="4cb38-142">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="4cb38-142">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="4cb38-143">**Платформа не NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="4cb38-143">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="4cb38-144">12</span><span class="sxs-lookup"><span data-stu-id="4cb38-144">12</span></span>

<span data-ttu-id="4cb38-145">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="4cb38-145">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="4cb38-146">**Диск не совпадает**</span><span class="sxs-lookup"><span data-stu-id="4cb38-146">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="4cb38-147">13</span><span class="sxs-lookup"><span data-stu-id="4cb38-147">13</span></span>

<span data-ttu-id="4cb38-148">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="4cb38-148">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="4cb38-149">**Каталог не пуст**</span><span class="sxs-lookup"><span data-stu-id="4cb38-149">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="4cb38-150">14</span><span class="sxs-lookup"><span data-stu-id="4cb38-150">14</span></span>

<span data-ttu-id="4cb38-151">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="4cb38-151">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="4cb38-152">**Нарушение общего доступа**</span><span class="sxs-lookup"><span data-stu-id="4cb38-152">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="4cb38-153">15</span><span class="sxs-lookup"><span data-stu-id="4cb38-153">15</span></span>

<span data-ttu-id="4cb38-154">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="4cb38-154">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="4cb38-155">**Недопустимый файл запуска**</span><span class="sxs-lookup"><span data-stu-id="4cb38-155">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="4cb38-156">16</span><span class="sxs-lookup"><span data-stu-id="4cb38-156">16</span></span>

<span data-ttu-id="4cb38-157">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="4cb38-157">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="4cb38-158">**Привилегия не удерживается**</span><span class="sxs-lookup"><span data-stu-id="4cb38-158">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="4cb38-159">17</span><span class="sxs-lookup"><span data-stu-id="4cb38-159">17</span></span>

<span data-ttu-id="4cb38-160">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="4cb38-160">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="4cb38-161">**недопустимый параметр.**</span><span class="sxs-lookup"><span data-stu-id="4cb38-161">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4cb38-162">21</span><span class="sxs-lookup"><span data-stu-id="4cb38-162">21</span></span>

<span data-ttu-id="4cb38-163">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="4cb38-163">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4cb38-164">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4cb38-164">Remarks</span></span>

<span data-ttu-id="4cb38-165">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="4cb38-165">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="4cb38-166">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="4cb38-166">To use this method, you must implement it in your own provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cb38-167">Требования</span><span class="sxs-lookup"><span data-stu-id="4cb38-167">Requirements</span></span>



| <span data-ttu-id="4cb38-168">Требование</span><span class="sxs-lookup"><span data-stu-id="4cb38-168">Requirement</span></span> | <span data-ttu-id="4cb38-169">Значение</span><span class="sxs-lookup"><span data-stu-id="4cb38-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4cb38-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4cb38-170">Minimum supported client</span></span><br/> | <span data-ttu-id="4cb38-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4cb38-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4cb38-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4cb38-172">Minimum supported server</span></span><br/> | <span data-ttu-id="4cb38-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4cb38-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4cb38-174">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4cb38-174">Namespace</span></span><br/>                | <span data-ttu-id="4cb38-175">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4cb38-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4cb38-176">MOF</span><span class="sxs-lookup"><span data-stu-id="4cb38-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4cb38-177"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4cb38-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4cb38-178">DLL</span><span class="sxs-lookup"><span data-stu-id="4cb38-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cb38-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cb38-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cb38-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cb38-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cb38-181">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="4cb38-181">CIM\_LogicalFile</span></span>](compressex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="4cb38-182">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="4cb38-182">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

