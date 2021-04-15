---
description: Метод Копекс копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное параметром FileName.
ms.assetid: e52c1a0f-e34c-4a61-9e54-ed172976cb61
ms.tgt_platform: multiple
title: Метод Копекс класса CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a83f1556aeeafbb5cc95eddbd84806bdaef0be14
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655897"
---
# <a name="copyex-method-of-the-cim_datafile-class"></a><span data-ttu-id="b4f4a-103">Метод Копекс \_ класса CIM File</span><span class="sxs-lookup"><span data-stu-id="b4f4a-103">CopyEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="b4f4a-104">Метод **копекс** копирует логический файл (или каталог), указанный в пути к объекту, в расположение, указанное параметром *filename* .</span><span class="sxs-lookup"><span data-stu-id="b4f4a-104">The **CopyEx** method copies the logical file (or directory) that is specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="b4f4a-105">Копирование не поддерживается, если требуется перезапись существующего логического файла.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-105">A copy is not supported if it requires overwriting an existing logical file.</span></span> <span data-ttu-id="b4f4a-106">Этот метод является расширенной версией метода [**Copy**](copy-method-in-class-cim-datafile.md) и наследуется от [CIM \_ LogicalFile](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="b4f4a-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-datafile.md) method and is inherited from [CIM\_LogicalFile](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b4f4a-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b4f4a-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b4f4a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b4f4a-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="b4f4a-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b4f4a-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b4f4a-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b4f4a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4f4a-111">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]  string     FileName,
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="b4f4a-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4f4a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4f4a-113">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4f4a-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f4a-114">Полное имя целевого файла (или каталога).</span><span class="sxs-lookup"><span data-stu-id="b4f4a-114">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="b4f4a-115">Пример: "c: \\ temp \\ невдиректори"</span><span class="sxs-lookup"><span data-stu-id="b4f4a-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="b4f4a-116">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b4f4a-116">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f4a-117">Строка, представляющая имя файла (или каталога), в котором произошел сбой метода.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-117">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="b4f4a-118">Если метод завершится с ошибкой, этот параметр будет иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="b4f4a-118">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="b4f4a-119">*StartFileName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4f4a-119">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f4a-120">Строка, представляющая дочерний файл (или каталог), используемый в качестве отправной точки для этого метода.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-120">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="b4f4a-121">Как правило, параметр *StartFileName* — это параметр *стопфиленаме* , указывающий файл (или каталог), в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-121">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="b4f4a-122">Если этот параметр имеет **значение NULL**, операция выполняется над файлом (или каталогом), указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="b4f4a-122">If this parameter is **null**, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

<span data-ttu-id="b4f4a-123">Если используется параметр *StartFileName* , то для *рекурсии* необходимо также задать значение true.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-123">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="b4f4a-124">*Рекурсивно* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4f4a-124">*Recursive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f4a-125">Если значение — TRUE, метод также применяется рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**\_ файла данных CIM**](cim-datafile.md) .</span><span class="sxs-lookup"><span data-stu-id="b4f4a-125">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_DataFile**](cim-datafile.md) instance.</span></span> <span data-ttu-id="b4f4a-126">Для экземпляров файлов этот параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-126">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4f4a-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4f4a-127">Return value</span></span>

<span data-ttu-id="b4f4a-128">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-128">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="b4f4a-129">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b4f4a-129">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b4f4a-130">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b4f4a-130">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="b4f4a-131">0</span><span class="sxs-lookup"><span data-stu-id="b4f4a-131">0</span></span>

<span data-ttu-id="b4f4a-132">Успешно.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-132">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b4f4a-133">2</span><span class="sxs-lookup"><span data-stu-id="b4f4a-133">2</span></span>

<span data-ttu-id="b4f4a-134">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-134">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b4f4a-135">8</span><span class="sxs-lookup"><span data-stu-id="b4f4a-135">8</span></span>

<span data-ttu-id="b4f4a-136">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-136">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b4f4a-137">9</span><span class="sxs-lookup"><span data-stu-id="b4f4a-137">9</span></span>

<span data-ttu-id="b4f4a-138">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-138">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b4f4a-139">10</span><span class="sxs-lookup"><span data-stu-id="b4f4a-139">10</span></span>

<span data-ttu-id="b4f4a-140">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-140">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b4f4a-141">11</span><span class="sxs-lookup"><span data-stu-id="b4f4a-141">11</span></span>

<span data-ttu-id="b4f4a-142">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-142">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b4f4a-143">12</span><span class="sxs-lookup"><span data-stu-id="b4f4a-143">12</span></span>

<span data-ttu-id="b4f4a-144">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-144">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b4f4a-145">13</span><span class="sxs-lookup"><span data-stu-id="b4f4a-145">13</span></span>

<span data-ttu-id="b4f4a-146">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-146">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b4f4a-147">14</span><span class="sxs-lookup"><span data-stu-id="b4f4a-147">14</span></span>

<span data-ttu-id="b4f4a-148">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-148">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b4f4a-149">15</span><span class="sxs-lookup"><span data-stu-id="b4f4a-149">15</span></span>

<span data-ttu-id="b4f4a-150">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-150">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b4f4a-151">16</span><span class="sxs-lookup"><span data-stu-id="b4f4a-151">16</span></span>

<span data-ttu-id="b4f4a-152">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-152">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b4f4a-153">17</span><span class="sxs-lookup"><span data-stu-id="b4f4a-153">17</span></span>

<span data-ttu-id="b4f4a-154">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-154">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="b4f4a-155">21</span><span class="sxs-lookup"><span data-stu-id="b4f4a-155">21</span></span>

<span data-ttu-id="b4f4a-156">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-156">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4f4a-157">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4f4a-157">Remarks</span></span>

<span data-ttu-id="b4f4a-158">Метод **копекс** в [**\_ файле CIM**](cim-datafile.md) реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-158">The **CopyEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="b4f4a-159">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-159">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b4f4a-160">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="b4f4a-160">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4f4a-161">Требования</span><span class="sxs-lookup"><span data-stu-id="b4f4a-161">Requirements</span></span>



| <span data-ttu-id="b4f4a-162">Требование</span><span class="sxs-lookup"><span data-stu-id="b4f4a-162">Requirement</span></span> | <span data-ttu-id="b4f4a-163">Значение</span><span class="sxs-lookup"><span data-stu-id="b4f4a-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f4a-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4f4a-164">Minimum supported client</span></span><br/> | <span data-ttu-id="b4f4a-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4f4a-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b4f4a-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4f4a-166">Minimum supported server</span></span><br/> | <span data-ttu-id="b4f4a-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4f4a-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b4f4a-168">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b4f4a-168">Namespace</span></span><br/>                | <span data-ttu-id="b4f4a-169">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b4f4a-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b4f4a-170">MOF</span><span class="sxs-lookup"><span data-stu-id="b4f4a-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4f4a-171"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4f4a-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4f4a-172">DLL</span><span class="sxs-lookup"><span data-stu-id="b4f4a-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4f4a-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4f4a-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4f4a-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4f4a-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4f4a-175">**\_Файл CIM**</span><span class="sxs-lookup"><span data-stu-id="b4f4a-175">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="b4f4a-176">Задачи WMI: файлы и папки</span><span class="sxs-lookup"><span data-stu-id="b4f4a-176">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="b4f4a-177">**Константы прав доступа к файлам и каталогам**</span><span class="sxs-lookup"><span data-stu-id="b4f4a-177">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

