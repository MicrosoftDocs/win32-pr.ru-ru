---
description: Переименовывает файл ярлыка (или каталог), указанный в пути к объекту.
ms.assetid: 6325fe96-19ee-4ccc-934c-ef0c0668f353
ms.tgt_platform: multiple
title: Метод Rename класса Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c095a702269084a938887ef9717253df4653aea0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655637"
---
# <a name="rename-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="660fe-103">Метод Rename класса Win32 \_ шорткутфиле</span><span class="sxs-lookup"><span data-stu-id="660fe-103">Rename method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="660fe-104">Метод класса **Rename** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) переименовывает файл ярлыка (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="660fe-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames the shortcut file (or directory) specified in the object path.</span></span> <span data-ttu-id="660fe-105">Переименование не поддерживается, если место назначения находится на другом диске или требуется перезапись существующего логического файла.</span><span class="sxs-lookup"><span data-stu-id="660fe-105">A rename is not supported if the destination is on another drive or if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="660fe-106">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="660fe-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="660fe-107">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="660fe-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="660fe-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="660fe-108">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="660fe-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="660fe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="660fe-110">*Имя файла* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="660fe-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="660fe-111">Полное новое имя файла (или каталога).</span><span class="sxs-lookup"><span data-stu-id="660fe-111">Fully qualified new name of the file (or directory).</span></span>

<span data-ttu-id="660fe-112">Пример: c: \\ temp \\newfile.txt</span><span class="sxs-lookup"><span data-stu-id="660fe-112">Example: c:\\temp\\newfile.txt</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="660fe-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="660fe-113">Return value</span></span>

<span data-ttu-id="660fe-114">Возвращает значение 0 (нуль), если файл был успешно переименован, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="660fe-114">Returns a value of 0 (zero) if the file was successfully renamed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="660fe-115">**0**</span><span class="sxs-lookup"><span data-stu-id="660fe-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="660fe-116">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="660fe-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="660fe-117">**2**</span><span class="sxs-lookup"><span data-stu-id="660fe-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="660fe-118">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="660fe-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="660fe-119">**8**</span><span class="sxs-lookup"><span data-stu-id="660fe-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="660fe-120">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="660fe-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="660fe-121">**9**</span><span class="sxs-lookup"><span data-stu-id="660fe-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="660fe-122">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="660fe-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="660fe-123">**10**</span><span class="sxs-lookup"><span data-stu-id="660fe-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="660fe-124">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="660fe-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="660fe-125">**11**</span><span class="sxs-lookup"><span data-stu-id="660fe-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="660fe-126">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="660fe-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="660fe-127">**12**</span><span class="sxs-lookup"><span data-stu-id="660fe-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="660fe-128">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="660fe-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="660fe-129">**13**</span><span class="sxs-lookup"><span data-stu-id="660fe-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="660fe-130">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="660fe-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="660fe-131">**14**</span><span class="sxs-lookup"><span data-stu-id="660fe-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="660fe-132">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="660fe-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="660fe-133">**15**</span><span class="sxs-lookup"><span data-stu-id="660fe-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="660fe-134">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="660fe-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="660fe-135">**16**</span><span class="sxs-lookup"><span data-stu-id="660fe-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="660fe-136">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="660fe-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="660fe-137">**17**</span><span class="sxs-lookup"><span data-stu-id="660fe-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="660fe-138">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="660fe-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="660fe-139">**открыт**</span><span class="sxs-lookup"><span data-stu-id="660fe-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="660fe-140">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="660fe-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="660fe-141">Требования</span><span class="sxs-lookup"><span data-stu-id="660fe-141">Requirements</span></span>



| <span data-ttu-id="660fe-142">Требование</span><span class="sxs-lookup"><span data-stu-id="660fe-142">Requirement</span></span> | <span data-ttu-id="660fe-143">Значение</span><span class="sxs-lookup"><span data-stu-id="660fe-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="660fe-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="660fe-144">Minimum supported client</span></span><br/> | <span data-ttu-id="660fe-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="660fe-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="660fe-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="660fe-146">Minimum supported server</span></span><br/> | <span data-ttu-id="660fe-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="660fe-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="660fe-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="660fe-148">Namespace</span></span><br/>                | <span data-ttu-id="660fe-149">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="660fe-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="660fe-150">MOF</span><span class="sxs-lookup"><span data-stu-id="660fe-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="660fe-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="660fe-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="660fe-152">DLL</span><span class="sxs-lookup"><span data-stu-id="660fe-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="660fe-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="660fe-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="660fe-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="660fe-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="660fe-155">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="660fe-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="660fe-156">**\_Шорткутфиле Win32**</span><span class="sxs-lookup"><span data-stu-id="660fe-156">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

