---
description: Метод Delete удаляет логический файл (или каталог), указанный в пути объекта. Этот метод наследуется от CIM \_ LogicalFile.
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
ms.openlocfilehash: 32e29808b60c9933bec927ed7e351fc8c5aa9250
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072415"
---
# <a name="delete-method-of-the-cim_devicefile-class"></a><span data-ttu-id="10fd9-104">Метод DELETE \_ класса ДЕВИЦЕФИЛЕ CIM</span><span class="sxs-lookup"><span data-stu-id="10fd9-104">Delete method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="10fd9-105">Метод **Delete** удаляет логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="10fd9-105">The **Delete** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="10fd9-106">Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="10fd9-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="10fd9-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="10fd9-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="10fd9-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="10fd9-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="10fd9-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="10fd9-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="10fd9-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="10fd9-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="10fd9-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10fd9-111">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="10fd9-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="10fd9-112">Parameters</span></span>

<span data-ttu-id="10fd9-113">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="10fd9-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="10fd9-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="10fd9-114">Return value</span></span>

<span data-ttu-id="10fd9-115">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="10fd9-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="10fd9-116">**0**</span><span class="sxs-lookup"><span data-stu-id="10fd9-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="10fd9-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="10fd9-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="10fd9-118">**2**</span><span class="sxs-lookup"><span data-stu-id="10fd9-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="10fd9-119">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="10fd9-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="10fd9-120">**8**</span><span class="sxs-lookup"><span data-stu-id="10fd9-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="10fd9-121">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="10fd9-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="10fd9-122">**9**</span><span class="sxs-lookup"><span data-stu-id="10fd9-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="10fd9-123">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="10fd9-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="10fd9-124">**10**</span><span class="sxs-lookup"><span data-stu-id="10fd9-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="10fd9-125">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="10fd9-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="10fd9-126">**11**</span><span class="sxs-lookup"><span data-stu-id="10fd9-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="10fd9-127">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="10fd9-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="10fd9-128">**12**</span><span class="sxs-lookup"><span data-stu-id="10fd9-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="10fd9-129">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="10fd9-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="10fd9-130">**13**</span><span class="sxs-lookup"><span data-stu-id="10fd9-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="10fd9-131">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="10fd9-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="10fd9-132">**14**</span><span class="sxs-lookup"><span data-stu-id="10fd9-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="10fd9-133">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="10fd9-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="10fd9-134">**15**</span><span class="sxs-lookup"><span data-stu-id="10fd9-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="10fd9-135">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="10fd9-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="10fd9-136">**16**</span><span class="sxs-lookup"><span data-stu-id="10fd9-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="10fd9-137">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="10fd9-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="10fd9-138">**17**</span><span class="sxs-lookup"><span data-stu-id="10fd9-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="10fd9-139">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="10fd9-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="10fd9-140">**открыт**</span><span class="sxs-lookup"><span data-stu-id="10fd9-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="10fd9-141">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="10fd9-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10fd9-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10fd9-142">Remarks</span></span>

<span data-ttu-id="10fd9-143">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="10fd9-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="10fd9-144">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="10fd9-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="10fd9-145">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="10fd9-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="10fd9-146">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="10fd9-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="10fd9-147">Требования</span><span class="sxs-lookup"><span data-stu-id="10fd9-147">Requirements</span></span>



| <span data-ttu-id="10fd9-148">Требование</span><span class="sxs-lookup"><span data-stu-id="10fd9-148">Requirement</span></span> | <span data-ttu-id="10fd9-149">Значение</span><span class="sxs-lookup"><span data-stu-id="10fd9-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10fd9-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10fd9-150">Minimum supported client</span></span><br/> | <span data-ttu-id="10fd9-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10fd9-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10fd9-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10fd9-152">Minimum supported server</span></span><br/> | <span data-ttu-id="10fd9-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10fd9-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10fd9-154">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="10fd9-154">Namespace</span></span><br/>                | <span data-ttu-id="10fd9-155">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="10fd9-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="10fd9-156">MOF</span><span class="sxs-lookup"><span data-stu-id="10fd9-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10fd9-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10fd9-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="10fd9-158">DLL</span><span class="sxs-lookup"><span data-stu-id="10fd9-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10fd9-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10fd9-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10fd9-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10fd9-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10fd9-161">\_ДЕВИЦЕФИЛЕ CIM</span><span class="sxs-lookup"><span data-stu-id="10fd9-161">CIM\_DeviceFile</span></span>](delete-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="10fd9-162">**\_ДЕВИЦЕФИЛЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="10fd9-162">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

