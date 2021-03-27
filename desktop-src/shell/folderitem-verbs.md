---
description: Извлекает объект Фолдеритемвербс элемента. Этот объект представляет собой коллекцию команд, которые могут быть выполнены для элемента.
ms.assetid: e31160cd-093a-45a6-a066-58120c44eb2c
title: Метод FolderItem. Verbs (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Verbs
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f15c2471f749748f7928a45aa03037d955c75d4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143039"
---
# <a name="folderitemverbs-method"></a><span data-ttu-id="a57a8-104">FolderItem. Verbs, метод</span><span class="sxs-lookup"><span data-stu-id="a57a8-104">FolderItem.Verbs method</span></span>

<span data-ttu-id="a57a8-105">Извлекает объект [**фолдеритемвербс**](folderitemverbs.md) элемента.</span><span class="sxs-lookup"><span data-stu-id="a57a8-105">Retrieves the item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span> <span data-ttu-id="a57a8-106">Этот объект представляет собой коллекцию команд, которые могут быть выполнены для элемента.</span><span class="sxs-lookup"><span data-stu-id="a57a8-106">This object is the collection of verbs that can be executed on the item.</span></span>

## <a name="syntax"></a><span data-ttu-id="a57a8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a57a8-107">Syntax</span></span>


```JScript
retVal = FolderItem.Verbs()
```



## <a name="parameters"></a><span data-ttu-id="a57a8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a57a8-108">Parameters</span></span>

<span data-ttu-id="a57a8-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a57a8-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a57a8-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a57a8-110">Return value</span></span>

<span data-ttu-id="a57a8-111">Тип: **[ **фолдеритемвербс**](folderitemverbs.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a57a8-111">Type: **[**FolderItemVerbs**](folderitemverbs.md)\*\***</span></span>

<span data-ttu-id="a57a8-112">Ссылка на объект [**фолдеритемвербс**](folderitemverbs.md) .</span><span class="sxs-lookup"><span data-stu-id="a57a8-112">An object reference to the [**FolderItemVerbs**](folderitemverbs.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="a57a8-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="a57a8-113">Examples</span></span>

<span data-ttu-id="a57a8-114">В следующем примере **команды** используются для получения объекта [**фолдеритемвербс**](folderitemverbs.md) , представляющего набор команд, которые могут быть выполнены в папке Windows.</span><span class="sxs-lookup"><span data-stu-id="a57a8-114">The following example uses **Verbs** to retrieve the [**FolderItemVerbs**](folderitemverbs.md) object representing the set of verbs that can be executed on the Windows folder.</span></span> <span data-ttu-id="a57a8-115">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a57a8-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a57a8-116">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="a57a8-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbsJ()
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
                var objItemVerbs;
                
                objItemVerbs = objFolderItem.Verbs();
                if (objItemVerbs != null)
                {
                    // Add code here
                }
            }
        }
    }
</script>
```



<span data-ttu-id="a57a8-117">Сценариев</span><span class="sxs-lookup"><span data-stu-id="a57a8-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemVerbsVB()
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
                    dim objItemVerbs
                    
                    set objItemVerbs = objFolderItem.Verbs
                        if (not objItemVerbs is nothing) then
                            'Add code here
                        end if
                    set objItemVerbs = nothing
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="a57a8-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="a57a8-118">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemVerbsVB()
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
                    Dim objItemVerbs As FolderItemVerbs
                    
                    Set objItemVerbs = objFolderItem.Verbs
                        If (Not objItemVerbs Is Nothing) Then
                            'Add code here
                        End If
                    Set objItemVerbs = Nothing
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



## <a name="requirements"></a><span data-ttu-id="a57a8-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a57a8-119">Requirements</span></span>



| <span data-ttu-id="a57a8-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a57a8-120">Requirement</span></span> | <span data-ttu-id="a57a8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a57a8-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a57a8-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a57a8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a57a8-123">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a57a8-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a57a8-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a57a8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a57a8-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a57a8-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a57a8-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a57a8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a57a8-127"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a57a8-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a57a8-128">IDL</span><span class="sxs-lookup"><span data-stu-id="a57a8-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a57a8-129"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a57a8-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a57a8-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a57a8-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a57a8-131"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="a57a8-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a57a8-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a57a8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a57a8-133">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="a57a8-133">**FolderItem**</span></span>](folderitem.md)
</dt> <dt>

[<span data-ttu-id="a57a8-134">**инвокеверб**</span><span class="sxs-lookup"><span data-stu-id="a57a8-134">**InvokeVerb**</span></span>](folderitem-invokeverb.md)
</dt> <dt>

[<span data-ttu-id="a57a8-135">**доит**</span><span class="sxs-lookup"><span data-stu-id="a57a8-135">**DoIt**</span></span>](folderitemverb-doit.md)
</dt> </dl>

 

 




