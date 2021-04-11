---
description: Использует сжатие NTFS для сжатия логического файла (или каталога), указанного в пути к объекту. Этот метод наследуется от CIM \_ LogicalFile.
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
ms.openlocfilehash: 070a15a0fb134c92e7c436e071e09b7cc09fa5dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262538"
---
# <a name="compressex-method-of-the-cim_datafile-class"></a><span data-ttu-id="3d476-104">Метод Компрессекс \_ класса CIM File</span><span class="sxs-lookup"><span data-stu-id="3d476-104">CompressEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="3d476-105">Метод **компрессекс** использует сжатие NTFS для сжатия логического файла (или каталога), указанного в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="3d476-105">The **CompressEx** method uses NTFS compression to compress the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="3d476-106">Этот метод наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="3d476-106">This method is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span> <span data-ttu-id="3d476-107">Этот метод является расширенной версией метода [**сжатия**](compress-method-in-class-cim-datafile.md) и наследуется от [CIM \_ LogicalFile](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3d476-107">This method is an extended version of the [**Compress**](compress-method-in-class-cim-datafile.md) method and is inherited from [CIM\_LogicalFile](/windows/desktop/WmiSdk/calling-a-method).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3d476-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="3d476-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3d476-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3d476-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3d476-110">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="3d476-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3d476-111">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="3d476-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3d476-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d476-112">Syntax</span></span>


```mof
uint32 CompressEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="3d476-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d476-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d476-114">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3d476-114">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d476-115">Строка, представляющая имя файла (или каталога), в котором произошел сбой метода.</span><span class="sxs-lookup"><span data-stu-id="3d476-115">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="3d476-116">Если метод выполнен, этот параметр имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="3d476-116">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="3d476-117">*StartFileName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3d476-117">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d476-118">Строка, представляющая дочерний файл (или каталог), используемый в качестве отправной точки для этого метода.</span><span class="sxs-lookup"><span data-stu-id="3d476-118">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="3d476-119">Как правило, параметр *StartFileName* — это параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="3d476-119">Typically, the *StartFileName* parameter is the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="3d476-120">Если этот параметр имеет значение null, операция выполняется над файлом или каталогом, указанным в вызове метода **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="3d476-120">If this parameter is null, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="3d476-121">Если используется параметр *StartFileName* , то для *рекурсии* необходимо также задать значение true.</span><span class="sxs-lookup"><span data-stu-id="3d476-121">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="3d476-122">*Рекурсивно* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3d476-122">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d476-123">Если **значение — true**, метод также применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**\_ файла данных CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="3d476-123">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="3d476-124">Для экземпляров файлов этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="3d476-124">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d476-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d476-125">Return value</span></span>

<span data-ttu-id="3d476-126">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="3d476-126">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="3d476-127">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="3d476-127">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3d476-128">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="3d476-128">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3d476-129">**0**</span><span class="sxs-lookup"><span data-stu-id="3d476-129">**0**</span></span>
</dt> <dd>

<span data-ttu-id="3d476-130">Успешно.</span><span class="sxs-lookup"><span data-stu-id="3d476-130">Success.</span></span>

</dd> <dt>

<span data-ttu-id="3d476-131">**2**</span><span class="sxs-lookup"><span data-stu-id="3d476-131">**2**</span></span>
</dt> <dd>

<span data-ttu-id="3d476-132">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="3d476-132">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="3d476-133">**8**</span><span class="sxs-lookup"><span data-stu-id="3d476-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="3d476-134">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="3d476-134">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="3d476-135">**9**</span><span class="sxs-lookup"><span data-stu-id="3d476-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="3d476-136">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="3d476-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="3d476-137">**10**</span><span class="sxs-lookup"><span data-stu-id="3d476-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="3d476-138">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="3d476-138">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3d476-139">**11**</span><span class="sxs-lookup"><span data-stu-id="3d476-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="3d476-140">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="3d476-140">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="3d476-141">**12**</span><span class="sxs-lookup"><span data-stu-id="3d476-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="3d476-142">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="3d476-142">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="3d476-143">**13**</span><span class="sxs-lookup"><span data-stu-id="3d476-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="3d476-144">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="3d476-144">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="3d476-145">**14**</span><span class="sxs-lookup"><span data-stu-id="3d476-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="3d476-146">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="3d476-146">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="3d476-147">**15**</span><span class="sxs-lookup"><span data-stu-id="3d476-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="3d476-148">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="3d476-148">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="3d476-149">**16**</span><span class="sxs-lookup"><span data-stu-id="3d476-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="3d476-150">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="3d476-150">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="3d476-151">**17**</span><span class="sxs-lookup"><span data-stu-id="3d476-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="3d476-152">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="3d476-152">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="3d476-153">**открыт**</span><span class="sxs-lookup"><span data-stu-id="3d476-153">**21**</span></span>
</dt> <dd>

<span data-ttu-id="3d476-154">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="3d476-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d476-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d476-155">Remarks</span></span>

<span data-ttu-id="3d476-156">Метод **компрессекс** в [**\_ файле CIM**](cim-datafile.md) реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="3d476-156">The **CompressEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="3d476-157">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="3d476-157">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3d476-158">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="3d476-158">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d476-159">Требования</span><span class="sxs-lookup"><span data-stu-id="3d476-159">Requirements</span></span>



| <span data-ttu-id="3d476-160">Требование</span><span class="sxs-lookup"><span data-stu-id="3d476-160">Requirement</span></span> | <span data-ttu-id="3d476-161">Значение</span><span class="sxs-lookup"><span data-stu-id="3d476-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d476-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d476-162">Minimum supported client</span></span><br/> | <span data-ttu-id="3d476-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d476-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d476-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d476-164">Minimum supported server</span></span><br/> | <span data-ttu-id="3d476-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d476-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d476-166">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3d476-166">Namespace</span></span><br/>                | <span data-ttu-id="3d476-167">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3d476-167">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3d476-168">MOF</span><span class="sxs-lookup"><span data-stu-id="3d476-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d476-169"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d476-169"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d476-170">DLL</span><span class="sxs-lookup"><span data-stu-id="3d476-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d476-171"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d476-171"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d476-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d476-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d476-173">\_Файл CIM</span><span class="sxs-lookup"><span data-stu-id="3d476-173">CIM\_DataFile</span></span>](compressex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="3d476-174">**\_Файл CIM**</span><span class="sxs-lookup"><span data-stu-id="3d476-174">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="3d476-175">Задачи WMI: файлы и папки</span><span class="sxs-lookup"><span data-stu-id="3d476-175">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="3d476-176">**Константы прав доступа к файлам и каталогам**</span><span class="sxs-lookup"><span data-stu-id="3d476-176">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

