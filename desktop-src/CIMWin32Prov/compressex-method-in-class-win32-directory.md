---
description: Сжимает логический файл записи каталога (или каталог), указанный в пути к объекту (этот метод является расширенной версией метода сжатия).
ms.assetid: 6b6e559c-4ca6-49d4-b255-5e1511fdf2e2
ms.tgt_platform: multiple
title: Метод Компрессекс класса Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3ee300919efa388d27ae9d594bc2b6c27def88e6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655713"
---
# <a name="compressex-method-of-the-win32_directory-class"></a><span data-ttu-id="639b3-103">Метод Компрессекс \_ класса каталога Win32</span><span class="sxs-lookup"><span data-stu-id="639b3-103">CompressEx method of the Win32\_Directory class</span></span>

<span data-ttu-id="639b3-104">Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) компрессекс сжимает логический файл записи каталога (или каталог), указанный в пути к объекту (этот метод является расширенной версией метода [**сжатия**](compress-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="639b3-104">The **CompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical directory entry file (or directory) specified in the object path (this method is an extended version of the [**Compress**](compress-method-in-class-win32-directory.md) method).</span></span>

<span data-ttu-id="639b3-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="639b3-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="639b3-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="639b3-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="639b3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="639b3-107">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="639b3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="639b3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="639b3-109">*Стопфиленаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="639b3-109">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="639b3-110">Имя файла или каталога, в котором произошел сбой метода **компрессекс** .</span><span class="sxs-lookup"><span data-stu-id="639b3-110">Name of the file or directory where the **CompressEx** method failed.</span></span> <span data-ttu-id="639b3-111">Если метод завершится с ошибкой, этот параметр будет иметь **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="639b3-111">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="639b3-112">*StartFileName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="639b3-112">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="639b3-113">Имя дочернего файла или каталога, который будет использоваться в качестве отправной точки для **компрессекс**.</span><span class="sxs-lookup"><span data-stu-id="639b3-113">Names the child file or directory to use as a starting point for **CompressEx**.</span></span> <span data-ttu-id="639b3-114">Параметр *StartFileName* обычно представляет собой параметр *стопфиленаме* , указывающий файл или каталог, в котором произошла ошибка из предыдущего вызова метода.</span><span class="sxs-lookup"><span data-stu-id="639b3-114">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="639b3-115">Если этот параметр имеет **значение NULL**, операция выполняется над файлом или каталогом, указанным в вызове метода **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="639b3-115">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

<span data-ttu-id="639b3-116">Если используется параметр *StartFileName* , то для *рекурсии* необходимо также задать значение true.</span><span class="sxs-lookup"><span data-stu-id="639b3-116">If *StartFileName* is used, *Recursive* must be set to true as well.</span></span>

</dd> <dt>

<span data-ttu-id="639b3-117">*Рекурсивно* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="639b3-117">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="639b3-118">Если **значение — true**, изменение владельца будет применяться рекурсивно к файлам и каталогам в каталоге, указанном в экземпляре [**CIM \_ LogicalFile**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="639b3-118">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="639b3-119">Для экземпляров файлов *рекурсивный* входной параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="639b3-119">For file instances, the *Recursive* input parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="639b3-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="639b3-120">Return value</span></span>

<span data-ttu-id="639b3-121">Возвращает значение 0 (ноль), если файл был успешно сжат, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="639b3-121">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="639b3-122">**0**</span><span class="sxs-lookup"><span data-stu-id="639b3-122">**0**</span></span>
</dt> <dd>

<span data-ttu-id="639b3-123">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="639b3-123">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="639b3-124">**2**</span><span class="sxs-lookup"><span data-stu-id="639b3-124">**2**</span></span>
</dt> <dd>

<span data-ttu-id="639b3-125">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="639b3-125">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="639b3-126">**8**</span><span class="sxs-lookup"><span data-stu-id="639b3-126">**8**</span></span>
</dt> <dd>

<span data-ttu-id="639b3-127">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="639b3-127">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="639b3-128">**9**</span><span class="sxs-lookup"><span data-stu-id="639b3-128">**9**</span></span>
</dt> <dd>

<span data-ttu-id="639b3-129">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="639b3-129">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="639b3-130">**10**</span><span class="sxs-lookup"><span data-stu-id="639b3-130">**10**</span></span>
</dt> <dd>

<span data-ttu-id="639b3-131">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="639b3-131">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="639b3-132">**11**</span><span class="sxs-lookup"><span data-stu-id="639b3-132">**11**</span></span>
</dt> <dd>

<span data-ttu-id="639b3-133">Файловая система не является файловой системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="639b3-133">The file system is not an NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="639b3-134">**12**</span><span class="sxs-lookup"><span data-stu-id="639b3-134">**12**</span></span>
</dt> <dd>

<span data-ttu-id="639b3-135">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="639b3-135">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="639b3-136">**13**</span><span class="sxs-lookup"><span data-stu-id="639b3-136">**13**</span></span>
</dt> <dd>

<span data-ttu-id="639b3-137">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="639b3-137">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="639b3-138">**14**</span><span class="sxs-lookup"><span data-stu-id="639b3-138">**14**</span></span>
</dt> <dd>

<span data-ttu-id="639b3-139">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="639b3-139">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="639b3-140">**15**</span><span class="sxs-lookup"><span data-stu-id="639b3-140">**15**</span></span>
</dt> <dd>

<span data-ttu-id="639b3-141">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="639b3-141">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="639b3-142">**16**</span><span class="sxs-lookup"><span data-stu-id="639b3-142">**16**</span></span>
</dt> <dd>

<span data-ttu-id="639b3-143">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="639b3-143">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="639b3-144">**17**</span><span class="sxs-lookup"><span data-stu-id="639b3-144">**17**</span></span>
</dt> <dd>

<span data-ttu-id="639b3-145">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="639b3-145">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="639b3-146">**открыт**</span><span class="sxs-lookup"><span data-stu-id="639b3-146">**21**</span></span>
</dt> <dd>

<span data-ttu-id="639b3-147">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="639b3-147">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="639b3-148">Требования</span><span class="sxs-lookup"><span data-stu-id="639b3-148">Requirements</span></span>



| <span data-ttu-id="639b3-149">Требование</span><span class="sxs-lookup"><span data-stu-id="639b3-149">Requirement</span></span> | <span data-ttu-id="639b3-150">Значение</span><span class="sxs-lookup"><span data-stu-id="639b3-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="639b3-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="639b3-151">Minimum supported client</span></span><br/> | <span data-ttu-id="639b3-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="639b3-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="639b3-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="639b3-153">Minimum supported server</span></span><br/> | <span data-ttu-id="639b3-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="639b3-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="639b3-155">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="639b3-155">Namespace</span></span><br/>                | <span data-ttu-id="639b3-156">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="639b3-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="639b3-157">MOF</span><span class="sxs-lookup"><span data-stu-id="639b3-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="639b3-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="639b3-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="639b3-159">DLL</span><span class="sxs-lookup"><span data-stu-id="639b3-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="639b3-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="639b3-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="639b3-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="639b3-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="639b3-162">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="639b3-162">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="639b3-163">**\_Каталог Win32**</span><span class="sxs-lookup"><span data-stu-id="639b3-163">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

