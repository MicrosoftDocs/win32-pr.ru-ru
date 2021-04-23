---
description: Возвращает битовую карту UInt32 с правами доступа к общему ресурсу, удерживаемому пользователем или группой, от имени которой возвращается экземпляр.
ms.assetid: 234f44a4-ffff-431d-a973-98f2bd313c7d
ms.tgt_platform: multiple
title: Метод Жетакцессмаск класса Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.GetAccessMask
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 745ce6d607adf84827c14a588640572b5d92be00
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990499"
---
# <a name="getaccessmask-method-of-the-win32_share-class"></a><span data-ttu-id="49ebb-103">Метод Жетакцессмаск \_ класса общего ресурса Win32</span><span class="sxs-lookup"><span data-stu-id="49ebb-103">GetAccessMask method of the Win32\_Share class</span></span>

<span data-ttu-id="49ebb-104">Метод **жетакцессмаск** возвращает битовую карту UInt32 с правами доступа к общему ресурсу, удерживаемому пользователем или группой, от имени которой возвращается экземпляр.</span><span class="sxs-lookup"><span data-stu-id="49ebb-104">The **GetAccessMask** method returns a uint32 bitmap with the access rights to the share held by the user or group on whose behalf the instance is returned.</span></span>

<span data-ttu-id="49ebb-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="49ebb-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="49ebb-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="49ebb-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="49ebb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49ebb-107">Syntax</span></span>


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a><span data-ttu-id="49ebb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="49ebb-108">Parameters</span></span>

<span data-ttu-id="49ebb-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="49ebb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="49ebb-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49ebb-110">Return value</span></span>

<span data-ttu-id="49ebb-111">Права доступа к общему ресурсу, удерживаемому пользователем или группой.</span><span class="sxs-lookup"><span data-stu-id="49ebb-111">Access rights to the share held by the user or group.</span></span>

<dl> <dt>

<span data-ttu-id="49ebb-112">**\_каталог списка \_ файлов**</span><span class="sxs-lookup"><span data-stu-id="49ebb-112">**FILE\_LIST\_DIRECTORY**</span></span>
</dt> <dd>

<span data-ttu-id="49ebb-113">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="49ebb-113">1 (0x1)</span></span>

<span data-ttu-id="49ebb-114">Предоставляет право на чтение данных из файла.</span><span class="sxs-lookup"><span data-stu-id="49ebb-114">Grants the right to read data from the file.</span></span> <span data-ttu-id="49ebb-115">Для каталога это значение предоставляет право на перечисление содержимого каталога.</span><span class="sxs-lookup"><span data-stu-id="49ebb-115">For a directory, this value grants the right to list the contents of the directory.</span></span>

</dd> <dt>

<span data-ttu-id="49ebb-116">**ФАЙЛ \_ Добавить \_ файл**</span><span class="sxs-lookup"><span data-stu-id="49ebb-116">**FILE\_ADD\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="49ebb-117">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="49ebb-117">2 (0x2)</span></span>

<span data-ttu-id="49ebb-118">Предоставляет право на запись данных в файл.</span><span class="sxs-lookup"><span data-stu-id="49ebb-118">Grants the right to write data to the file.</span></span> <span data-ttu-id="49ebb-119">Для каталога это значение предоставляет право на создание файла в каталоге.</span><span class="sxs-lookup"><span data-stu-id="49ebb-119">For a directory, this value grants the right to create a file in the directory.</span></span>

</dd> <dt>

<span data-ttu-id="49ebb-120">**ФАЙЛ \_ Добавить \_ подкаталог**</span><span class="sxs-lookup"><span data-stu-id="49ebb-120">**FILE\_ADD\_SUBDIRECTORY**</span></span>
</dt> <dd>

<span data-ttu-id="49ebb-121">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="49ebb-121">4 (0x4)</span></span>

<span data-ttu-id="49ebb-122">Предоставляет право добавлять данные в файл.</span><span class="sxs-lookup"><span data-stu-id="49ebb-122">Grants the right to append data to the file.</span></span> <span data-ttu-id="49ebb-123">Для каталога это значение предоставляет право на создание подкаталога.</span><span class="sxs-lookup"><span data-stu-id="49ebb-123">For a directory, this value grants the right to create a subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="49ebb-124">**\_чтение файла \_ EA**</span><span class="sxs-lookup"><span data-stu-id="49ebb-124">**FILE\_READ\_EA**</span></span>
</dt> <dd>

