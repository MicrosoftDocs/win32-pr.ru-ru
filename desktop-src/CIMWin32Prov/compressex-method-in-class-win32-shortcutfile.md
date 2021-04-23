---
description: Сжимает логический файл ярлыка (или каталог), указанный в пути объекта (этот метод является расширенной версией метода сжатия).
ms.assetid: 1f7b6182-6ab7-4801-83a8-b57b1c78001f
ms.tgt_platform: multiple
title: Метод Компрессекс класса Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 512511b690ed6769895e9c4f9922d479d66f847e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990425"
---
# <a name="compressex-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="f7767-103">Метод Компрессекс \_ класса Win32 шорткутфиле</span><span class="sxs-lookup"><span data-stu-id="f7767-103">CompressEx method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="f7767-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) компрессекс сжимает логический файл ярлыка (или каталог), указанный в пути к объекту (этот метод является расширенной версией метода [**сжатия**](compress-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="f7767-104">The **CompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical shortcut file (or directory) specified in the object path (this method is an extended version of the [**Compress**](compress-method-in-class-win32-directory.md) method).</span></span>

<span data-ttu-id="f7767-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="f7767-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f7767-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f7767-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f7767-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7767-107">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="f7767-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7767-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7767-109">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f7767-109">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7767-110">Имя файла или каталога, в котором произошел сбой метода [**компрессекс**](compressex-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="f7767-110">Name of the file or directory where the [**CompressEx**](compressex-method-in-class-win32-directory.md) method failed.</span></span> <span data-ttu-id="f7767-111">Если метод завершится с ошибкой, этот параметр будет иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="f7767-111">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="f7767-112">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f7767-112">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f7767-113">Имя дочернего файла или каталога, который будет использоваться в качестве отправной точки для [**компрессекс**](compressex-method-in-class-win32-directory.md).</span><span class="sxs-lookup"><span data-stu-id="f7767-113">Names the child file or directory to use as a starting point for [**CompressEx**](compressex-method-in-class-win32-directory.md).</span></span> <span data-ttu-id="f7767-114">Параметр *StartFileName* обычно представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="f7767-114">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="f7767-115">Если этот параметр имеет **значение NULL**, операция выполняется над файлом или каталогом, указанным в вызове метода **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="f7767-115">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="f7767-116">*Рекурсивно* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f7767-116">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f7767-117">Если **значение — true**, изменение владельца будет применяться рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="f7767-117">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="f7767-118">Для экземпляров файлов *рекурсивный* параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="f7767-118">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7767-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7767-119">Return value</span></span>

<span data-ttu-id="f7767-120">Возвращает значение 0 (ноль), если файл был успешно сжат, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="f7767-120">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="f7767-121">**0**</span><span class="sxs-lookup"><span data-stu-id="f7767-121">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f7767-122">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="f7767-122">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="f7767-123">**2**</span><span class="sxs-lookup"><span data-stu-id="f7767-123">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f7767-124">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="f7767-124">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="f7767-125">**8**</span><span class="sxs-lookup"><span data-stu-id="f7767-125">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f7767-126">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f7767-126">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="f7767-127">**9**</span><span class="sxs-lookup"><span data-stu-id="f7767-127">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f7767-128">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="f7767-128">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f7767-129">**10**</span><span class="sxs-lookup"><span data-stu-id="f7767-129">**10**</span></span>
</dt> <dd>

<span data-ttu-id="f7767-130">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="f7767-130">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f7767-131">**11**</span><span class="sxs-lookup"><span data-stu-id="f7767-131">**11**</span></span>
</dt> <dd>

<span data-ttu-id="f7767-132">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="f7767-132">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="f7767-133">**12**</span><span class="sxs-lookup"><span data-stu-id="f7767-133">**12**</span></span>
</dt> <dd>

<span data-ttu-id="f7767-134">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="f7767-134">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="f7767-135">**13**</span><span class="sxs-lookup"><span data-stu-id="f7767-135">**13**</span></span>
</dt> <dd>

<span data-ttu-id="f7767-136">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="f7767-136">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="f7767-137">**14**</span><span class="sxs-lookup"><span data-stu-id="f7767-137">**14**</span></span>
</dt> <dd>

<span data-ttu-id="f7767-138">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="f7767-138">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="f7767-139">**15**</span><span class="sxs-lookup"><span data-stu-id="f7767-139">**15**</span></span>
</dt> <dd>

<span data-ttu-id="f7767-140">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="f7767-140">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="f7767-141">**16**</span><span class="sxs-lookup"><span data-stu-id="f7767-141">**16**</span></span>
</dt> <dd>

<span data-ttu-id="f7767-142">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="f7767-142">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f7767-143">**17**</span><span class="sxs-lookup"><span data-stu-id="f7767-143">**17**</span></span>
</dt> <dd>

<span data-ttu-id="f7767-144">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="f7767-144">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="f7767-145">**открыт**</span><span class="sxs-lookup"><span data-stu-id="f7767-145">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f7767-146">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="f7767-146">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7767-147">Требования</span><span class="sxs-lookup"><span data-stu-id="f7767-147">Requirements</span></span>



| <span data-ttu-id="f7767-148">Требование</span><span class="sxs-lookup"><span data-stu-id="f7767-148">Requirement</span></span> | <span data-ttu-id="f7767-149">Значение</span><span class="sxs-lookup"><span data-stu-id="f7767-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7767-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7767-150">Minimum supported client</span></span><br/> | <span data-ttu-id="f7767-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7767-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f7767-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7767-152">Minimum supported server</span></span><br/> | <span data-ttu-id="f7767-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7767-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f7767-154">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f7767-154">Namespace</span></span><br/>                | <span data-ttu-id="f7767-155">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f7767-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f7767-156">MOF</span><span class="sxs-lookup"><span data-stu-id="f7767-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7767-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7767-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7767-158">DLL</span><span class="sxs-lookup"><span data-stu-id="f7767-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7767-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7767-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7767-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7767-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="f7767-161">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f7767-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f7767-162">**\_Шорткутфиле Win32**</span><span class="sxs-lookup"><span data-stu-id="f7767-162">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

