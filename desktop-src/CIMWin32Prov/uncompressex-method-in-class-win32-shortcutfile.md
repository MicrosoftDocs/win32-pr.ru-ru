---
description: Распаковывает логический файл ярлыка (или каталог), указанный в пути объекта. Этот метод является расширенной версией метода uncompressия.
ms.assetid: aa1c04d1-4cce-4096-bce3-b9c61b9a4eb7
ms.tgt_platform: multiple
title: Метод Ункомпрессекс класса Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e07e86be3666b06063ef81c896eab6ee7a918657
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142526"
---
# <a name="uncompressex-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="ea3a5-104">Метод Ункомпрессекс \_ класса Win32 шорткутфиле</span><span class="sxs-lookup"><span data-stu-id="ea3a5-104">UncompressEx method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="ea3a5-105">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) ункомпрессекс распаковывает логический файл ярлыка (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="ea3a5-105">The **UncompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical shortcut file (or directory) specified in the object path.</span></span> <span data-ttu-id="ea3a5-106">Этот метод является расширенной версией метода [**uncompressия**](uncompress-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="ea3a5-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="ea3a5-107">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="ea3a5-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ea3a5-108">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ea3a5-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ea3a5-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ea3a5-109">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="ea3a5-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea3a5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea3a5-111">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ea3a5-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea3a5-112">Имя файла или каталога, в котором произошел сбой метода **ункомпрессекс** .</span><span class="sxs-lookup"><span data-stu-id="ea3a5-112">Name of the file or directory where the **UncompressEx** method failed.</span></span> <span data-ttu-id="ea3a5-113">Если метод завершится с ошибкой, этот параметр будет иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="ea3a5-113">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="ea3a5-114">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="ea3a5-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ea3a5-115">Имя дочернего файла или каталога, который будет использоваться в качестве отправной точки для **ункомпрессекс**.</span><span class="sxs-lookup"><span data-stu-id="ea3a5-115">Names the child file or directory to use as a starting point for **UncompressEx**.</span></span> <span data-ttu-id="ea3a5-116">Параметр *StartFileName* обычно представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="ea3a5-116">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="ea3a5-117">Если этот параметр имеет **значение NULL**, операция выполняется над файлом или каталогом, указанным в вызове метода ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="ea3a5-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="ea3a5-118">*Рекурсивно* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="ea3a5-118">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ea3a5-119">Если **значение — true**, изменение владельца будет применяться рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="ea3a5-119">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="ea3a5-120">Для экземпляров файлов *рекурсивный* параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="ea3a5-120">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea3a5-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea3a5-121">Return value</span></span>

<span data-ttu-id="ea3a5-122">Возвращает значение 0 (нуль), если файл был успешно распакован, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="ea3a5-122">Returns a value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="ea3a5-123">**0**</span><span class="sxs-lookup"><span data-stu-id="ea3a5-123">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ea3a5-124">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="ea3a5-124">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="ea3a5-125">**2**</span><span class="sxs-lookup"><span data-stu-id="ea3a5-125">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ea3a5-126">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="ea3a5-126">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="ea3a5-127">**8**</span><span class="sxs-lookup"><span data-stu-id="ea3a5-127">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ea3a5-128">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="ea3a5-128">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="ea3a5-129">**9**</span><span class="sxs-lookup"><span data-stu-id="ea3a5-129">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ea3a5-130">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="ea3a5-130">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ea3a5-131">**10**</span><span class="sxs-lookup"><span data-stu-id="ea3a5-131">**10**</span></span>
</dt> <dd>

<span data-ttu-id="ea3a5-132">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="ea3a5-132">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ea3a5-133">**11**</span><span class="sxs-lookup"><span data-stu-id="ea3a5-133">**11**</span></span>
</dt> <dd>

<span data-ttu-id="ea3a5-134">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="ea3a5-134">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="ea3a5-135">**12**</span><span class="sxs-lookup"><span data-stu-id="ea3a5-135">**12**</span></span>
</dt> <dd>

<span data-ttu-id="ea3a5-136">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="ea3a5-136">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="ea3a5-137">**13**</span><span class="sxs-lookup"><span data-stu-id="ea3a5-137">**13**</span></span>
</dt> <dd>

<span data-ttu-id="ea3a5-138">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="ea3a5-138">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="ea3a5-139">**14**</span><span class="sxs-lookup"><span data-stu-id="ea3a5-139">**14**</span></span>
</dt> <dd>

<span data-ttu-id="ea3a5-140">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="ea3a5-140">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="ea3a5-141">**15**</span><span class="sxs-lookup"><span data-stu-id="ea3a5-141">**15**</span></span>
</dt> <dd>

<span data-ttu-id="ea3a5-142">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="ea3a5-142">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="ea3a5-143">**16**</span><span class="sxs-lookup"><span data-stu-id="ea3a5-143">**16**</span></span>
</dt> <dd>

<span data-ttu-id="ea3a5-144">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="ea3a5-144">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ea3a5-145">**17**</span><span class="sxs-lookup"><span data-stu-id="ea3a5-145">**17**</span></span>
</dt> <dd>

<span data-ttu-id="ea3a5-146">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="ea3a5-146">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="ea3a5-147">**открыт**</span><span class="sxs-lookup"><span data-stu-id="ea3a5-147">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ea3a5-148">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="ea3a5-148">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea3a5-149">Требования</span><span class="sxs-lookup"><span data-stu-id="ea3a5-149">Requirements</span></span>



| <span data-ttu-id="ea3a5-150">Требование</span><span class="sxs-lookup"><span data-stu-id="ea3a5-150">Requirement</span></span> | <span data-ttu-id="ea3a5-151">Значение</span><span class="sxs-lookup"><span data-stu-id="ea3a5-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea3a5-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea3a5-152">Minimum supported client</span></span><br/> | <span data-ttu-id="ea3a5-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea3a5-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ea3a5-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea3a5-154">Minimum supported server</span></span><br/> | <span data-ttu-id="ea3a5-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea3a5-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ea3a5-156">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ea3a5-156">Namespace</span></span><br/>                | <span data-ttu-id="ea3a5-157">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ea3a5-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ea3a5-158">MOF</span><span class="sxs-lookup"><span data-stu-id="ea3a5-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea3a5-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea3a5-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea3a5-160">DLL</span><span class="sxs-lookup"><span data-stu-id="ea3a5-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea3a5-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea3a5-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea3a5-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea3a5-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="ea3a5-163">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ea3a5-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ea3a5-164">**\_Шорткутфиле Win32**</span><span class="sxs-lookup"><span data-stu-id="ea3a5-164">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