<span data-ttu-id="49ebb-125">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="49ebb-125">8 (0x8)</span></span>

<span data-ttu-id="49ebb-126">Предоставляет право на чтение расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="49ebb-126">Grants the right to read extended attributes.</span></span>

</dd> <dt>

<span data-ttu-id="49ebb-127">**запись в файл \_ \_ EA**</span><span class="sxs-lookup"><span data-stu-id="49ebb-127">**FILE\_WRITE\_EA**</span></span>
</dt> <dd>

<span data-ttu-id="49ebb-128">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="49ebb-128">16 (0x10)</span></span>

<span data-ttu-id="49ebb-129">Предоставляет право на запись расширенных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="49ebb-129">Grants the right to write extended attributes.</span></span>

</dd> <dt>

<span data-ttu-id="49ebb-130">**\_обход файла**</span><span class="sxs-lookup"><span data-stu-id="49ebb-130">**FILE\_TRAVERSE**</span></span>
</dt> <dd>

<span data-ttu-id="49ebb-131">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="49ebb-131">32 (0x20)</span></span>

<span data-ttu-id="49ebb-132">Предоставляет право на выполнение файла.</span><span class="sxs-lookup"><span data-stu-id="49ebb-132">Grants the right to execute a file.</span></span> <span data-ttu-id="49ebb-133">Для каталога можно просмотреть каталог.</span><span class="sxs-lookup"><span data-stu-id="49ebb-133">For a directory, the directory can be traversed.</span></span>

</dd> <dt>

<span data-ttu-id="49ebb-134">**\_дочерний файл удаления файла \_**</span><span class="sxs-lookup"><span data-stu-id="49ebb-134">**FILE\_DELETE\_CHILD**</span></span>
</dt> <dd>

<span data-ttu-id="49ebb-135">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="49ebb-135">64 (0x40)</span></span>

<span data-ttu-id="49ebb-136">Предоставляет право удалять каталог и все содержащиеся в нем файлы (дочерние элементы), даже если файлы доступны только для чтения.</span><span class="sxs-lookup"><span data-stu-id="49ebb-136">Grants the right to delete a directory and all of the files it contains (its children), even if the files are read-only.</span></span>

</dd> <dt>

<span data-ttu-id="49ebb-137">**\_атрибуты чтения \_ файла**</span><span class="sxs-lookup"><span data-stu-id="49ebb-137">**FILE\_READ\_ATTRIBUTES**</span></span>
</dt> <dd>

<span data-ttu-id="49ebb-138">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="49ebb-138">128 (0x80)</span></span>

<span data-ttu-id="49ebb-139">Предоставляет право на чтение атрибутов файлов.</span><span class="sxs-lookup"><span data-stu-id="49ebb-139">Grants the right to read file attributes.</span></span>

</dd> <dt>

<span data-ttu-id="49ebb-140">**\_атрибуты записи \_ файла**</span><span class="sxs-lookup"><span data-stu-id="49ebb-140">**FILE\_WRITE\_ATTRIBUTES**</span></span>
</dt> <dd>

<span data-ttu-id="49ebb-141">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="49ebb-141">256 (0x100)</span></span>

<span data-ttu-id="49ebb-142">Предоставляет право на изменение атрибутов файлов.</span><span class="sxs-lookup"><span data-stu-id="49ebb-142">Grants the right to change file attributes.</span></span>

</dd> <dt>

<span data-ttu-id="49ebb-143">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="49ebb-143">**DELETE**</span></span>
</dt> <dd>

<span data-ttu-id="49ebb-144">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="49ebb-144">65536 (0x10000)</span></span>

<span data-ttu-id="49ebb-145">Предоставляет доступ на удаление.</span><span class="sxs-lookup"><span data-stu-id="49ebb-145">Grants delete access.</span></span>

</dd> <dt>

<span data-ttu-id="49ebb-146">**\_Контроль чтения**</span><span class="sxs-lookup"><span data-stu-id="49ebb-146">**READ\_CONTROL**</span></span>
</dt> <dd>

<span data-ttu-id="49ebb-147">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="49ebb-147">131072 (0x20000)</span></span>

<span data-ttu-id="49ebb-148">Предоставляет доступ на чтение дескриптора безопасности и владельца.</span><span class="sxs-lookup"><span data-stu-id="49ebb-148">Grants read access to the security descriptor and owner.</span></span>

