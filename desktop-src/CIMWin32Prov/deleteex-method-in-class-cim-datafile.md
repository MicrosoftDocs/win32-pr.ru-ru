---
description: Метод Делетикс удаляет логический файл (или каталог), указанный в пути к объекту. Этот метод является расширенной версией метода Delete и наследуется от CIM \_ LogicalFile.
ms.assetid: 565d604f-01e0-4cd4-b182-9750c58bae5f
ms.tgt_platform: multiple
title: Метод Делетикс класса CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9af120c76e4ab8c53c945bd13aa62a2295385ac2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141339"
---
# <a name="deleteex-method-of-the-cim_datafile-class"></a><span data-ttu-id="2be97-104">Метод Делетикс \_ класса CIM File</span><span class="sxs-lookup"><span data-stu-id="2be97-104">DeleteEx method of the CIM\_DataFile class</span></span>

<span data-ttu-id="2be97-105">Метод **делетикс** удаляет логический файл (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="2be97-105">The **DeleteEx** method deletes the logical file (or directory) that is specified in the object path.</span></span> <span data-ttu-id="2be97-106">Этот метод является расширенной версией метода [**Delete**](delete-method-in-class-cim-datafile.md) и наследуется от [**CIM \_ LogicalFile**](cim-logicalfile.md).</span><span class="sxs-lookup"><span data-stu-id="2be97-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-datafile.md) method and is inherited from [**CIM\_LogicalFile**](cim-logicalfile.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2be97-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="2be97-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2be97-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2be97-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2be97-109">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="2be97-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2be97-110">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="2be97-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2be97-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2be97-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="2be97-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="2be97-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2be97-113">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2be97-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2be97-114">Строка, представляющая имя файла (или каталога), в котором произошел сбой метода.</span><span class="sxs-lookup"><span data-stu-id="2be97-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="2be97-115">Если метод выполнен, этот параметр имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="2be97-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="2be97-116">*StartFileName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2be97-116">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2be97-117">Строка, представляющая дочерний файл (или каталог), используемый в качестве отправной точки для этого метода.</span><span class="sxs-lookup"><span data-stu-id="2be97-117">String that represents the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="2be97-118">Как правило, параметр *StartFileName* — это параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="2be97-118">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="2be97-119">Если этот параметр имеет значение null, операция выполняется над файлом (или каталогом), указанным в вызове метода [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="2be97-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2be97-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2be97-120">Return value</span></span>

<span data-ttu-id="2be97-121">Возвращает значение 0 (нуль) при успешном выполнении и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="2be97-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="2be97-122">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="2be97-122">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2be97-123">Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="2be97-123">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="2be97-124">0</span><span class="sxs-lookup"><span data-stu-id="2be97-124">0</span></span>

<span data-ttu-id="2be97-125">Успешно.</span><span class="sxs-lookup"><span data-stu-id="2be97-125">Success.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2be97-126">2</span><span class="sxs-lookup"><span data-stu-id="2be97-126">2</span></span>

<span data-ttu-id="2be97-127">Доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="2be97-127">Access denied.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2be97-128">8</span><span class="sxs-lookup"><span data-stu-id="2be97-128">8</span></span>

<span data-ttu-id="2be97-129">Неопределенный сбой.</span><span class="sxs-lookup"><span data-stu-id="2be97-129">Unspecified failure.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2be97-130">9</span><span class="sxs-lookup"><span data-stu-id="2be97-130">9</span></span>

<span data-ttu-id="2be97-131">Недопустимый объект.</span><span class="sxs-lookup"><span data-stu-id="2be97-131">Invalid object.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2be97-132">10</span><span class="sxs-lookup"><span data-stu-id="2be97-132">10</span></span>

<span data-ttu-id="2be97-133">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="2be97-133">Object already exists.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2be97-134">11</span><span class="sxs-lookup"><span data-stu-id="2be97-134">11</span></span>

<span data-ttu-id="2be97-135">Файловая система не NTFS.</span><span class="sxs-lookup"><span data-stu-id="2be97-135">File system not NTFS.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2be97-136">12</span><span class="sxs-lookup"><span data-stu-id="2be97-136">12</span></span>

<span data-ttu-id="2be97-137">Платформа не Windows.</span><span class="sxs-lookup"><span data-stu-id="2be97-137">Platform not Windows.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2be97-138">13</span><span class="sxs-lookup"><span data-stu-id="2be97-138">13</span></span>

<span data-ttu-id="2be97-139">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="2be97-139">Drive not the same.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2be97-140">14</span><span class="sxs-lookup"><span data-stu-id="2be97-140">14</span></span>

<span data-ttu-id="2be97-141">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="2be97-141">Directory not empty.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2be97-142">15</span><span class="sxs-lookup"><span data-stu-id="2be97-142">15</span></span>

<span data-ttu-id="2be97-143">Нарушение правил общего доступа.</span><span class="sxs-lookup"><span data-stu-id="2be97-143">Sharing violation.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2be97-144">16</span><span class="sxs-lookup"><span data-stu-id="2be97-144">16</span></span>

<span data-ttu-id="2be97-145">Недопустимый начальный файл.</span><span class="sxs-lookup"><span data-stu-id="2be97-145">Invalid start file.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2be97-146">17</span><span class="sxs-lookup"><span data-stu-id="2be97-146">17</span></span>

<span data-ttu-id="2be97-147">Привилегия не удерживается.</span><span class="sxs-lookup"><span data-stu-id="2be97-147">Privilege not held.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="2be97-148">21</span><span class="sxs-lookup"><span data-stu-id="2be97-148">21</span></span>

<span data-ttu-id="2be97-149">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="2be97-149">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2be97-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2be97-150">Remarks</span></span>

<span data-ttu-id="2be97-151">Метод **делетикс** в [**\_ файле CIM**](cim-datafile.md) реализуется инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="2be97-151">The **DeleteEx** method in [**CIM\_DataFile**](cim-datafile.md) is implemented by WMI.</span></span>

<span data-ttu-id="2be97-152">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="2be97-152">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2be97-153">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="2be97-153">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2be97-154">Требования</span><span class="sxs-lookup"><span data-stu-id="2be97-154">Requirements</span></span>



| <span data-ttu-id="2be97-155">Требование</span><span class="sxs-lookup"><span data-stu-id="2be97-155">Requirement</span></span> | <span data-ttu-id="2be97-156">Значение</span><span class="sxs-lookup"><span data-stu-id="2be97-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2be97-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2be97-157">Minimum supported client</span></span><br/> | <span data-ttu-id="2be97-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2be97-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2be97-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2be97-159">Minimum supported server</span></span><br/> | <span data-ttu-id="2be97-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2be97-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2be97-161">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2be97-161">Namespace</span></span><br/>                | <span data-ttu-id="2be97-162">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2be97-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2be97-163">MOF</span><span class="sxs-lookup"><span data-stu-id="2be97-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2be97-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2be97-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2be97-165">DLL</span><span class="sxs-lookup"><span data-stu-id="2be97-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2be97-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2be97-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2be97-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2be97-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2be97-168">\_Файл CIM</span><span class="sxs-lookup"><span data-stu-id="2be97-168">CIM\_DataFile</span></span>](deleteex-method-in-class-cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="2be97-169">**\_Файл CIM**</span><span class="sxs-lookup"><span data-stu-id="2be97-169">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dt>

[<span data-ttu-id="2be97-170">Задачи WMI: файлы и папки</span><span class="sxs-lookup"><span data-stu-id="2be97-170">WMI Tasks: Files and Folders</span></span>](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[<span data-ttu-id="2be97-171">**Константы прав доступа к файлам и каталогам**</span><span class="sxs-lookup"><span data-stu-id="2be97-171">**File and Directory Access Rights Constants**</span></span>](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

