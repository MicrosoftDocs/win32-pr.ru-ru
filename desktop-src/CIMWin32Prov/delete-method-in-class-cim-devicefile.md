---
description: Метод Delete класса CIM_DeviceFile. метод Delete удаляет логический файл (или каталог), указанный в пути к объекту. Этот метод наследуется от CIM \_ LogicalFile.
ms.assetid: 490d0578-a545-423b-9640-ec09f4ef8d96
ms.tgt_platform: multiple
title: Метод Delete класса CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e96ba9837252158510c306a622df86c09bbfd96
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089632"
---
# <a name="delete-method-of-the-cim_devicefile-class"></a><span data-ttu-id="04762-104">Метод DELETE \_ класса ДЕВИЦЕФИЛЕ CIM</span><span class="sxs-lookup"><span data-stu-id="04762-104">Delete method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="04762-105">Метод **Delete** удаляет логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="04762-105">The **Delete** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="04762-106">Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="04762-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04762-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="04762-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="04762-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="04762-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="04762-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="04762-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="04762-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="04762-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="04762-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04762-111">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="04762-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="04762-112">Parameters</span></span>

<span data-ttu-id="04762-113">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="04762-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="04762-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04762-114">Return value</span></span>

<span data-ttu-id="04762-115">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="04762-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="04762-116">**0**</span><span class="sxs-lookup"><span data-stu-id="04762-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="04762-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="04762-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="04762-118">**2**</span><span class="sxs-lookup"><span data-stu-id="04762-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="04762-119">Access denied. (Недопустимое значение {значение_утверждения} для утверждения {имя_утверждения}. Доступ запрещен.)</span><span class="sxs-lookup"><span data-stu-id="04762-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="04762-120">**8**</span><span class="sxs-lookup"><span data-stu-id="04762-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="04762-121">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="04762-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="04762-122">**9**</span><span class="sxs-lookup"><span data-stu-id="04762-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="04762-123">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="04762-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="04762-124">**10**</span><span class="sxs-lookup"><span data-stu-id="04762-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="04762-125">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="04762-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="04762-126">**11**</span><span class="sxs-lookup"><span data-stu-id="04762-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="04762-127">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="04762-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="04762-128">**12**</span><span class="sxs-lookup"><span data-stu-id="04762-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="04762-129">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="04762-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="04762-130">**13**</span><span class="sxs-lookup"><span data-stu-id="04762-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="04762-131">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="04762-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="04762-132">**14**</span><span class="sxs-lookup"><span data-stu-id="04762-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="04762-133">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="04762-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="04762-134">**15**</span><span class="sxs-lookup"><span data-stu-id="04762-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="04762-135">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="04762-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="04762-136">**16**</span><span class="sxs-lookup"><span data-stu-id="04762-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="04762-137">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="04762-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="04762-138">**17**</span><span class="sxs-lookup"><span data-stu-id="04762-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="04762-139">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="04762-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="04762-140">**открыт**</span><span class="sxs-lookup"><span data-stu-id="04762-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="04762-141">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="04762-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04762-142">Remarks</span><span class="sxs-lookup"><span data-stu-id="04762-142">Remarks</span></span>

<span data-ttu-id="04762-143">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="04762-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="04762-144">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="04762-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="04762-145">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="04762-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="04762-146">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="04762-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="04762-147">Требования</span><span class="sxs-lookup"><span data-stu-id="04762-147">Requirements</span></span>



| <span data-ttu-id="04762-148">Требование</span><span class="sxs-lookup"><span data-stu-id="04762-148">Requirement</span></span> | <span data-ttu-id="04762-149">Значение</span><span class="sxs-lookup"><span data-stu-id="04762-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04762-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04762-150">Minimum supported client</span></span><br/> | <span data-ttu-id="04762-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04762-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="04762-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04762-152">Minimum supported server</span></span><br/> | <span data-ttu-id="04762-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04762-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="04762-154">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="04762-154">Namespace</span></span><br/>                | <span data-ttu-id="04762-155">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="04762-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="04762-156">MOF</span><span class="sxs-lookup"><span data-stu-id="04762-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04762-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04762-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="04762-158">DLL</span><span class="sxs-lookup"><span data-stu-id="04762-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04762-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04762-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04762-160">См. также</span><span class="sxs-lookup"><span data-stu-id="04762-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04762-161">\_ДЕВИЦЕФИЛЕ CIM</span><span class="sxs-lookup"><span data-stu-id="04762-161">CIM\_DeviceFile</span></span>](delete-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="04762-162">**\_ДЕВИЦЕФИЛЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="04762-162">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