</dd> <dt>

<span data-ttu-id="49ebb-149">**ЗАПИСЬ \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="49ebb-149">**WRITE\_DAC**</span></span>
</dt> <dd>

<span data-ttu-id="49ebb-150">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="49ebb-150">262144 (0x40000)</span></span>

<span data-ttu-id="49ebb-151">Предоставляет доступ на запись к списку управления доступом на уровне пользователей (DACL).</span><span class="sxs-lookup"><span data-stu-id="49ebb-151">Grants write access to the discretionary access control list (DACL).</span></span>

</dd> <dt>

<span data-ttu-id="49ebb-152">**\_владелец записи**</span><span class="sxs-lookup"><span data-stu-id="49ebb-152">**WRITE\_OWNER**</span></span>
</dt> <dd>

<span data-ttu-id="49ebb-153">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="49ebb-153">524288 (0x80000)</span></span>

<span data-ttu-id="49ebb-154">Назначает владельца записи.</span><span class="sxs-lookup"><span data-stu-id="49ebb-154">Assigns the write owner.</span></span>

</dd> <dt>

<span data-ttu-id="49ebb-155">**SYNCHRONIZE**</span><span class="sxs-lookup"><span data-stu-id="49ebb-155">**SYNCHRONIZE**</span></span>
</dt> <dd>

<span data-ttu-id="49ebb-156">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="49ebb-156">1048576 (0x100000)</span></span>

<span data-ttu-id="49ebb-157">Синхронизирует доступ и позволяет процессу ожидать, пока объект перейдет в сигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="49ebb-157">Synchronizes access and allows a process to wait for an object to enter the signaled state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49ebb-158">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49ebb-158">Remarks</span></span>

<span data-ttu-id="49ebb-159">Метод **жетакцессмаск** является методом объекта и используется для вхождения этого класса.</span><span class="sxs-lookup"><span data-stu-id="49ebb-159">**GetAccessMask** method is an object method and is used on an occurrence of this class.</span></span>

## <a name="examples"></a><span data-ttu-id="49ebb-160">Примеры</span><span class="sxs-lookup"><span data-stu-id="49ebb-160">Examples</span></span>

<span data-ttu-id="49ebb-161">Следующий пример кода VBScript создает общую папку, а затем получает значение маски доступа в дескрипторе безопасности, который защищает общую папку.</span><span class="sxs-lookup"><span data-stu-id="49ebb-161">The following VBScript code example creates a share folder and then gets the value of the access mask in the security descriptor that secures the share folder.</span></span>


```VB
Const FILE_SHARE = 0
Const MAXIMUM_CONNECTIONS = 4000 
strComputer = "."

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objNewShare = objWMIService.Get("Win32_Share")
Return = objNewShare.Create ("C:\Temp", "TestShare", FILE_SHARE, MAXIMUM_CONNECTIONS, "test share")

If Return <> 0 Then
          WScript.Echo Return
          WScript.Quit
End If

Set objShare = objWMIService.Get("Win32_Share.Name='TestShare'")
Return = objShare.GetAccessMask
WScript.Echo Return
```



## <a name="requirements"></a><span data-ttu-id="49ebb-162">Требования</span><span class="sxs-lookup"><span data-stu-id="49ebb-162">Requirements</span></span>



| <span data-ttu-id="49ebb-163">Требование</span><span class="sxs-lookup"><span data-stu-id="49ebb-163">Requirement</span></span> | <span data-ttu-id="49ebb-164">Значение</span><span class="sxs-lookup"><span data-stu-id="49ebb-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49ebb-165">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49ebb-165">Minimum supported client</span></span><br/> | <span data-ttu-id="49ebb-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49ebb-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49ebb-167">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49ebb-167">Minimum supported server</span></span><br/> | <span data-ttu-id="49ebb-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49ebb-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49ebb-169">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="49ebb-169">Namespace</span></span><br/>                | <span data-ttu-id="49ebb-170">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="49ebb-170">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="49ebb-171">MOF</span><span class="sxs-lookup"><span data-stu-id="49ebb-171">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49ebb-172"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49ebb-172"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="49ebb-173">DLL</span><span class="sxs-lookup"><span data-stu-id="49ebb-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49ebb-174"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49ebb-174"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49ebb-175">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49ebb-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49ebb-176">**\_Общий ресурс Win32**</span><span class="sxs-lookup"><span data-stu-id="49ebb-176">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

