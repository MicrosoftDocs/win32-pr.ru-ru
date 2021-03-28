---
description: Содержит автономное состояние папки.
ms.assetid: b50b130d-0675-49b5-b730-f67ea1c71d8c
title: Свойство folder2. Оффлинестатус (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.OfflineStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d456eae826e8a2e173b92fac4be716fb24bcb92d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984196"
---
# <a name="folder2offlinestatus-property"></a><span data-ttu-id="faf50-103">Folder2. Оффлинестатус, свойство</span><span class="sxs-lookup"><span data-stu-id="faf50-103">Folder2.OfflineStatus property</span></span>

<span data-ttu-id="faf50-104">Содержит автономное состояние папки.</span><span class="sxs-lookup"><span data-stu-id="faf50-104">Contains the offline status of the folder.</span></span>

<span data-ttu-id="faf50-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="faf50-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="faf50-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="faf50-106">Syntax</span></span>


```JScript
iOfflineStatus = Folder2.OfflineStatus
```



## <a name="property-value"></a><span data-ttu-id="faf50-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="faf50-107">Property value</span></span>

<span data-ttu-id="faf50-108">**Целое число** , заданное в качестве одного из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="faf50-108">An **Integer** that is set to one of the following values.</span></span>

<dt>



 <span data-ttu-id="faf50-109">(OFS \_ ДИРТИКАЧЕ)</span><span class="sxs-lookup"><span data-stu-id="faf50-109">(OFS\_DIRTYCACHE)</span></span>


</dt> <dd>

<span data-ttu-id="faf50-110">Сервер находится в режиме "в сети" с несинхронизированными изменениями.</span><span class="sxs-lookup"><span data-stu-id="faf50-110">Server is online with unsynchronized changes.</span></span>

</dd> <dt>



 <span data-ttu-id="faf50-111">(OFS \_ Активный</span><span class="sxs-lookup"><span data-stu-id="faf50-111">(OFS\_INACTIVE)</span></span>


</dt> <dd>

<span data-ttu-id="faf50-112">Автономное кэширование не включено для этой папки.</span><span class="sxs-lookup"><span data-stu-id="faf50-112">Offline caching is not enabled for this folder.</span></span>

</dd> <dt>



 <span data-ttu-id="faf50-113">(OFS \_ РАБОТА</span><span class="sxs-lookup"><span data-stu-id="faf50-113">(OFS\_OFFLINE)</span></span>


</dt> <dd>

<span data-ttu-id="faf50-114">Сервер находится в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="faf50-114">Server is offline.</span></span>

</dd> <dt>



 <span data-ttu-id="faf50-115">(OFS \_ СОБРАНИЯ</span><span class="sxs-lookup"><span data-stu-id="faf50-115">(OFS\_ONLINE)</span></span>


</dt> <dd>

<span data-ttu-id="faf50-116">Сервер находится в режиме "в сети".</span><span class="sxs-lookup"><span data-stu-id="faf50-116">Server is online.</span></span>

</dd> <dt>



 <span data-ttu-id="faf50-117">(OFS \_ СЕРВЕРБАКК)</span><span class="sxs-lookup"><span data-stu-id="faf50-117">(OFS\_SERVERBACK)</span></span>


</dt> <dd>

<span data-ttu-id="faf50-118">Сервер находится в автономном режиме, но может быть достигнут.</span><span class="sxs-lookup"><span data-stu-id="faf50-118">Server is offline but can be reached.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="faf50-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="faf50-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="faf50-120">Для правильной работы **оффлинестатус** необходимо включить автономные файлы с помощью параметров папки.</span><span class="sxs-lookup"><span data-stu-id="faf50-120">Offline Files must be enabled through Folder Options for **OfflineStatus** to work correctly.</span></span> <span data-ttu-id="faf50-121">Если параметр автономные файлы не включен, свойство возвращает значение **OFS \_ Inactive**.</span><span class="sxs-lookup"><span data-stu-id="faf50-121">If the Offline Files option is not enabled, the property returns **OFS\_INACTIVE**.</span></span>

 

## <a name="examples"></a><span data-ttu-id="faf50-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="faf50-122">Examples</span></span>

<span data-ttu-id="faf50-123">В следующем примере показано правильное использование **оффлинестатус** для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="faf50-123">The following example shows the proper use of **OfflineStatus** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="faf50-124">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="faf50-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnOfflineStatusJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("\\\\server\\share\\folder");
        if (objFolder2 != null)
        {
            var nReturn;

            nReturn = objFolder2.OfflineStatus;
        }
    }
</script>
```



<span data-ttu-id="faf50-125">Сценариев</span><span class="sxs-lookup"><span data-stu-id="faf50-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnOfflineStatusVB()
        dim objShell
        dim objFolder2
       
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("\\server\share\folder")

        if (not objFolder2 is nothing) then
            dim nReturn

            nReturn = objFolder2.OfflineStatus
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="faf50-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="faf50-126">Visual Basic:</span></span>


```VB
Private Sub fnOfflineStatusVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("\\server\share\folder")

    If (Not objFolder2 Is Nothing) Then
        Dim nReturn As Integer
        
        nReturn = objFolder2.OfflineStatus()
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="faf50-127">Требования</span><span class="sxs-lookup"><span data-stu-id="faf50-127">Requirements</span></span>



| <span data-ttu-id="faf50-128">Требование</span><span class="sxs-lookup"><span data-stu-id="faf50-128">Requirement</span></span> | <span data-ttu-id="faf50-129">Значение</span><span class="sxs-lookup"><span data-stu-id="faf50-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faf50-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="faf50-130">Minimum supported client</span></span><br/> | <span data-ttu-id="faf50-131">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="faf50-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="faf50-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="faf50-132">Minimum supported server</span></span><br/> | <span data-ttu-id="faf50-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="faf50-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="faf50-134">Header</span><span class="sxs-lookup"><span data-stu-id="faf50-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="faf50-135"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="faf50-135"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="faf50-136">IDL</span><span class="sxs-lookup"><span data-stu-id="faf50-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="faf50-137"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="faf50-137"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="faf50-138">DLL</span><span class="sxs-lookup"><span data-stu-id="faf50-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="faf50-139"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="faf50-139"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faf50-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="faf50-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faf50-141">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="faf50-141">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="faf50-142">**Папка**</span><span class="sxs-lookup"><span data-stu-id="faf50-142">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




