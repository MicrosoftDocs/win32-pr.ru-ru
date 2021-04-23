---
description: Выполняет команду для FolderItem, связанной с командой.
ms.assetid: 92400fe9-e4d1-4bc9-b4ee-d2adaf38154f
title: Фолдеритемверб. доит, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerb.DoIt
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0703b9403dfe9ff6600de68aaa710cd5a55c225a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984161"
---
# <a name="folderitemverbdoit-method"></a><span data-ttu-id="d4993-103">Фолдеритемверб. доит, метод</span><span class="sxs-lookup"><span data-stu-id="d4993-103">FolderItemVerb.DoIt method</span></span>

<span data-ttu-id="d4993-104">Выполняет команду для [**FolderItem**](folderitem.md) , связанной с командой.</span><span class="sxs-lookup"><span data-stu-id="d4993-104">Executes a verb on the [**FolderItem**](folderitem.md) associated with the verb.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4993-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4993-105">Syntax</span></span>


```JScript
FolderItemVerb.DoIt()
```



## <a name="parameters"></a><span data-ttu-id="d4993-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4993-106">Parameters</span></span>

<span data-ttu-id="d4993-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d4993-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d4993-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d4993-108">Return value</span></span>

<span data-ttu-id="d4993-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d4993-109">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="d4993-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="d4993-110">Examples</span></span>

<span data-ttu-id="d4993-111">В следующем примере используется **доит** для выполнения первой команды в коллекции команд, на которую реагирует папка программы пользователя.</span><span class="sxs-lookup"><span data-stu-id="d4993-111">The following example uses **DoIt** to execute the first verb in the collection of verbs to which the user's Program folder responds.</span></span> <span data-ttu-id="d4993-112">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d4993-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d4993-113">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="d4993-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbDoItJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objVerbs;
            
            objVerbs = objFolder.Self.Verbs();
            if (objVerbs != null)
            {
                objVerbs.Item(0).DoIt();
            }
        }
    }
</script>
```



<span data-ttu-id="d4993-114">Сценариев</span><span class="sxs-lookup"><span data-stu-id="d4993-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemVerbDoItVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objVerbs
                
                set objVerbs = objFolder.Self.Verbs
                    if (not objVerbs is nothing) then
                        objVerbs.Item(0).DoIt
                    end if
                set objVerbs = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="d4993-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="d4993-115">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemVerbDoItVB()
    Dim objShell    As Shell
    Dim objFolder2  As Folder2
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder2 Is Nothing) Then
        Dim objVerbs As FolderItemVerbs
        
        Set objVerbs = objFolder2.Self.Verbs
            If (Not objVerbs Is Nothing) Then
                objVerbs.Item(0).DoIt
            End If
        Set objVerbs = Nothing
    End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="d4993-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d4993-116">Requirements</span></span>



| <span data-ttu-id="d4993-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d4993-117">Requirement</span></span> | <span data-ttu-id="d4993-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d4993-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4993-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4993-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d4993-120">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d4993-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d4993-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4993-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d4993-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d4993-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d4993-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d4993-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4993-124"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4993-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d4993-125">IDL</span><span class="sxs-lookup"><span data-stu-id="d4993-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d4993-126"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d4993-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d4993-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d4993-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4993-128"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="d4993-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




