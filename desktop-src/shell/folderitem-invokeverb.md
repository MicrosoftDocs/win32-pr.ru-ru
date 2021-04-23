---
description: Выполняет команду для элемента.
ms.assetid: 569bdc88-15ef-4d08-923c-4f41e5ae5a38
title: FolderItem. Инвокеверб, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.InvokeVerb
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 259ff9613756940d5da8a37585dbf39fb2dc0a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539512"
---
# <a name="folderiteminvokeverb-method"></a><span data-ttu-id="14b6b-103">FolderItem. Инвокеверб, метод</span><span class="sxs-lookup"><span data-stu-id="14b6b-103">FolderItem.InvokeVerb method</span></span>

<span data-ttu-id="14b6b-104">Выполняет команду для элемента.</span><span class="sxs-lookup"><span data-stu-id="14b6b-104">Executes a verb on the item.</span></span>

## <a name="syntax"></a><span data-ttu-id="14b6b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14b6b-105">Syntax</span></span>


```JScript
FolderItem.InvokeVerb(
  [ vVerb ]
)
```



## <a name="parameters"></a><span data-ttu-id="14b6b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="14b6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14b6b-107">*вверб* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="14b6b-107">*vVerb* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14b6b-108">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="14b6b-108">Type: **Variant**</span></span>

<span data-ttu-id="14b6b-109">Строка, указывающая выполняемую команду.</span><span class="sxs-lookup"><span data-stu-id="14b6b-109">A string that specifies the verb to be executed.</span></span> <span data-ttu-id="14b6b-110">Это должно быть одно из значений, возвращаемых свойством [**FolderItemVerb.Name**](folderitemverb-name.md) элемента.</span><span class="sxs-lookup"><span data-stu-id="14b6b-110">It must be one of the values returned by the item's [**FolderItemVerb.Name**](folderitemverb-name.md) property.</span></span> <span data-ttu-id="14b6b-111">Если команда не указана, будет вызвана команда по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="14b6b-111">If no verb is specified, the default verb will be invoked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14b6b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14b6b-112">Return value</span></span>

<span data-ttu-id="14b6b-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="14b6b-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="14b6b-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="14b6b-114">Remarks</span></span>

<span data-ttu-id="14b6b-115">Глагол — это строка, используемая для указания конкретного действия, которое поддерживает элемент.</span><span class="sxs-lookup"><span data-stu-id="14b6b-115">A verb is a string used to specify a particular action that an item supports.</span></span> <span data-ttu-id="14b6b-116">Вызов глагола эквивалентен выбору команды из контекстного меню элемента.</span><span class="sxs-lookup"><span data-stu-id="14b6b-116">Invoking a verb is equivalent to selecting a command from an item's shortcut menu.</span></span> <span data-ttu-id="14b6b-117">Как правило, вызов команды запускает связанное приложение.</span><span class="sxs-lookup"><span data-stu-id="14b6b-117">Typically, invoking a verb launches a related application.</span></span> <span data-ttu-id="14b6b-118">Например, при вызове команды "Открыть" для TXT-файла файл открывается в текстовом редакторе, обычно в Microsoft Notepad.</span><span class="sxs-lookup"><span data-stu-id="14b6b-118">For example, invoking the "open" verb on a .txt file opens the file with a text editor, usually Microsoft Notepad.</span></span> <span data-ttu-id="14b6b-119">Дополнительные сведения о командах см. в статье [Запуск приложений](launch.md) .</span><span class="sxs-lookup"><span data-stu-id="14b6b-119">See [Launching Applications](launch.md) for further discussion of verbs.</span></span>

<span data-ttu-id="14b6b-120">Объект [**фолдеритемвербс**](folderitemverbs.md) представляет коллекцию команд, связанных с элементом.</span><span class="sxs-lookup"><span data-stu-id="14b6b-120">The [**FolderItemVerbs**](folderitemverbs.md) object represents the collection of verbs associated with the item.</span></span> <span data-ttu-id="14b6b-121">Глагол по умолчанию может различаться для различных элементов, но обычно это "Open".</span><span class="sxs-lookup"><span data-stu-id="14b6b-121">The default verb may vary for different items, but it is typically "open".</span></span>

## <a name="examples"></a><span data-ttu-id="14b6b-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="14b6b-122">Examples</span></span>

<span data-ttu-id="14b6b-123">В следующем примере используется **инвокеверб** для вызова глагола по умолчанию (в данном случае "Open") в папке Windows.</span><span class="sxs-lookup"><span data-stu-id="14b6b-123">The following example uses **InvokeVerb** to invoke the default verb ("open" in this case) on the Windows folder.</span></span> <span data-ttu-id="14b6b-124">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="14b6b-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="14b6b-125">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="14b6b-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemInvokeVerbJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var szReturn;
                
                objFolderItem.InvokeVerb();
            }
        }
    }
</script>
```



<span data-ttu-id="14b6b-126">Сценариев</span><span class="sxs-lookup"><span data-stu-id="14b6b-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbVB()
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
                    dim szReturn
                                
                    objFolderItem.InvokeVerb()
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="14b6b-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="14b6b-127">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemInvokeVerbVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    objFolderItem.InvokeVerb
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="14b6b-128">Требования</span><span class="sxs-lookup"><span data-stu-id="14b6b-128">Requirements</span></span>



| <span data-ttu-id="14b6b-129">Требование</span><span class="sxs-lookup"><span data-stu-id="14b6b-129">Requirement</span></span> | <span data-ttu-id="14b6b-130">Значение</span><span class="sxs-lookup"><span data-stu-id="14b6b-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14b6b-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14b6b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="14b6b-132">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="14b6b-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="14b6b-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14b6b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="14b6b-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="14b6b-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="14b6b-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="14b6b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="14b6b-136"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="14b6b-136"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="14b6b-137">IDL</span><span class="sxs-lookup"><span data-stu-id="14b6b-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="14b6b-138"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="14b6b-138"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="14b6b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="14b6b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14b6b-140"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="14b6b-140"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14b6b-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14b6b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14b6b-142">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="14b6b-142">**FolderItem**</span></span>](folderitem.md)
</dt> <dt>

[<span data-ttu-id="14b6b-143">**Команды**</span><span class="sxs-lookup"><span data-stu-id="14b6b-143">**Verbs**</span></span>](folderitem-verbs.md)
</dt> <dt>

[<span data-ttu-id="14b6b-144">**доит**</span><span class="sxs-lookup"><span data-stu-id="14b6b-144">**DoIt**</span></span>](folderitemverb-doit.md)
</dt> </dl>

 

 




