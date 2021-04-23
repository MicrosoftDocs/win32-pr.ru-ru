---
description: Удалите логический аудио-или видеофайловый кодек (или каталог), указанный в пути к объекту.
ms.assetid: df85c8a4-3be3-4bde-b36e-6bc8af6495a9
ms.tgt_platform: multiple
title: Метод Делетикс класса Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: df5527be497176f167ac368b872253fa3254a404
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895733"
---
# <a name="deleteex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="6153e-103">Метод Делетикс \_ класса Win32 кодекфиле</span><span class="sxs-lookup"><span data-stu-id="6153e-103">DeleteEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="6153e-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) делетикс удалит логический аудио-или видеокодек (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="6153e-104">The **DeleteEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method will delete the logical audio or video codec file (or directory) specified in the object path.</span></span> <span data-ttu-id="6153e-105">**Делетикс** — это расширенная версия метода [**Delete**](delete-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="6153e-105">**DeleteEx** is an extended version of the [**Delete**](delete-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="6153e-106">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="6153e-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6153e-107">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6153e-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6153e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6153e-108">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out] string StopFileName,
  [in]  String StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="6153e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6153e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6153e-110">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6153e-110">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6153e-111">Имя файла или каталога, в котором произошел сбой метода **делетикс** .</span><span class="sxs-lookup"><span data-stu-id="6153e-111">Name of the file or directory where the **DeleteEx** method failed.</span></span> <span data-ttu-id="6153e-112">Если метод завершится с ошибкой, этот параметр будет иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="6153e-112">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="6153e-113">*StartFileName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6153e-113">*StartFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6153e-114">Имя дочернего файла или каталога, который будет использоваться в качестве отправной точки для **делетикс**.</span><span class="sxs-lookup"><span data-stu-id="6153e-114">Names the child file or directory to use as a starting point for **DeleteEx**.</span></span> <span data-ttu-id="6153e-115">Параметр *StartFileName* обычно представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="6153e-115">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="6153e-116">Если этот параметр имеет **значение NULL**, операция выполняется над файлом или каталогом, указанным в вызове метода **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="6153e-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span> <span data-ttu-id="6153e-117">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6153e-117">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6153e-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6153e-118">Return value</span></span>

<span data-ttu-id="6153e-119">Возвращает целочисленное значение 0 (ноль), если файл был успешно удален, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="6153e-119">Returns an integer value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="6153e-120">**0**</span><span class="sxs-lookup"><span data-stu-id="6153e-120">**0**</span></span>
</dt> <dd>

<span data-ttu-id="6153e-121">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="6153e-121">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="6153e-122">**2**</span><span class="sxs-lookup"><span data-stu-id="6153e-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="6153e-123">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="6153e-123">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="6153e-124">**8**</span><span class="sxs-lookup"><span data-stu-id="6153e-124">**8**</span></span>
</dt> <dd>

<span data-ttu-id="6153e-125">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="6153e-125">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="6153e-126">**9**</span><span class="sxs-lookup"><span data-stu-id="6153e-126">**9**</span></span>
</dt> <dd>

<span data-ttu-id="6153e-127">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="6153e-127">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6153e-128">**10**</span><span class="sxs-lookup"><span data-stu-id="6153e-128">**10**</span></span>
</dt> <dd>

<span data-ttu-id="6153e-129">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="6153e-129">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="6153e-130">**11**</span><span class="sxs-lookup"><span data-stu-id="6153e-130">**11**</span></span>
</dt> <dd>

<span data-ttu-id="6153e-131">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="6153e-131">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="6153e-132">**12**</span><span class="sxs-lookup"><span data-stu-id="6153e-132">**12**</span></span>
</dt> <dd>

<span data-ttu-id="6153e-133">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="6153e-133">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="6153e-134">**13**</span><span class="sxs-lookup"><span data-stu-id="6153e-134">**13**</span></span>
</dt> <dd>

<span data-ttu-id="6153e-135">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="6153e-135">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="6153e-136">**14**</span><span class="sxs-lookup"><span data-stu-id="6153e-136">**14**</span></span>
</dt> <dd>

<span data-ttu-id="6153e-137">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="6153e-137">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="6153e-138">**15**</span><span class="sxs-lookup"><span data-stu-id="6153e-138">**15**</span></span>
</dt> <dd>

<span data-ttu-id="6153e-139">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="6153e-139">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="6153e-140">**16**</span><span class="sxs-lookup"><span data-stu-id="6153e-140">**16**</span></span>
</dt> <dd>

<span data-ttu-id="6153e-141">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="6153e-141">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6153e-142">**17**</span><span class="sxs-lookup"><span data-stu-id="6153e-142">**17**</span></span>
</dt> <dd>

<span data-ttu-id="6153e-143">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="6153e-143">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="6153e-144">**открыт**</span><span class="sxs-lookup"><span data-stu-id="6153e-144">**21**</span></span>
</dt> <dd>

<span data-ttu-id="6153e-145">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="6153e-145">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6153e-146">Требования</span><span class="sxs-lookup"><span data-stu-id="6153e-146">Requirements</span></span>



| <span data-ttu-id="6153e-147">Требование</span><span class="sxs-lookup"><span data-stu-id="6153e-147">Requirement</span></span> | <span data-ttu-id="6153e-148">Значение</span><span class="sxs-lookup"><span data-stu-id="6153e-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6153e-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6153e-149">Minimum supported client</span></span><br/> | <span data-ttu-id="6153e-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6153e-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6153e-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6153e-151">Minimum supported server</span></span><br/> | <span data-ttu-id="6153e-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6153e-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6153e-153">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6153e-153">Namespace</span></span><br/>                | <span data-ttu-id="6153e-154">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6153e-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6153e-155">MOF</span><span class="sxs-lookup"><span data-stu-id="6153e-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6153e-156"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6153e-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6153e-157">DLL</span><span class="sxs-lookup"><span data-stu-id="6153e-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6153e-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6153e-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6153e-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6153e-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="6153e-160">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6153e-160">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6153e-161">**\_Кодекфиле Win32**</span><span class="sxs-lookup"><span data-stu-id="6153e-161">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

