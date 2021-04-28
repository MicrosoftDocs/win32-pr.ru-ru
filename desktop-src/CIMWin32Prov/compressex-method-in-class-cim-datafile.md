---
description: Метод Компрессекс класса CIM_DataFile — использует сжатие NTFS для сжатия логического файла (или каталога), указанного в пути к объекту. Этот метод наследуется от CIM \_ LogicalFile.
ms.assetid: 553b6a90-d16c-4abb-9015-66fe8e1606f6
ms.tgt_platform: multiple
title: Метод Компрессекс класса CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccc155c04c6c25f38050bd37827eb0c2e2e0e73e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089792"
---
# <a name="compressex-method-of-the-cim_datafile-class"></a><span data-ttu-id="97b38-104">Метод Компрессекс \_ класса CIM File</span><span class="sxs-lookup"><span data-stu-id="97b38-104">CompressEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="97b38-105">Метод **компрессекс** использует сжатие NTFS для сжатия логического файла (или каталога), указанного в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="97b38-105">The **CompressEx** method uses NTFS compression to compress the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="97b38-106">Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="97b38-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="97b38-107">Этот метод является расширенной версией метода [**сжатия**](compress-method-in-class-cim-datafile.md) и наследуется от [CIM \_ LogicalFile](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="97b38-107">This method is an extended version of the [**Compress**](compress-method-in-class-cim-datafile.md) method and is inherited from [CIM\_LogicalFile](/windows/desktop/WmiSdk/calling-a-method).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="97b38-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="97b38-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="97b38-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="97b38-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="97b38-110">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="97b38-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="97b38-111">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="97b38-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="97b38-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97b38-112">Syntax</span></span>


```mof
uint32 CompressEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="97b38-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="97b38-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97b38-114">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="97b38-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97b38-115">Строка, представляющая имя файла (или каталога), в котором произошел сбой метода.</span><span class="sxs-lookup"><span data-stu-id="97b38-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="97b38-116">Если метод выполнен, этот параметр имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="97b38-116">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="97b38-117">*StartFileName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="97b38-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97b38-118">Строка, представляющая дочерний файл (или каталог), используемый в качестве отправной точки для этого метода.</span><span class="sxs-lookup"><span data-stu-id="97b38-118">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="97b38-119">Как правило, параметр *StartFileName* — это параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="97b38-119">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="97b38-120">Если этот параметр имеет значение null, операция выполняется над файлом или каталогом, указанным в вызове метода **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="97b38-120">If this parameter is null, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="97b38-121">Если используется параметр *StartFileName* , то для *рекурсии* необходимо также задать значение true.</span><span class="sxs-lookup"><span data-stu-id="97b38-121">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="97b38-122">*Рекурсивно* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="97b38-122">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97b38-123">Если **значение — true**, метод также применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**\_ файла данных CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="97b38-123">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="97b38-124">Для экземпляров файлов этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="97b38-124">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97b38-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="97b38-125">Return value</span></span>

<span data-ttu-id="97b38-126">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="97b38-126">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="97b38-127">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="97b38-127">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="97b38-128">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="97b38-128">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="97b38-129">**0**</span><span class="sxs-lookup"><span data-stu-id="97b38-129">**0**</span></span>
</dt> <dd>

<span data-ttu-id="97b38-130">Успешно.</span><span class="sxs-lookup"><span data-stu-id="97b38-130">Success.</span></span>

</dd> <dt>

<span data-ttu-id="97b38-131">**2**</span><span class="sxs-lookup"><span data-stu-id="97b38-131">**2**</span></span>
</dt> <dd>

<span data-ttu-id="97b38-132">Access denied. (Недопустимое значение {значение_утверждения} для утверждения {имя_утверждения}. Доступ запрещен.)</span><span class="sxs-lookup"><span data-stu-id="97b38-132">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="97b38-133">**8**</span><span class="sxs-lookup"><span data-stu-id="97b38-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="97b38-134">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="97b38-134">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="97b38-135">**9**</span><span class="sxs-lookup"><span data-stu-id="97b38-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="97b38-136">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="97b38-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="97b38-137">**10**</span><span class="sxs-lookup"><span data-stu-id="97b38-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="97b38-138">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="97b38-138">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="97b38-139">**11**</span><span class="sxs-lookup"><span data-stu-id="97b38-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="97b38-140">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="97b38-140">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="97b38-141">**12**</span><span class="sxs-lookup"><span data-stu-id="97b38-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="97b38-142">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="97b38-142">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="97b38-143">**13**</span><span class="sxs-lookup"><span data-stu-id="97b38-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="97b38-144">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="97b38-144">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="97b38-145">**14**</span><span class="sxs-lookup"><span data-stu-id="97b38-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="97b38-146">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="97b38-146">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="97b38-147">**15**</span><span class="sxs-lookup"><span data-stu-id="97b38-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="97b38-148">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="97b38-148">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="97b38-149">**16**</span><span class="sxs-lookup"><span data-stu-id="97b38-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="97b38-150">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="97b38-150">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="97b38-151">**17**</span><span class="sxs-lookup"><span data-stu-id="97b38-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="97b38-152">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="97b38-152">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="97b38-153">**открыт**</span><span class="sxs-lookup"><span data-stu-id="97b38-153">**21**</span></span>
</dt> <dd>

<span data-ttu-id="97b38-154">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="97b38-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97b38-155">Remarks</span><span class="sxs-lookup"><span data-stu-id="97b38-155">Remarks</span></span>

<span data-ttu-id="97b38-156">Метод **компрессекс** в [**\_ файле CIM**](cim-datafile.md) реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="97b38-156">The **CompressEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="97b38-157">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="97b38-157">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="97b38-158">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="97b38-158">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="97b38-159">Требования</span><span class="sxs-lookup"><span data-stu-id="97b38-159">Requirements</span></span>



| <span data-ttu-id="97b38-160">Требование</span><span class="sxs-lookup"><span data-stu-id="97b38-160">Requirement</span></span> | <span data-ttu-id="97b38-161">Значение</span><span class="sxs-lookup"><span data-stu-id="97b38-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97b38-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97b38-162">Minimum supported client</span></span><br/> | <span data-ttu-id="97b38-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97b38-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="97b38-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97b38-164">Minimum supported server</span></span><br/> | <span data-ttu-id="97b38-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97b38-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="97b38-166">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="97b38-166">Namespace</span></span><br/>                | <span data-ttu-id="97b38-167">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="97b38-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="97b38-168">MOF</span><span class="sxs-lookup"><span data-stu-id="97b38-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97b38-169"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97b38-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="97b38-170">DLL</span><span class="sxs-lookup"><span data-stu-id="97b38-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97b38-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97b38-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97b38-172">См. также</span><span class="sxs-lookup"><span data-stu-id="97b38-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97b38-173">\_Файл CIM</span><span class="sxs-lookup"><span data-stu-id="97b38-173">CIM\_DataFile</span></span>](compressex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="97b38-174">**\_Файл CIM**</span><span class="sxs-lookup"><span data-stu-id="97b38-174">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="97b38-175">Задачи WMI: файлы и папки</span><span class="sxs-lookup"><span data-stu-id="97b38-175">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="97b38-176">**Константы прав доступа к файлам и каталогам**</span><span class="sxs-lookup"><span data-stu-id="97b38-176">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

