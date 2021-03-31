---
description: Метод Delete удаляет логический файл (или каталог), указанный в пути объекта. Этот метод наследуется от CIM \_ LogicalFile.
ms.assetid: 74f59073-a17a-4be5-8247-fba8d023f448
ms.tgt_platform: multiple
title: Метод Delete класса CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6ad193231ffc15f5ce61257ee545f583d8e58e17
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990769"
---
# <a name="delete-method-of-the-cim_directory-class"></a><span data-ttu-id="b0597-104">Метод DELETE \_ класса каталога CIM</span><span class="sxs-lookup"><span data-stu-id="b0597-104">Delete method of the CIM\_Directory class</span></span>

<span data-ttu-id="b0597-105">Метод **Delete** удаляет логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="b0597-105">The **Delete** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="b0597-106">Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b0597-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b0597-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="b0597-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b0597-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b0597-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b0597-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="b0597-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b0597-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b0597-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b0597-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0597-111">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="b0597-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0597-112">Parameters</span></span>

<span data-ttu-id="b0597-113">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b0597-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0597-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0597-114">Return value</span></span>

<span data-ttu-id="b0597-115">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="b0597-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="b0597-116">**0**</span><span class="sxs-lookup"><span data-stu-id="b0597-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b0597-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="b0597-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="b0597-118">**2**</span><span class="sxs-lookup"><span data-stu-id="b0597-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b0597-119">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="b0597-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="b0597-120">**8**</span><span class="sxs-lookup"><span data-stu-id="b0597-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b0597-121">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="b0597-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="b0597-122">**9**</span><span class="sxs-lookup"><span data-stu-id="b0597-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b0597-123">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="b0597-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="b0597-124">**10**</span><span class="sxs-lookup"><span data-stu-id="b0597-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="b0597-125">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="b0597-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b0597-126">**11**</span><span class="sxs-lookup"><span data-stu-id="b0597-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="b0597-127">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="b0597-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="b0597-128">**12**</span><span class="sxs-lookup"><span data-stu-id="b0597-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="b0597-129">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="b0597-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="b0597-130">**13**</span><span class="sxs-lookup"><span data-stu-id="b0597-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="b0597-131">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="b0597-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="b0597-132">**14**</span><span class="sxs-lookup"><span data-stu-id="b0597-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="b0597-133">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="b0597-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="b0597-134">**15**</span><span class="sxs-lookup"><span data-stu-id="b0597-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="b0597-135">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="b0597-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="b0597-136">**16**</span><span class="sxs-lookup"><span data-stu-id="b0597-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="b0597-137">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="b0597-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="b0597-138">**17**</span><span class="sxs-lookup"><span data-stu-id="b0597-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="b0597-139">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="b0597-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="b0597-140">**открыт**</span><span class="sxs-lookup"><span data-stu-id="b0597-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b0597-141">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="b0597-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0597-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0597-142">Remarks</span></span>

<span data-ttu-id="b0597-143">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="b0597-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="b0597-144">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="b0597-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="b0597-145">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="b0597-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b0597-146">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="b0597-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0597-147">Требования</span><span class="sxs-lookup"><span data-stu-id="b0597-147">Requirements</span></span>



| <span data-ttu-id="b0597-148">Требование</span><span class="sxs-lookup"><span data-stu-id="b0597-148">Requirement</span></span> | <span data-ttu-id="b0597-149">Значение</span><span class="sxs-lookup"><span data-stu-id="b0597-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0597-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0597-150">Minimum supported client</span></span><br/> | <span data-ttu-id="b0597-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0597-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b0597-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0597-152">Minimum supported server</span></span><br/> | <span data-ttu-id="b0597-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0597-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b0597-154">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b0597-154">Namespace</span></span><br/>                | <span data-ttu-id="b0597-155">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b0597-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b0597-156">MOF</span><span class="sxs-lookup"><span data-stu-id="b0597-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0597-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0597-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0597-158">DLL</span><span class="sxs-lookup"><span data-stu-id="b0597-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0597-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0597-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0597-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0597-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0597-161">\_Каталог CIM</span><span class="sxs-lookup"><span data-stu-id="b0597-161">CIM\_Directory</span></span>](delete-method-in-class-cim-directory.md)
</dt> <dt>

[<span data-ttu-id="b0597-162">**\_Каталог CIM**</span><span class="sxs-lookup"><span data-stu-id="b0597-162">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> </dl>

 

