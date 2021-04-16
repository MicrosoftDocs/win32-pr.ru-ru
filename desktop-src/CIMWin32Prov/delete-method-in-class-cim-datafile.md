---
description: Метод Delete удаляет логический файл (или каталог), указанный в пути к объекту. Этот метод наследуется от CIM \_ LogicalFile.
ms.assetid: bc2ff005-b2c3-4098-b597-3a96d345b497
ms.tgt_platform: multiple
title: Метод Delete класса CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: adb1cc8ca08dc3139b3e5b85db81d35ae3b7100c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655999"
---
# <a name="delete-method-of-the-cim_datafile-class"></a><span data-ttu-id="2e8f2-104">Метод DELETE \_ класса CIM File</span><span class="sxs-lookup"><span data-stu-id="2e8f2-104">Delete method of the CIM\_DataFile class</span></span>

<span data-ttu-id="2e8f2-105">Метод **Delete** удаляет логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-105">The **Delete** method deletes the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="2e8f2-106">Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2e8f2-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e8f2-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2e8f2-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2e8f2-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2e8f2-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="2e8f2-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2e8f2-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2e8f2-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2e8f2-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e8f2-111">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="2e8f2-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e8f2-112">Parameters</span></span>

<span data-ttu-id="2e8f2-113">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e8f2-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e8f2-114">Return value</span></span>

<span data-ttu-id="2e8f2-115">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="2e8f2-116">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2e8f2-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2e8f2-117">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="2e8f2-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="2e8f2-118">**0**</span><span class="sxs-lookup"><span data-stu-id="2e8f2-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="2e8f2-119">Успешно.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-119">Success.</span></span>

</dd> <dt>

<span data-ttu-id="2e8f2-120">**2**</span><span class="sxs-lookup"><span data-stu-id="2e8f2-120">**2**</span></span>
</dt> <dd>

<span data-ttu-id="2e8f2-121">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="2e8f2-122">**8**</span><span class="sxs-lookup"><span data-stu-id="2e8f2-122">**8**</span></span>
</dt> <dd>

<span data-ttu-id="2e8f2-123">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-123">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="2e8f2-124">**9**</span><span class="sxs-lookup"><span data-stu-id="2e8f2-124">**9**</span></span>
</dt> <dd>

<span data-ttu-id="2e8f2-125">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="2e8f2-126">**10**</span><span class="sxs-lookup"><span data-stu-id="2e8f2-126">**10**</span></span>
</dt> <dd>

<span data-ttu-id="2e8f2-127">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-127">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2e8f2-128">**11**</span><span class="sxs-lookup"><span data-stu-id="2e8f2-128">**11**</span></span>
</dt> <dd>

<span data-ttu-id="2e8f2-129">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-129">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="2e8f2-130">**12**</span><span class="sxs-lookup"><span data-stu-id="2e8f2-130">**12**</span></span>
</dt> <dd>

<span data-ttu-id="2e8f2-131">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-131">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="2e8f2-132">**13**</span><span class="sxs-lookup"><span data-stu-id="2e8f2-132">**13**</span></span>
</dt> <dd>

<span data-ttu-id="2e8f2-133">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-133">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="2e8f2-134">**14**</span><span class="sxs-lookup"><span data-stu-id="2e8f2-134">**14**</span></span>
</dt> <dd>

<span data-ttu-id="2e8f2-135">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-135">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="2e8f2-136">**15**</span><span class="sxs-lookup"><span data-stu-id="2e8f2-136">**15**</span></span>
</dt> <dd>

<span data-ttu-id="2e8f2-137">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-137">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="2e8f2-138">**16**</span><span class="sxs-lookup"><span data-stu-id="2e8f2-138">**16**</span></span>
</dt> <dd>

<span data-ttu-id="2e8f2-139">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-139">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="2e8f2-140">**17**</span><span class="sxs-lookup"><span data-stu-id="2e8f2-140">**17**</span></span>
</dt> <dd>

<span data-ttu-id="2e8f2-141">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-141">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="2e8f2-142">**открыт**</span><span class="sxs-lookup"><span data-stu-id="2e8f2-142">**21**</span></span>
</dt> <dd>

<span data-ttu-id="2e8f2-143">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-143">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e8f2-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e8f2-144">Remarks</span></span>

<span data-ttu-id="2e8f2-145">Метод **Delete** в [**\_ файле CIM**](cim-datafile.md) реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-145">The **Delete** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="2e8f2-146">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-146">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2e8f2-147">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="2e8f2-147">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e8f2-148">Требования</span><span class="sxs-lookup"><span data-stu-id="2e8f2-148">Requirements</span></span>



| <span data-ttu-id="2e8f2-149">Требование</span><span class="sxs-lookup"><span data-stu-id="2e8f2-149">Requirement</span></span> | <span data-ttu-id="2e8f2-150">Значение</span><span class="sxs-lookup"><span data-stu-id="2e8f2-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e8f2-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2e8f2-151">Minimum supported client</span></span><br/> | <span data-ttu-id="2e8f2-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2e8f2-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2e8f2-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2e8f2-153">Minimum supported server</span></span><br/> | <span data-ttu-id="2e8f2-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2e8f2-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2e8f2-155">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2e8f2-155">Namespace</span></span><br/>                | <span data-ttu-id="2e8f2-156">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2e8f2-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2e8f2-157">MOF</span><span class="sxs-lookup"><span data-stu-id="2e8f2-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e8f2-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e8f2-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e8f2-159">DLL</span><span class="sxs-lookup"><span data-stu-id="2e8f2-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e8f2-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e8f2-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e8f2-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e8f2-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e8f2-162">\_Файл CIM</span><span class="sxs-lookup"><span data-stu-id="2e8f2-162">CIM\_DataFile</span></span>](delete-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="2e8f2-163">**\_Файл CIM**</span><span class="sxs-lookup"><span data-stu-id="2e8f2-163">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="2e8f2-164">Задачи WMI: файлы и папки</span><span class="sxs-lookup"><span data-stu-id="2e8f2-164">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="2e8f2-165">**Константы прав доступа к файлам и каталогам**</span><span class="sxs-lookup"><span data-stu-id="2e8f2-165">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

