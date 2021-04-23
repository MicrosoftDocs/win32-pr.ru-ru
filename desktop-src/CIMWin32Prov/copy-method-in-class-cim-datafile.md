---
description: Метод Copy копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное параметром input.
ms.assetid: 13bd7da8-a562-414b-8d23-6f58e1c55878
ms.tgt_platform: multiple
title: Метод Copy класса CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c126f1cd54470e50a700fdea1c121776d687a9dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655902"
---
# <a name="copy-method-of-the-cim_datafile-class"></a><span data-ttu-id="ff246-103">Метод Copy \_ класса CIM File</span><span class="sxs-lookup"><span data-stu-id="ff246-103">Copy method of the CIM\_DataFile class</span></span>

<span data-ttu-id="ff246-104">Метод **Copy** копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное параметром input.</span><span class="sxs-lookup"><span data-stu-id="ff246-104">The **Copy** method copies the logical file (or directory) that is specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="ff246-105">Копирование не поддерживается, если требуется перезапись существующего логического файла.</span><span class="sxs-lookup"><span data-stu-id="ff246-105">A copy is not supported if it requires overwriting an existing logical file.</span></span> <span data-ttu-id="ff246-106">Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="ff246-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff246-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="ff246-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ff246-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ff246-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ff246-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="ff246-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ff246-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ff246-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ff246-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff246-111">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="ff246-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff246-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff246-113">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff246-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff246-114">Полное имя целевого файла (или каталога).</span><span class="sxs-lookup"><span data-stu-id="ff246-114">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="ff246-115">Пример: "c: \\ temp \\ невдиректори"</span><span class="sxs-lookup"><span data-stu-id="ff246-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff246-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff246-116">Return value</span></span>

<span data-ttu-id="ff246-117">Возвращает значение 0 в случае успешного выполнения и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="ff246-117">Returns a value of 0 on success, and any other number to indicate an error.</span></span> <span data-ttu-id="ff246-118">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ff246-118">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ff246-119">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ff246-119">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ff246-120">**0**</span><span class="sxs-lookup"><span data-stu-id="ff246-120">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ff246-121">Успешно.</span><span class="sxs-lookup"><span data-stu-id="ff246-121">Success.</span></span>

</dd> <dt>

<span data-ttu-id="ff246-122">**2**</span><span class="sxs-lookup"><span data-stu-id="ff246-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ff246-123">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="ff246-123">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="ff246-124">**8**</span><span class="sxs-lookup"><span data-stu-id="ff246-124">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ff246-125">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="ff246-125">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="ff246-126">**9**</span><span class="sxs-lookup"><span data-stu-id="ff246-126">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ff246-127">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="ff246-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="ff246-128">**10**</span><span class="sxs-lookup"><span data-stu-id="ff246-128">**10**</span></span>
</dt> <dd>

<span data-ttu-id="ff246-129">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="ff246-129">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ff246-130">**11**</span><span class="sxs-lookup"><span data-stu-id="ff246-130">**11**</span></span>
</dt> <dd>

<span data-ttu-id="ff246-131">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="ff246-131">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="ff246-132">**12**</span><span class="sxs-lookup"><span data-stu-id="ff246-132">**12**</span></span>
</dt> <dd>

<span data-ttu-id="ff246-133">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="ff246-133">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="ff246-134">**13**</span><span class="sxs-lookup"><span data-stu-id="ff246-134">**13**</span></span>
</dt> <dd>

<span data-ttu-id="ff246-135">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="ff246-135">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="ff246-136">**14**</span><span class="sxs-lookup"><span data-stu-id="ff246-136">**14**</span></span>
</dt> <dd>

<span data-ttu-id="ff246-137">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="ff246-137">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="ff246-138">**15**</span><span class="sxs-lookup"><span data-stu-id="ff246-138">**15**</span></span>
</dt> <dd>

<span data-ttu-id="ff246-139">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="ff246-139">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="ff246-140">**16**</span><span class="sxs-lookup"><span data-stu-id="ff246-140">**16**</span></span>
</dt> <dd>

<span data-ttu-id="ff246-141">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="ff246-141">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="ff246-142">**17**</span><span class="sxs-lookup"><span data-stu-id="ff246-142">**17**</span></span>
</dt> <dd>

<span data-ttu-id="ff246-143">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="ff246-143">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="ff246-144">**открыт**</span><span class="sxs-lookup"><span data-stu-id="ff246-144">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ff246-145">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="ff246-145">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff246-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff246-146">Remarks</span></span>

<span data-ttu-id="ff246-147">Метод **Copy** в [**\_ файле CIM**](cim-datafile.md) реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="ff246-147">The **Copy** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="ff246-148">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="ff246-148">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ff246-149">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="ff246-149">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff246-150">Требования</span><span class="sxs-lookup"><span data-stu-id="ff246-150">Requirements</span></span>



| <span data-ttu-id="ff246-151">Требование</span><span class="sxs-lookup"><span data-stu-id="ff246-151">Requirement</span></span> | <span data-ttu-id="ff246-152">Значение</span><span class="sxs-lookup"><span data-stu-id="ff246-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff246-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff246-153">Minimum supported client</span></span><br/> | <span data-ttu-id="ff246-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff246-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ff246-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff246-155">Minimum supported server</span></span><br/> | <span data-ttu-id="ff246-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff246-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ff246-157">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ff246-157">Namespace</span></span><br/>                | <span data-ttu-id="ff246-158">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ff246-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ff246-159">MOF</span><span class="sxs-lookup"><span data-stu-id="ff246-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff246-160"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ff246-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff246-161">DLL</span><span class="sxs-lookup"><span data-stu-id="ff246-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff246-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff246-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff246-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff246-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff246-164">\_Файл CIM</span><span class="sxs-lookup"><span data-stu-id="ff246-164">CIM\_DataFile</span></span>](copy-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="ff246-165">**\_Файл CIM**</span><span class="sxs-lookup"><span data-stu-id="ff246-165">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="ff246-166">Задачи WMI: файлы и папки</span><span class="sxs-lookup"><span data-stu-id="ff246-166">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="ff246-167">**Константы прав доступа к файлам и каталогам**</span><span class="sxs-lookup"><span data-stu-id="ff246-167">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

