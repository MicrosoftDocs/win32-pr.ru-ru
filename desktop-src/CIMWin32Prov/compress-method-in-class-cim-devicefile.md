---
description: Метод сжатия сжимает логический файл (или каталог), указанный в пути объекта. Этот метод наследуется от CIM \_ LogicalFile.
ms.assetid: baafe82c-fe4d-49b2-8868-4495f573895a
ms.tgt_platform: multiple
title: Метод сжатия класса CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0af6a1792383ad2665064a6e577807997a1aba16
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895498"
---
# <a name="compress-method-of-the-cim_devicefile-class"></a><span data-ttu-id="9a009-104">Метод сжатия \_ класса CIM девицефиле</span><span class="sxs-lookup"><span data-stu-id="9a009-104">Compress method of the CIM\_DeviceFile class</span></span>

<span data-ttu-id="9a009-105">Метод **сжатия** сжимает логический файл (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="9a009-105">The **Compress** method compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="9a009-106">Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="9a009-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9a009-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="9a009-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9a009-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9a009-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9a009-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="9a009-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9a009-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9a009-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9a009-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a009-111">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="9a009-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a009-112">Parameters</span></span>

<span data-ttu-id="9a009-113">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9a009-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a009-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a009-114">Return value</span></span>

<span data-ttu-id="9a009-115">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="9a009-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="9a009-116">**0**</span><span class="sxs-lookup"><span data-stu-id="9a009-116">**0**</span></span>
</dt> <dd>

<span data-ttu-id="9a009-117">Успешно.</span><span class="sxs-lookup"><span data-stu-id="9a009-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="9a009-118">**2**</span><span class="sxs-lookup"><span data-stu-id="9a009-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="9a009-119">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="9a009-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="9a009-120">**8**</span><span class="sxs-lookup"><span data-stu-id="9a009-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="9a009-121">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="9a009-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="9a009-122">**9**</span><span class="sxs-lookup"><span data-stu-id="9a009-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="9a009-123">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="9a009-123">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="9a009-124">**10**</span><span class="sxs-lookup"><span data-stu-id="9a009-124">**10**</span></span>
</dt> <dd>

<span data-ttu-id="9a009-125">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="9a009-125">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="9a009-126">**11**</span><span class="sxs-lookup"><span data-stu-id="9a009-126">**11**</span></span>
</dt> <dd>

<span data-ttu-id="9a009-127">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="9a009-127">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="9a009-128">**12**</span><span class="sxs-lookup"><span data-stu-id="9a009-128">**12**</span></span>
</dt> <dd>

<span data-ttu-id="9a009-129">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="9a009-129">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="9a009-130">**13**</span><span class="sxs-lookup"><span data-stu-id="9a009-130">**13**</span></span>
</dt> <dd>

<span data-ttu-id="9a009-131">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="9a009-131">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="9a009-132">**14**</span><span class="sxs-lookup"><span data-stu-id="9a009-132">**14**</span></span>
</dt> <dd>

<span data-ttu-id="9a009-133">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="9a009-133">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="9a009-134">**15**</span><span class="sxs-lookup"><span data-stu-id="9a009-134">**15**</span></span>
</dt> <dd>

<span data-ttu-id="9a009-135">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="9a009-135">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="9a009-136">**16**</span><span class="sxs-lookup"><span data-stu-id="9a009-136">**16**</span></span>
</dt> <dd>

<span data-ttu-id="9a009-137">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="9a009-137">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="9a009-138">**17**</span><span class="sxs-lookup"><span data-stu-id="9a009-138">**17**</span></span>
</dt> <dd>

<span data-ttu-id="9a009-139">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="9a009-139">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="9a009-140">**открыт**</span><span class="sxs-lookup"><span data-stu-id="9a009-140">**21**</span></span>
</dt> <dd>

<span data-ttu-id="9a009-141">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="9a009-141">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9a009-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a009-142">Remarks</span></span>

<span data-ttu-id="9a009-143">В настоящее время этот метод не реализован инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="9a009-143">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="9a009-144">Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.</span><span class="sxs-lookup"><span data-stu-id="9a009-144">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="9a009-145">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="9a009-145">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9a009-146">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="9a009-146">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a009-147">Требования</span><span class="sxs-lookup"><span data-stu-id="9a009-147">Requirements</span></span>



| <span data-ttu-id="9a009-148">Требование</span><span class="sxs-lookup"><span data-stu-id="9a009-148">Requirement</span></span> | <span data-ttu-id="9a009-149">Значение</span><span class="sxs-lookup"><span data-stu-id="9a009-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a009-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9a009-150">Minimum supported client</span></span><br/> | <span data-ttu-id="9a009-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a009-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9a009-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9a009-152">Minimum supported server</span></span><br/> | <span data-ttu-id="9a009-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a009-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9a009-154">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9a009-154">Namespace</span></span><br/>                | <span data-ttu-id="9a009-155">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9a009-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9a009-156">MOF</span><span class="sxs-lookup"><span data-stu-id="9a009-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a009-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a009-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a009-158">DLL</span><span class="sxs-lookup"><span data-stu-id="9a009-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a009-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a009-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a009-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a009-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a009-161">\_ДЕВИЦЕФИЛЕ CIM</span><span class="sxs-lookup"><span data-stu-id="9a009-161">CIM\_DeviceFile</span></span>](compress-method-in-class-cim-devicefile.md)
</dt> <dt>

[<span data-ttu-id="9a009-162">**\_ДЕВИЦЕФИЛЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="9a009-162">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> </dl>

 

