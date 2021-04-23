---
description: Копирует файл логического кодека или каталог, указанный в пути к объекту, в расположение, указанное входным параметром.
ms.assetid: 77e67b01-561b-4233-899d-fa4bbf75ecf8
ms.tgt_platform: multiple
title: Метод Copy класса Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e3bd6621c065192eb45176444257f1c29c897201
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655901"
---
# <a name="copy-method-of-the-win32_codecfile-class"></a><span data-ttu-id="45f60-103">Метод Copy \_ класса Win32 кодекфиле</span><span class="sxs-lookup"><span data-stu-id="45f60-103">Copy method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="45f60-104">Метод **копирования** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) копирует логический файл кодека или каталог, указанный в пути к объекту, в расположение, указанное входным параметром.</span><span class="sxs-lookup"><span data-stu-id="45f60-104">The **Copy** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical codec file or directory specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="45f60-105">Копирование не поддерживается, если требуется перезапись существующего логического файла.</span><span class="sxs-lookup"><span data-stu-id="45f60-105">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="45f60-106">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="45f60-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="45f60-107">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="45f60-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="45f60-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45f60-108">Syntax</span></span>


```mof
uint32 Copy(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="45f60-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="45f60-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45f60-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="45f60-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="45f60-111">Полное имя копии файла (или каталога).</span><span class="sxs-lookup"><span data-stu-id="45f60-111">Fully qualified name of the copy of the file (or directory).</span></span> <span data-ttu-id="45f60-112">Пример: c: \\ temp \\ невдиректори.</span><span class="sxs-lookup"><span data-stu-id="45f60-112">Example: c:\\temp\\newdirectory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45f60-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45f60-113">Return value</span></span>

<span data-ttu-id="45f60-114">Возвращает значение 0 (нуль), если файл был успешно скопирован, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="45f60-114">Returns an value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="45f60-115">**0**</span><span class="sxs-lookup"><span data-stu-id="45f60-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="45f60-116">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="45f60-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="45f60-117">**2**</span><span class="sxs-lookup"><span data-stu-id="45f60-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="45f60-118">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="45f60-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="45f60-119">**8**</span><span class="sxs-lookup"><span data-stu-id="45f60-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="45f60-120">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="45f60-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="45f60-121">**9**</span><span class="sxs-lookup"><span data-stu-id="45f60-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="45f60-122">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="45f60-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="45f60-123">**10**</span><span class="sxs-lookup"><span data-stu-id="45f60-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="45f60-124">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="45f60-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="45f60-125">**11**</span><span class="sxs-lookup"><span data-stu-id="45f60-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="45f60-126">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="45f60-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="45f60-127">**12**</span><span class="sxs-lookup"><span data-stu-id="45f60-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="45f60-128">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="45f60-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="45f60-129">**13**</span><span class="sxs-lookup"><span data-stu-id="45f60-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="45f60-130">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="45f60-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="45f60-131">**14**</span><span class="sxs-lookup"><span data-stu-id="45f60-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="45f60-132">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="45f60-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="45f60-133">**15**</span><span class="sxs-lookup"><span data-stu-id="45f60-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="45f60-134">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="45f60-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="45f60-135">**16**</span><span class="sxs-lookup"><span data-stu-id="45f60-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="45f60-136">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="45f60-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="45f60-137">**17**</span><span class="sxs-lookup"><span data-stu-id="45f60-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="45f60-138">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="45f60-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="45f60-139">**открыт**</span><span class="sxs-lookup"><span data-stu-id="45f60-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="45f60-140">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="45f60-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="45f60-141">Требования</span><span class="sxs-lookup"><span data-stu-id="45f60-141">Requirements</span></span>



| <span data-ttu-id="45f60-142">Требование</span><span class="sxs-lookup"><span data-stu-id="45f60-142">Requirement</span></span> | <span data-ttu-id="45f60-143">Значение</span><span class="sxs-lookup"><span data-stu-id="45f60-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45f60-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45f60-144">Minimum supported client</span></span><br/> | <span data-ttu-id="45f60-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45f60-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="45f60-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45f60-146">Minimum supported server</span></span><br/> | <span data-ttu-id="45f60-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45f60-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="45f60-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="45f60-148">Namespace</span></span><br/>                | <span data-ttu-id="45f60-149">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="45f60-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="45f60-150">MOF</span><span class="sxs-lookup"><span data-stu-id="45f60-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45f60-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45f60-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="45f60-152">DLL</span><span class="sxs-lookup"><span data-stu-id="45f60-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45f60-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45f60-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45f60-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45f60-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="45f60-155">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="45f60-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="45f60-156">**\_Кодекфиле Win32**</span><span class="sxs-lookup"><span data-stu-id="45f60-156">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

