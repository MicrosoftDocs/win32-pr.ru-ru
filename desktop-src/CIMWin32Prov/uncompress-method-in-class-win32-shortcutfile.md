---
description: Распаковывает логический файл ярлыка (или каталог), указанный в пути объекта.
ms.assetid: e120391a-3839-4f8c-aca3-473d7f8b30bf
ms.tgt_platform: multiple
title: Метод uncompressия класса Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 48267f519dce9ae5d78581050255bd8e8b02222c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807858"
---
# <a name="uncompress-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="aa6af-103">Метод uncompressия класса Win32 \_ шорткутфиле</span><span class="sxs-lookup"><span data-stu-id="aa6af-103">Uncompress method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="aa6af-104">Метод **uncompressия** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) распаковывает логический файл ярлыка (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="aa6af-104">The **Uncompress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical shortcut file (or directory) specified in the object path.</span></span>

<span data-ttu-id="aa6af-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="aa6af-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="aa6af-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="aa6af-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="aa6af-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa6af-107">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="aa6af-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa6af-108">Parameters</span></span>

<span data-ttu-id="aa6af-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="aa6af-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aa6af-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aa6af-110">Return value</span></span>

<span data-ttu-id="aa6af-111">Возвращает значение 0 (нуль), если файл был успешно распакован, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="aa6af-111">Returns a value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="aa6af-112">**0**</span><span class="sxs-lookup"><span data-stu-id="aa6af-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="aa6af-113">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="aa6af-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="aa6af-114">**2**</span><span class="sxs-lookup"><span data-stu-id="aa6af-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="aa6af-115">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="aa6af-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="aa6af-116">**8**</span><span class="sxs-lookup"><span data-stu-id="aa6af-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="aa6af-117">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="aa6af-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="aa6af-118">**9**</span><span class="sxs-lookup"><span data-stu-id="aa6af-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="aa6af-119">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="aa6af-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="aa6af-120">**10**</span><span class="sxs-lookup"><span data-stu-id="aa6af-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="aa6af-121">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="aa6af-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="aa6af-122">**11**</span><span class="sxs-lookup"><span data-stu-id="aa6af-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="aa6af-123">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="aa6af-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="aa6af-124">**12**</span><span class="sxs-lookup"><span data-stu-id="aa6af-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="aa6af-125">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="aa6af-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="aa6af-126">**13**</span><span class="sxs-lookup"><span data-stu-id="aa6af-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="aa6af-127">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="aa6af-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="aa6af-128">**14**</span><span class="sxs-lookup"><span data-stu-id="aa6af-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="aa6af-129">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="aa6af-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="aa6af-130">**15**</span><span class="sxs-lookup"><span data-stu-id="aa6af-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="aa6af-131">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="aa6af-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="aa6af-132">**16**</span><span class="sxs-lookup"><span data-stu-id="aa6af-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="aa6af-133">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="aa6af-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="aa6af-134">**17**</span><span class="sxs-lookup"><span data-stu-id="aa6af-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="aa6af-135">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="aa6af-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="aa6af-136">**открыт**</span><span class="sxs-lookup"><span data-stu-id="aa6af-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="aa6af-137">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="aa6af-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa6af-138">Требования</span><span class="sxs-lookup"><span data-stu-id="aa6af-138">Requirements</span></span>



| <span data-ttu-id="aa6af-139">Требование</span><span class="sxs-lookup"><span data-stu-id="aa6af-139">Requirement</span></span> | <span data-ttu-id="aa6af-140">Значение</span><span class="sxs-lookup"><span data-stu-id="aa6af-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa6af-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa6af-141">Minimum supported client</span></span><br/> | <span data-ttu-id="aa6af-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa6af-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aa6af-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa6af-143">Minimum supported server</span></span><br/> | <span data-ttu-id="aa6af-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa6af-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aa6af-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="aa6af-145">Namespace</span></span><br/>                | <span data-ttu-id="aa6af-146">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="aa6af-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aa6af-147">MOF</span><span class="sxs-lookup"><span data-stu-id="aa6af-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa6af-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa6af-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa6af-149">DLL</span><span class="sxs-lookup"><span data-stu-id="aa6af-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa6af-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa6af-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa6af-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa6af-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="aa6af-152">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aa6af-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="aa6af-153">**\_Шорткутфиле Win32**</span><span class="sxs-lookup"><span data-stu-id="aa6af-153">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

