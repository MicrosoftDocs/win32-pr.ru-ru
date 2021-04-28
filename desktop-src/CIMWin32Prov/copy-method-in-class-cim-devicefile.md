---
description: Метод Copy класса CIM_DeviceFile. метод Copy копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное входным параметром.
ms.assetid: 6c1c6172-80a2-4779-903a-935f8c7091a5
ms.tgt_platform: multiple
title: Метод Copy класса CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 09c6d0f9400a04cc6e5a8ed4bd49ec7075b3c190
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089808"
---
# <a name="copy-method-of-the-cim_devicefile-class"></a><span data-ttu-id="f9966-103">Метод Copy \_ класса CIM девицефиле</span><span class="sxs-lookup"><span data-stu-id="f9966-103">Copy method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="f9966-104">Метод **Copy** копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное входным параметром.</span><span class="sxs-lookup"><span data-stu-id="f9966-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="f9966-105">Копирование не поддерживается, если требуется перезапись существующего логического файла.</span><span class="sxs-lookup"><span data-stu-id="f9966-105">A copy is not supported if it requires overwriting an existing logical file.</span></span> <span data-ttu-id="f9966-106">Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="f9966-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f9966-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="f9966-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f9966-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f9966-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f9966-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="f9966-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f9966-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f9966-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f9966-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9966-111">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="f9966-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9966-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9966-113">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f9966-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9966-114">Полное имя копии файла назначения (или каталога).</span><span class="sxs-lookup"><span data-stu-id="f9966-114">Fully qualified name of the destination file (or directory) copy.</span></span>

<span data-ttu-id="f9966-115">Пример: "c: \\ temp \\ невдиректори"</span><span class="sxs-lookup"><span data-stu-id="f9966-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9966-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f9966-116">Return value</span></span>

<span data-ttu-id="f9966-117">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="f9966-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="f9966-118">**0**</span><span class="sxs-lookup"><span data-stu-id="f9966-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f9966-119">Успешно.</span><span class="sxs-lookup"><span data-stu-id="f9966-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="f9966-120">**2**</span><span class="sxs-lookup"><span data-stu-id="f9966-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f9966-121">Access denied. (Недопустимое значение {значение_утверждения} для утверждения {имя_утверждения}. Доступ запрещен.)</span><span class="sxs-lookup"><span data-stu-id="f9966-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="f9966-122">**8**</span><span class="sxs-lookup"><span data-stu-id="f9966-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f9966-123">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="f9966-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="f9966-124">**9**</span><span class="sxs-lookup"><span data-stu-id="f9966-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f9966-125">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="f9966-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="f9966-126">**10**</span><span class="sxs-lookup"><span data-stu-id="f9966-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="f9966-127">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="f9966-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f9966-128">**11**</span><span class="sxs-lookup"><span data-stu-id="f9966-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="f9966-129">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="f9966-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="f9966-130">**12**</span><span class="sxs-lookup"><span data-stu-id="f9966-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="f9966-131">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="f9966-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="f9966-132">**13**</span><span class="sxs-lookup"><span data-stu-id="f9966-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="f9966-133">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="f9966-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="f9966-134">**14**</span><span class="sxs-lookup"><span data-stu-id="f9966-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="f9966-135">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="f9966-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="f9966-136">**15**</span><span class="sxs-lookup"><span data-stu-id="f9966-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="f9966-137">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="f9966-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="f9966-138">**16**</span><span class="sxs-lookup"><span data-stu-id="f9966-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="f9966-139">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="f9966-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="f9966-140">**17**</span><span class="sxs-lookup"><span data-stu-id="f9966-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="f9966-141">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="f9966-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="f9966-142">**открыт**</span><span class="sxs-lookup"><span data-stu-id="f9966-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f9966-143">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="f9966-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9966-144">Remarks</span><span class="sxs-lookup"><span data-stu-id="f9966-144">Remarks</span></span>

<span data-ttu-id="f9966-145">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="f9966-145">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="f9966-146">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="f9966-146">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="f9966-147">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="f9966-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f9966-148">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="f9966-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9966-149">Требования</span><span class="sxs-lookup"><span data-stu-id="f9966-149">Requirements</span></span>



| <span data-ttu-id="f9966-150">Требование</span><span class="sxs-lookup"><span data-stu-id="f9966-150">Requirement</span></span> | <span data-ttu-id="f9966-151">Значение</span><span class="sxs-lookup"><span data-stu-id="f9966-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9966-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f9966-152">Minimum supported client</span></span><br/> | <span data-ttu-id="f9966-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9966-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f9966-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f9966-154">Minimum supported server</span></span><br/> | <span data-ttu-id="f9966-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9966-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f9966-156">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f9966-156">Namespace</span></span><br/>                | <span data-ttu-id="f9966-157">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f9966-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f9966-158">MOF</span><span class="sxs-lookup"><span data-stu-id="f9966-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9966-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9966-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9966-160">DLL</span><span class="sxs-lookup"><span data-stu-id="f9966-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9966-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9966-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9966-162">См. также</span><span class="sxs-lookup"><span data-stu-id="f9966-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9966-163">\_ДЕВИЦЕФИЛЕ CIM</span><span class="sxs-lookup"><span data-stu-id="f9966-163">CIM\_DeviceFile</span></span>](copy-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="f9966-164">**\_ДЕВИЦЕФИЛЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="f9966-164">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

