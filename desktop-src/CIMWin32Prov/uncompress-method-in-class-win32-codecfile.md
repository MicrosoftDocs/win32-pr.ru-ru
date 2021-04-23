---
description: Распаковывает логический файл кодека (или каталог), указанный в пути объекта.
ms.assetid: abe74267-1274-4b20-82ac-51ca94d7af33
ms.tgt_platform: multiple
title: Метод uncompressия класса Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7d1ffcf99877781c7070b42dac5ffe9ef83af2d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895598"
---
# <a name="uncompress-method-of-the-win32_codecfile-class"></a><span data-ttu-id="ecf7e-103">Метод uncompressия класса Win32 \_ кодекфиле</span><span class="sxs-lookup"><span data-stu-id="ecf7e-103">Uncompress method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="ecf7e-104">Метод **uncompress** [WMI-класс](/windows/desktop/WmiSdk/retrieving-a-class) распаковывает логический файл кодека (или каталог), указанный в пути объекта.</span><span class="sxs-lookup"><span data-stu-id="ecf7e-104">The **Uncompress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical codec file (or directory) specified in the object path.</span></span>

<span data-ttu-id="ecf7e-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="ecf7e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ecf7e-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ecf7e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ecf7e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ecf7e-107">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="ecf7e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ecf7e-108">Parameters</span></span>

<span data-ttu-id="ecf7e-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="ecf7e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ecf7e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ecf7e-110">Return value</span></span>

<span data-ttu-id="ecf7e-111">Возвращает целочисленное значение 0 (ноль), если файл был успешно распакован, и любое другое число для указания ошибки.</span><span class="sxs-lookup"><span data-stu-id="ecf7e-111">Returns an integer value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="ecf7e-112">**0**</span><span class="sxs-lookup"><span data-stu-id="ecf7e-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ecf7e-113">Запрос выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="ecf7e-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="ecf7e-114">**2**</span><span class="sxs-lookup"><span data-stu-id="ecf7e-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ecf7e-115">Отказано в доступе.</span><span class="sxs-lookup"><span data-stu-id="ecf7e-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="ecf7e-116">**8**</span><span class="sxs-lookup"><span data-stu-id="ecf7e-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ecf7e-117">Произошла неопределенная ошибка.</span><span class="sxs-lookup"><span data-stu-id="ecf7e-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="ecf7e-118">**9**</span><span class="sxs-lookup"><span data-stu-id="ecf7e-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ecf7e-119">Указано недопустимое имя.</span><span class="sxs-lookup"><span data-stu-id="ecf7e-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ecf7e-120">**10**</span><span class="sxs-lookup"><span data-stu-id="ecf7e-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="ecf7e-121">Указанный объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="ecf7e-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ecf7e-122">**11**</span><span class="sxs-lookup"><span data-stu-id="ecf7e-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="ecf7e-123">Файловая система не является системой NTFS.</span><span class="sxs-lookup"><span data-stu-id="ecf7e-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="ecf7e-124">**12**</span><span class="sxs-lookup"><span data-stu-id="ecf7e-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="ecf7e-125">Платформа не является Windows.</span><span class="sxs-lookup"><span data-stu-id="ecf7e-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="ecf7e-126">**13**</span><span class="sxs-lookup"><span data-stu-id="ecf7e-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="ecf7e-127">Диск не совпадает.</span><span class="sxs-lookup"><span data-stu-id="ecf7e-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="ecf7e-128">**14**</span><span class="sxs-lookup"><span data-stu-id="ecf7e-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="ecf7e-129">Каталог не пуст.</span><span class="sxs-lookup"><span data-stu-id="ecf7e-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="ecf7e-130">**15**</span><span class="sxs-lookup"><span data-stu-id="ecf7e-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="ecf7e-131">Нарушение общего доступа.</span><span class="sxs-lookup"><span data-stu-id="ecf7e-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="ecf7e-132">**16**</span><span class="sxs-lookup"><span data-stu-id="ecf7e-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="ecf7e-133">Указан недопустимый файл запуска.</span><span class="sxs-lookup"><span data-stu-id="ecf7e-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ecf7e-134">**17**</span><span class="sxs-lookup"><span data-stu-id="ecf7e-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="ecf7e-135">Привилегия, необходимая для операции, не удерживается.</span><span class="sxs-lookup"><span data-stu-id="ecf7e-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="ecf7e-136">**открыт**</span><span class="sxs-lookup"><span data-stu-id="ecf7e-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ecf7e-137">Указан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="ecf7e-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ecf7e-138">Требования</span><span class="sxs-lookup"><span data-stu-id="ecf7e-138">Requirements</span></span>



| <span data-ttu-id="ecf7e-139">Требование</span><span class="sxs-lookup"><span data-stu-id="ecf7e-139">Requirement</span></span> | <span data-ttu-id="ecf7e-140">Значение</span><span class="sxs-lookup"><span data-stu-id="ecf7e-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecf7e-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ecf7e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ecf7e-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ecf7e-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ecf7e-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ecf7e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ecf7e-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ecf7e-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ecf7e-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ecf7e-145">Namespace</span></span><br/>                | <span data-ttu-id="ecf7e-146">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ecf7e-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ecf7e-147">MOF</span><span class="sxs-lookup"><span data-stu-id="ecf7e-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ecf7e-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ecf7e-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ecf7e-149">DLL</span><span class="sxs-lookup"><span data-stu-id="ecf7e-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecf7e-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecf7e-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecf7e-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ecf7e-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="ecf7e-152">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ecf7e-152">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ecf7e-153">**\_Кодекфиле Win32**</span><span class="sxs-lookup"><span data-stu-id="ecf7e-153">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

