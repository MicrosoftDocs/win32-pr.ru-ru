---
description: Распаковывает логический файл данных (или каталог), указанный в пути к объекту. Этот метод является расширенной версией метода uncompressия и наследуется от CIM \_ LogicalFile.
ms.assetid: 30b62930-1d4a-47c0-8b57-b460edb5dbd0
ms.tgt_platform: multiple
title: Метод Ункомпрессекс класса CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0d11585a834ecc357447394ce09b73698bf2de86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142541"
---
# <a name="uncompressex-method-of-the-cim_datafile-class"></a><span data-ttu-id="6339e-104">Метод Ункомпрессекс \_ класса CIM File</span><span class="sxs-lookup"><span data-stu-id="6339e-104">UncompressEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="6339e-105">Метод **ункомпрессекс** распаковывает логический файл данных (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="6339e-105">The **UncompressEx** method uncompresses the logical data file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="6339e-106">Этот метод является расширенной версией метода [**uncompressия**](uncompress-method-in-class-cim-datafile.md) и наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="6339e-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-cim-datafile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6339e-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="6339e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6339e-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6339e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6339e-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="6339e-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6339e-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6339e-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6339e-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6339e-111">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="6339e-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="6339e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6339e-113">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6339e-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6339e-114">Имя файла (или каталога), в котором произошел сбой метода.</span><span class="sxs-lookup"><span data-stu-id="6339e-114">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="6339e-115">Если метод выполнен, этот параметр имеет **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="6339e-115">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="6339e-116">*StartFileName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6339e-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6339e-117">Дочерний файл (или каталог) для использования в качестве отправной точки для этого метода.</span><span class="sxs-lookup"><span data-stu-id="6339e-117">Child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="6339e-118">Как правило, параметр *StartFileName* — это параметр *стопфиленаме* , указывающий файл (или каталог), в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="6339e-118">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="6339e-119">Если этот параметр имеет **значение NULL**, операция выполняется над файлом (или каталогом), указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="6339e-119">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

<span data-ttu-id="6339e-120">Если используется параметр *StartFileName* , то для *рекурсии* необходимо также задать значение true.</span><span class="sxs-lookup"><span data-stu-id="6339e-120">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="6339e-121">*Рекурсивно* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6339e-121">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6339e-122">Если **значение — true**, метод также применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**\_ файла данных CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="6339e-122">If **TRUE**, the method is also applied recursively to files and directories within the directory that is specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="6339e-123">Для экземпляров файлов этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="6339e-123">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6339e-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6339e-124">Return value</span></span>

<span data-ttu-id="6339e-125">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="6339e-125">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="6339e-126">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="6339e-126">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="6339e-127">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="6339e-127">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="6339e-128">**0**</span><span class="sxs-lookup"><span data-stu-id="6339e-128">**0**</span></span>
</dt> <dd>

<span data-ttu-id="6339e-129">Успешно.</span><span class="sxs-lookup"><span data-stu-id="6339e-129">Success.</span></span>

</dd> <dt>

<span data-ttu-id="6339e-130">**2**</span><span class="sxs-lookup"><span data-stu-id="6339e-130">**2**</span></span>
</dt> <dd>

<span data-ttu-id="6339e-131">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="6339e-131">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="6339e-132">**8**</span><span class="sxs-lookup"><span data-stu-id="6339e-132">**8**</span></span>
</dt> <dd>

<span data-ttu-id="6339e-133">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="6339e-133">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="6339e-134">**9**</span><span class="sxs-lookup"><span data-stu-id="6339e-134">**9**</span></span>
</dt> <dd>

<span data-ttu-id="6339e-135">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="6339e-135">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="6339e-136">**10**</span><span class="sxs-lookup"><span data-stu-id="6339e-136">**10**</span></span>
</dt> <dd>

<span data-ttu-id="6339e-137">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="6339e-137">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="6339e-138">**11**</span><span class="sxs-lookup"><span data-stu-id="6339e-138">**11**</span></span>
</dt> <dd>

<span data-ttu-id="6339e-139">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="6339e-139">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="6339e-140">**12**</span><span class="sxs-lookup"><span data-stu-id="6339e-140">**12**</span></span>
</dt> <dd>

<span data-ttu-id="6339e-141">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="6339e-141">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="6339e-142">**13**</span><span class="sxs-lookup"><span data-stu-id="6339e-142">**13**</span></span>
</dt> <dd>

<span data-ttu-id="6339e-143">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="6339e-143">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="6339e-144">**14**</span><span class="sxs-lookup"><span data-stu-id="6339e-144">**14**</span></span>
</dt> <dd>

<span data-ttu-id="6339e-145">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="6339e-145">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="6339e-146">**15**</span><span class="sxs-lookup"><span data-stu-id="6339e-146">**15**</span></span>
</dt> <dd>

<span data-ttu-id="6339e-147">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="6339e-147">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="6339e-148">**16**</span><span class="sxs-lookup"><span data-stu-id="6339e-148">**16**</span></span>
</dt> <dd>

<span data-ttu-id="6339e-149">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="6339e-149">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="6339e-150">**17**</span><span class="sxs-lookup"><span data-stu-id="6339e-150">**17**</span></span>
</dt> <dd>

<span data-ttu-id="6339e-151">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="6339e-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="6339e-152">**открыт**</span><span class="sxs-lookup"><span data-stu-id="6339e-152">**21**</span></span>
</dt> <dd>

<span data-ttu-id="6339e-153">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="6339e-153">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6339e-154">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6339e-154">Remarks</span></span>

<span data-ttu-id="6339e-155">Метод **ункомпрессекс** в [**\_ файле CIM**](cim-datafile.md) реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="6339e-155">The **UncompressEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="6339e-156">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="6339e-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6339e-157">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="6339e-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6339e-158">Требования</span><span class="sxs-lookup"><span data-stu-id="6339e-158">Requirements</span></span>



| <span data-ttu-id="6339e-159">Требование</span><span class="sxs-lookup"><span data-stu-id="6339e-159">Requirement</span></span> | <span data-ttu-id="6339e-160">Значение</span><span class="sxs-lookup"><span data-stu-id="6339e-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6339e-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6339e-161">Minimum supported client</span></span><br/> | <span data-ttu-id="6339e-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6339e-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6339e-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6339e-163">Minimum supported server</span></span><br/> | <span data-ttu-id="6339e-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6339e-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6339e-165">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6339e-165">Namespace</span></span><br/>                | <span data-ttu-id="6339e-166">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6339e-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6339e-167">MOF</span><span class="sxs-lookup"><span data-stu-id="6339e-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6339e-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6339e-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6339e-169">DLL</span><span class="sxs-lookup"><span data-stu-id="6339e-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6339e-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6339e-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6339e-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6339e-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6339e-172">**\_Файл CIM**</span><span class="sxs-lookup"><span data-stu-id="6339e-172">**CIM\_DataFile**</span></span>](uncompressex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="6339e-173">**\_Файл CIM**</span><span class="sxs-lookup"><span data-stu-id="6339e-173">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="6339e-174">Задачи WMI: файлы и папки</span><span class="sxs-lookup"><span data-stu-id="6339e-174">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="6339e-175">**Константы прав доступа к файлам и каталогам**</span><span class="sxs-lookup"><span data-stu-id="6339e-175">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

