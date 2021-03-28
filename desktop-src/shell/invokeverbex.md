---
description: Выполняет команду для элемента оболочки.
ms.assetid: aac3f338-6074-4b1f-9b2f-e6206db52419
title: Шеллфолдеритем. Инвокевербекс, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 627c2b40869ac9c509dcd645ec259de7db118235
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984740"
---
# <a name="shellfolderiteminvokeverbex-method"></a><span data-ttu-id="656fd-103">Шеллфолдеритем. Инвокевербекс, метод</span><span class="sxs-lookup"><span data-stu-id="656fd-103">ShellFolderItem.InvokeVerbEx method</span></span>

<span data-ttu-id="656fd-104">Выполняет команду для элемента оболочки.</span><span class="sxs-lookup"><span data-stu-id="656fd-104">Executes a verb on a Shell item.</span></span>

## <a name="syntax"></a><span data-ttu-id="656fd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="656fd-105">Syntax</span></span>


```JScript
iRetVal = ShellFolderItem.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a><span data-ttu-id="656fd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="656fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="656fd-107">*вверб* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="656fd-107">*vVerb* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="656fd-108">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="656fd-108">Type: **Variant**</span></span>

<span data-ttu-id="656fd-109">**Значение типа Variant** , содержащее строку команды, соответствующую выполняемой команде.</span><span class="sxs-lookup"><span data-stu-id="656fd-109">A **Variant** that contains the verb string that corresponds to the command to be executed.</span></span> <span data-ttu-id="656fd-110">Оно должно быть одним из значений, возвращаемых свойством [**Name**](folderitemverb-name.md) элемента.</span><span class="sxs-lookup"><span data-stu-id="656fd-110">It must be one of the values returned by the item's [**Name**](folderitemverb-name.md) property.</span></span> <span data-ttu-id="656fd-111">Если команда не указана, выполняется команда по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="656fd-111">If no verb is specified, the default verb is executed.</span></span>

</dd> <dt>

<span data-ttu-id="656fd-112">*варгс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="656fd-112">*vArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="656fd-113">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="656fd-113">Type: **Variant**</span></span>

<span data-ttu-id="656fd-114">**Вариант** , состоящий из строки с одним или несколькими аргументами команды, заданной параметром *вверб*.</span><span class="sxs-lookup"><span data-stu-id="656fd-114">A **Variant** that consists of a string with one or more arguments to the command specified by *vVerb*.</span></span> <span data-ttu-id="656fd-115">Формат этой строки зависит от конкретной команды.</span><span class="sxs-lookup"><span data-stu-id="656fd-115">The format of this string depends on the particular verb.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="656fd-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="656fd-116">Remarks</span></span>

<span data-ttu-id="656fd-117">Глагол — это строка, используемая для указания конкретного действия, которое поддерживает элемент.</span><span class="sxs-lookup"><span data-stu-id="656fd-117">A verb is a string used to specify a particular action that an item supports.</span></span> <span data-ttu-id="656fd-118">Как правило, вызов команды запускает связанное приложение.</span><span class="sxs-lookup"><span data-stu-id="656fd-118">Typically, calling a verb launches a related application.</span></span> <span data-ttu-id="656fd-119">Например, вызов команды **Open** для TXT-файла обычно открывает файл в текстовом редакторе, обычно Microsoft Notepad.</span><span class="sxs-lookup"><span data-stu-id="656fd-119">For example, calling the **open** verb on a .txt file normally opens the file with a text editor, usually Microsoft Notepad.</span></span> <span data-ttu-id="656fd-120">Объект [**фолдеритемвербс**](folderitemverbs.md) представляет коллекцию команд, связанных с элементом.</span><span class="sxs-lookup"><span data-stu-id="656fd-120">The [**FolderItemVerbs**](folderitemverbs.md) object represents the collection of verbs associated with the item.</span></span> <span data-ttu-id="656fd-121">Дальнейшее обсуждение глаголов см. в разделе [Запуск приложений](launch.md).</span><span class="sxs-lookup"><span data-stu-id="656fd-121">For further discussion of verbs, see [Launching Applications](launch.md).</span></span>

<span data-ttu-id="656fd-122">Этот метод аналогичен [**инвокеверб**](folderitem-invokeverb.md), но он позволяет задавать аргументы для команды, а также саму команду.</span><span class="sxs-lookup"><span data-stu-id="656fd-122">This method is similar to [**InvokeVerb**](folderitem-invokeverb.md), but it allows you to specify arguments to the command as well as the command itself.</span></span>

## <a name="examples"></a><span data-ttu-id="656fd-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="656fd-123">Examples</span></span>

<span data-ttu-id="656fd-124">В следующих примерах показано правильное использование этого метода в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="656fd-124">The following examples show the proper use of this method in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="656fd-125">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="656fd-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItem2InvokeVerbExJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                objFolderItem.InvokeVerbEx("open", "c:\\autoexec.bat");
            }
        }
    }
</script>
```



<span data-ttu-id="656fd-126">Сценариев</span><span class="sxs-lookup"><span data-stu-id="656fd-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    objFolderItem.InvokeVerbEx()
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="656fd-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="656fd-127">Visual Basic:</span></span>


```VB
Private Sub fnFolderItem2InvokeVerbExVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem2 As Object
            
            Set objFolderItem2 = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem2 Is Nothing) Then
                    objFolderItem2.InvokeVerbEx ("open")
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem2 = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="656fd-128">Требования</span><span class="sxs-lookup"><span data-stu-id="656fd-128">Requirements</span></span>



| <span data-ttu-id="656fd-129">Требование</span><span class="sxs-lookup"><span data-stu-id="656fd-129">Requirement</span></span> | <span data-ttu-id="656fd-130">Значение</span><span class="sxs-lookup"><span data-stu-id="656fd-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="656fd-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="656fd-131">Minimum supported client</span></span><br/> | <span data-ttu-id="656fd-132">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="656fd-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="656fd-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="656fd-133">Minimum supported server</span></span><br/> | <span data-ttu-id="656fd-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="656fd-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="656fd-135">Header</span><span class="sxs-lookup"><span data-stu-id="656fd-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="656fd-136"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="656fd-136"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="656fd-137">IDL</span><span class="sxs-lookup"><span data-stu-id="656fd-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="656fd-138"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="656fd-138"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="656fd-139">DLL</span><span class="sxs-lookup"><span data-stu-id="656fd-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="656fd-140"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="656fd-140"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="656fd-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="656fd-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="656fd-142">**шеллфолдеритем**</span><span class="sxs-lookup"><span data-stu-id="656fd-142">**ShellFolderItem**</span></span>](shellfolderitem-object.md)
</dt> <dt>

[<span data-ttu-id="656fd-143">**инвокеверб**</span><span class="sxs-lookup"><span data-stu-id="656fd-143">**InvokeVerb**</span></span>](folderitem-invokeverb.md)
</dt> </dl>

 

 




