---
description: Выполняет команду для коллекции объектов FolderItem. Этот метод является расширением метода Инвокеверб, что позволяет дополнительно управлять операцией с помощью набора флагов.
ms.assetid: 2c02985d-8877-4a02-a232-6aeb1716928c
title: FolderItems2. Инвокевербекс, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems2.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: aa9b986b5cb76f14cc950f522e1e289224c17b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984168"
---
# <a name="folderitems2invokeverbex-method"></a><span data-ttu-id="d678d-104">FolderItems2. Инвокевербекс, метод</span><span class="sxs-lookup"><span data-stu-id="d678d-104">FolderItems2.InvokeVerbEx method</span></span>

<span data-ttu-id="d678d-105">Выполняет команду для коллекции объектов [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="d678d-105">Executes a verb on a collection of [**FolderItem**](folderitem.md) objects.</span></span> <span data-ttu-id="d678d-106">Этот метод является расширением метода [**инвокеверб**](folderitem-invokeverb.md) , что позволяет дополнительно управлять операцией с помощью набора флагов.</span><span class="sxs-lookup"><span data-stu-id="d678d-106">This method is an extension of the [**InvokeVerb**](folderitem-invokeverb.md) method, allowing additional control of the operation through a set of flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="d678d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d678d-107">Syntax</span></span>


```JScript
iRetVal = FolderItems2.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a><span data-ttu-id="d678d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d678d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d678d-109">*вверб* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="d678d-109">*vVerb* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d678d-110">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="d678d-110">Type: **Variant**</span></span>

<span data-ttu-id="d678d-111">**Вариант** со строкой команды, соответствующей выполняемой команде.</span><span class="sxs-lookup"><span data-stu-id="d678d-111">A **Variant** with the verb string that corresponds to the command to be executed.</span></span> <span data-ttu-id="d678d-112">Если команда не указана, выполняется команда по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d678d-112">If no verb is specified, the default verb is executed.</span></span>

</dd> <dt>

<span data-ttu-id="d678d-113">*варгс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="d678d-113">*vArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d678d-114">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="d678d-114">Type: **Variant**</span></span>

<span data-ttu-id="d678d-115">**Вариант** , состоящий из строки с одним или несколькими аргументами команды, заданной параметром *вверб*.</span><span class="sxs-lookup"><span data-stu-id="d678d-115">A **Variant** that consists of a string with one or more arguments to the command specified by *vVerb*.</span></span> <span data-ttu-id="d678d-116">Формат этой строки зависит от конкретной команды.</span><span class="sxs-lookup"><span data-stu-id="d678d-116">The format of this string depends on the particular verb.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d678d-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="d678d-117">Remarks</span></span>

<span data-ttu-id="d678d-118">Глагол — это строка, используемая для указания конкретного действия, связанного с элементом или коллекцией элементов.</span><span class="sxs-lookup"><span data-stu-id="d678d-118">A verb is a string used to specify a particular action associated with an item or collection of items.</span></span> <span data-ttu-id="d678d-119">Как правило, вызов команды запускает связанное приложение.</span><span class="sxs-lookup"><span data-stu-id="d678d-119">Typically, calling a verb launches a related application.</span></span> <span data-ttu-id="d678d-120">Например, вызов команды **Open** для TXT-файла обычно открывает файл в текстовом редакторе, обычно Microsoft Notepad.</span><span class="sxs-lookup"><span data-stu-id="d678d-120">For example, calling the **open** verb on a .txt file normally opens the file with a text editor, usually Microsoft Notepad.</span></span> <span data-ttu-id="d678d-121">Дальнейшее обсуждение глаголов см. в разделе [Запуск приложений](launch.md).</span><span class="sxs-lookup"><span data-stu-id="d678d-121">For further discussion of verbs, see [Launching Applications](launch.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d678d-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="d678d-122">Examples</span></span>

<span data-ttu-id="d678d-123">В следующем примере **инвокевербекс** используется для вызова глагола по умолчанию ("Open") на **Мой компьютер**.</span><span class="sxs-lookup"><span data-stu-id="d678d-123">The following example uses **InvokeVerbEx** to invoke the default verb ("open") on **My Computer**.</span></span> <span data-ttu-id="d678d-124">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d678d-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d678d-125">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="d678d-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItems2InvokeVerbExJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder;
        var ssfDRIVES = 17;
        
        objFolder = objShell.NameSpace(ssfDRIVES);
        if (objFolder != null)
        {
            var objFolderItems2;
            
            objFolderItems2 = objFolder.Items();
            if (objFolderItems2 != null)
            {
                objFolderItems2.InvokeVerbEx();
            }
        }
    }
</script>
```



<span data-ttu-id="d678d-126">Сценариев</span><span class="sxs-lookup"><span data-stu-id="d678d-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItems2InvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfDRIVES
                
            ssfWINDOWS = 17
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems2
                        
                set objFolderItems2 = objFolder.Items()
                if (not objFolderItems2 is nothing) then
                    objFolderItems2.InvokeVerbEx
                end if
                set objFolderItems2 = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="d678d-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="d678d-127">Visual Basic:</span></span>


```VB
Private Sub fnFolderItems2InvokeVerbExVB()
    Dim objShell      As Shell
    Dim objFolder     As Folder2
    Dim ssfDRIVES     As Long
    
    ssfDRIVES = 17
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfDRIVES)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems2 As FolderItems
            
            Set objFolderItems2 = objFolder.Items
                If (Not objFolderItems2 Is Nothing) Then
                    objFolderItems2.InvokeVerbEx
                End If
            Set objFolderItems2 = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="d678d-128">Требования</span><span class="sxs-lookup"><span data-stu-id="d678d-128">Requirements</span></span>



| <span data-ttu-id="d678d-129">Требование</span><span class="sxs-lookup"><span data-stu-id="d678d-129">Requirement</span></span> | <span data-ttu-id="d678d-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d678d-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d678d-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d678d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d678d-132">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d678d-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d678d-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d678d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d678d-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d678d-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d678d-135">Header</span><span class="sxs-lookup"><span data-stu-id="d678d-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d678d-136"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="d678d-136"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="d678d-137">IDL</span><span class="sxs-lookup"><span data-stu-id="d678d-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d678d-138"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d678d-138"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="d678d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d678d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d678d-140"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="d678d-140"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d678d-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d678d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d678d-142">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="d678d-142">**FolderItems2**</span></span>](folderitems2-object.md)
</dt> <dt>

[<span data-ttu-id="d678d-143">**инвокеверб**</span><span class="sxs-lookup"><span data-stu-id="d678d-143">**InvokeVerb**</span></span>](folderitem-invokeverb.md)
</dt> </dl>

 

 




