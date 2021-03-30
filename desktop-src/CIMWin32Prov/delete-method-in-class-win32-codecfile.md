---
description: Удаляет логический аудио-или видеофайловый кодек (или каталог), указанный в пути к объекту.
ms.assetid: 70233615-8924-4bd4-8a20-279a18b5c807
ms.tgt_platform: multiple
title: Метод Delete класса Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9d9395f5c5ebaf2948043fe43e84685e4c39d4d0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896446"
---
# <a name="delete-method-of-the-win32_codecfile-class"></a><span data-ttu-id="d5b32-103">Метод DELETE \_ класса Кодекфиле Win32</span><span class="sxs-lookup"><span data-stu-id="d5b32-103">Delete method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="d5b32-104">Метод **удаления** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) удаляет логический аудио-или видеофайловый кодек (или каталог), указанный в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="d5b32-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes the logical audio or video codec file (or directory) specified in the object path.</span></span>

<span data-ttu-id="d5b32-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="d5b32-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d5b32-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d5b32-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5b32-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5b32-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="d5b32-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5b32-108">Parameters</span></span>

<span data-ttu-id="d5b32-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d5b32-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5b32-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5b32-110">Return value</span></span>

<span data-ttu-id="d5b32-111">Возвращает значение 0 (нуль), если файл был успешно удален, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="d5b32-111">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d5b32-112">**0**</span><span class="sxs-lookup"><span data-stu-id="d5b32-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d5b32-113">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="d5b32-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="d5b32-114">**2**</span><span class="sxs-lookup"><span data-stu-id="d5b32-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d5b32-115">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="d5b32-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="d5b32-116">**8**</span><span class="sxs-lookup"><span data-stu-id="d5b32-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d5b32-117">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d5b32-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d5b32-118">**9**</span><span class="sxs-lookup"><span data-stu-id="d5b32-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d5b32-119">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="d5b32-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d5b32-120">**10**</span><span class="sxs-lookup"><span data-stu-id="d5b32-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="d5b32-121">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="d5b32-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d5b32-122">**11**</span><span class="sxs-lookup"><span data-stu-id="d5b32-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="d5b32-123">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="d5b32-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="d5b32-124">**12**</span><span class="sxs-lookup"><span data-stu-id="d5b32-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="d5b32-125">Платформа не является Windows NT или Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d5b32-125">The platform is not Windows NT or Windows 2000.</span></span>

</dd> <dt>

<span data-ttu-id="d5b32-126">**13**</span><span class="sxs-lookup"><span data-stu-id="d5b32-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="d5b32-127">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="d5b32-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="d5b32-128">**14**</span><span class="sxs-lookup"><span data-stu-id="d5b32-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="d5b32-129">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="d5b32-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="d5b32-130">**15**</span><span class="sxs-lookup"><span data-stu-id="d5b32-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="d5b32-131">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="d5b32-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="d5b32-132">**16**</span><span class="sxs-lookup"><span data-stu-id="d5b32-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="d5b32-133">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="d5b32-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d5b32-134">**17**</span><span class="sxs-lookup"><span data-stu-id="d5b32-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="d5b32-135">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="d5b32-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="d5b32-136">**открыт**</span><span class="sxs-lookup"><span data-stu-id="d5b32-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d5b32-137">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="d5b32-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5b32-138">Требования</span><span class="sxs-lookup"><span data-stu-id="d5b32-138">Requirements</span></span>



| <span data-ttu-id="d5b32-139">Требование</span><span class="sxs-lookup"><span data-stu-id="d5b32-139">Requirement</span></span> | <span data-ttu-id="d5b32-140">Значение</span><span class="sxs-lookup"><span data-stu-id="d5b32-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5b32-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d5b32-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d5b32-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5b32-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d5b32-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d5b32-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d5b32-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5b32-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d5b32-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d5b32-145">Namespace</span></span><br/>                | <span data-ttu-id="d5b32-146">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d5b32-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d5b32-147">MOF</span><span class="sxs-lookup"><span data-stu-id="d5b32-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5b32-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5b32-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5b32-149">DLL</span><span class="sxs-lookup"><span data-stu-id="d5b32-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5b32-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5b32-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5b32-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5b32-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="d5b32-152">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d5b32-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d5b32-153">**\_Кодекфиле Win32**</span><span class="sxs-lookup"><span data-stu-id="d5b32-153">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

