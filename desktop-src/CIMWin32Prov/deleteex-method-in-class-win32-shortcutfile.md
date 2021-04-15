---
description: Удаляет логический файл ярлыка (или каталог), указанный в пути объекта.
ms.assetid: 278cd856-bb8d-4494-b43c-f0858366e136
ms.tgt_platform: multiple
title: Метод Делетикс класса Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bbe382ca57c4bdef36b19742313965c8bac68fd3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655807"
---
# <a name="deleteex-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="c9fa6-103">Метод Делетикс \_ класса Win32 шорткутфиле</span><span class="sxs-lookup"><span data-stu-id="c9fa6-103">DeleteEx method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="c9fa6-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) делетикс удаляет логический файл ярлыка (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="c9fa6-104">The **DeleteEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes the logical shortcut file (or directory) specified in the object path.</span></span> <span data-ttu-id="c9fa6-105">**Делетикс** — это расширенная версия метода [**Delete**](delete-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="c9fa6-105">**DeleteEx** is an extended version of the [**Delete**](delete-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="c9fa6-106">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="c9fa6-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c9fa6-107">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c9fa6-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c9fa6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9fa6-108">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="c9fa6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9fa6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9fa6-110">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c9fa6-110">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9fa6-111">Имя файла или каталога, в котором произошел сбой метода **делетикс** .</span><span class="sxs-lookup"><span data-stu-id="c9fa6-111">Name of the file or directory where the **DeleteEx** method failed.</span></span> <span data-ttu-id="c9fa6-112">Если метод выполнен, этот параметр имеет **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="c9fa6-112">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="c9fa6-113">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="c9fa6-113">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c9fa6-114">Имя дочернего файла или каталога, который будет использоваться в качестве отправной точки для **делетикс**.</span><span class="sxs-lookup"><span data-stu-id="c9fa6-114">Names the child file or directory to use as a starting point for **DeleteEx**.</span></span> <span data-ttu-id="c9fa6-115">Параметр *StartFileName* обычно представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="c9fa6-115">The *StartFileName* parameter is typically the *StopFileName* parameter that specifies the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="c9fa6-116">Если этот параметр имеет **значение NULL**, операция выполняется над файлом или каталогом, указанным в вызове метода ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="c9fa6-116">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9fa6-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9fa6-117">Return value</span></span>

<span data-ttu-id="c9fa6-118">Возвращает значение 0 (нуль), если файл был успешно удален, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="c9fa6-118">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="c9fa6-119">**0**</span><span class="sxs-lookup"><span data-stu-id="c9fa6-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c9fa6-120">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="c9fa6-120">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="c9fa6-121">**2**</span><span class="sxs-lookup"><span data-stu-id="c9fa6-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c9fa6-122">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="c9fa6-122">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="c9fa6-123">**8**</span><span class="sxs-lookup"><span data-stu-id="c9fa6-123">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c9fa6-124">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c9fa6-124">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c9fa6-125">**9**</span><span class="sxs-lookup"><span data-stu-id="c9fa6-125">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c9fa6-126">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="c9fa6-126">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c9fa6-127">**10**</span><span class="sxs-lookup"><span data-stu-id="c9fa6-127">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c9fa6-128">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="c9fa6-128">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c9fa6-129">**11**</span><span class="sxs-lookup"><span data-stu-id="c9fa6-129">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c9fa6-130">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="c9fa6-130">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="c9fa6-131">**12**</span><span class="sxs-lookup"><span data-stu-id="c9fa6-131">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c9fa6-132">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="c9fa6-132">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="c9fa6-133">**13**</span><span class="sxs-lookup"><span data-stu-id="c9fa6-133">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c9fa6-134">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="c9fa6-134">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="c9fa6-135">**14**</span><span class="sxs-lookup"><span data-stu-id="c9fa6-135">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c9fa6-136">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="c9fa6-136">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="c9fa6-137">**15**</span><span class="sxs-lookup"><span data-stu-id="c9fa6-137">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c9fa6-138">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="c9fa6-138">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="c9fa6-139">**16**</span><span class="sxs-lookup"><span data-stu-id="c9fa6-139">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c9fa6-140">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="c9fa6-140">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c9fa6-141">**17**</span><span class="sxs-lookup"><span data-stu-id="c9fa6-141">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c9fa6-142">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="c9fa6-142">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="c9fa6-143">**открыт**</span><span class="sxs-lookup"><span data-stu-id="c9fa6-143">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c9fa6-144">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="c9fa6-144">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9fa6-145">Требования</span><span class="sxs-lookup"><span data-stu-id="c9fa6-145">Requirements</span></span>



| <span data-ttu-id="c9fa6-146">Требование</span><span class="sxs-lookup"><span data-stu-id="c9fa6-146">Requirement</span></span> | <span data-ttu-id="c9fa6-147">Значение</span><span class="sxs-lookup"><span data-stu-id="c9fa6-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9fa6-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9fa6-148">Minimum supported client</span></span><br/> | <span data-ttu-id="c9fa6-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c9fa6-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c9fa6-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9fa6-150">Minimum supported server</span></span><br/> | <span data-ttu-id="c9fa6-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9fa6-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c9fa6-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c9fa6-152">Namespace</span></span><br/>                | <span data-ttu-id="c9fa6-153">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c9fa6-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c9fa6-154">MOF</span><span class="sxs-lookup"><span data-stu-id="c9fa6-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9fa6-155"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9fa6-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9fa6-156">DLL</span><span class="sxs-lookup"><span data-stu-id="c9fa6-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9fa6-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9fa6-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9fa6-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9fa6-158">See also</span></span>

<dl> <dt>

<span data-ttu-id="c9fa6-159">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c9fa6-159">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c9fa6-160">**\_Шорткутфиле Win32**</span><span class="sxs-lookup"><span data-stu-id="c9fa6-160">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

