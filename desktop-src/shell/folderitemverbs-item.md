---
description: Извлекает объект Фолдеритемверб для указанного элемента в коллекции.
ms.assetid: 65871926-0920-4ad6-82da-7aba0a3c0fab
title: Метод Фолдеритемвербс. Item (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 013215af3f5005e68b396312d0ef13fa974d8a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985489"
---
# <a name="folderitemverbsitem-method"></a><span data-ttu-id="b7269-103">Фолдеритемвербс. Item, метод</span><span class="sxs-lookup"><span data-stu-id="b7269-103">FolderItemVerbs.Item method</span></span>

<span data-ttu-id="b7269-104">Извлекает объект [**фолдеритемверб**](folderitemverb.md) для указанного элемента в коллекции.</span><span class="sxs-lookup"><span data-stu-id="b7269-104">Retrieves the [**FolderItemVerb**](folderitemverb.md) object for a specified item in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7269-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7269-105">Syntax</span></span>


```JScript
retVal = FolderItemVerbs.Item(
  iIndex
)
```



## <a name="parameters"></a><span data-ttu-id="b7269-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b7269-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7269-107">*ииндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b7269-107">*iIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7269-108">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="b7269-108">Type: **Variant**</span></span>

<span data-ttu-id="b7269-109">Начинающийся с нуля индекс извлекаемого элемента.</span><span class="sxs-lookup"><span data-stu-id="b7269-109">The zero-based index of the item to retrieve.</span></span> <span data-ttu-id="b7269-110">Это значение должно быть меньше значения свойства [**Count**](folderitemverbs-count.md) .</span><span class="sxs-lookup"><span data-stu-id="b7269-110">This value must be less than the value of the [**Count**](folderitemverbs-count.md) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7269-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b7269-111">Return value</span></span>

<span data-ttu-id="b7269-112">Тип: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="b7269-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="b7269-113">Объект, который получает объект [**фолдеритемверб**](folderitemverb.md) .</span><span class="sxs-lookup"><span data-stu-id="b7269-113">Object that receives the [**FolderItemVerb**](folderitemverb.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="b7269-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="b7269-114">Examples</span></span>

<span data-ttu-id="b7269-115">В следующем примере **элемент** используется для получения первых команд из коллекции, доступной в папке панели управления, и отображается ее имя.</span><span class="sxs-lookup"><span data-stu-id="b7269-115">The following example uses **Item** to retrieve the first verbs in the collection available to the Control Panel folder and displays its name.</span></span> <span data-ttu-id="b7269-116">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b7269-116">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b7269-117">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="b7269-117">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfCONTROLS = 3;
        
        objFolder2 = objShell.NameSpace(ssfCONTROLS);

        if (objFolder2 != null)
        {
            var objVerbs;
            objVerbs = objFolder2.Self.Verbs();
 
            if (objVerbs != null)
            {
                var objFolderItemVerb;
                objFolderItemVerb = objVerbs.Item(0);
 
                if (objFolderItemVerb != null)
                {
                    alert(objFolderItemVerb.Name);
                }
            }
        }
    }
</script>
```



<span data-ttu-id="b7269-118">Сценариев</span><span class="sxs-lookup"><span data-stu-id="b7269-118">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemVerbsItemVB()
        dim objShell
        dim objFolder2
        dim ssfCONTROLS
        
        ssfCONTROLS = 3
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace(ssfCONTROLS)
        if (not objFolder2 is nothing) then
            dim objVerbs
            set objVerbs = objFolder2.Self.Verbs

            if (not objVerbs is nothing) then
                dim objFolderItemVerb
                set objFolderItemVerb = objVerbs.Item(0)

                if (not objFolderItemVerb is nothing) then
                    alert(objFolderItemVerb.Name)
                end if

                set objFolderItemVerb = nothing
            end if

            set objVerbs = nothing
        end if

        set objFolder2 = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="b7269-119">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b7269-119">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemVerbsItemVB()
    Dim objShell    As Shell
    Dim objFolder2  As Folder2
    Dim ssfCONTROLS As Long
            
    ssfCONTROLS = 3
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfPROGRAMS)

    If (Not objFolder2 Is Nothing) Then
        Dim objVerbs As FolderItemVerbs
        Set objVerbs = objFolder2.Self.Verbs

        If (Not objVerbs Is Nothing) Then
            Dim objFolderItemVerb As FolderItemVerb
            Set objFolderItemVerb = objVerbs.Item(0)

            If (Not objFolderItemVerb Is Nothing) Then
                Debug.Print objFolderItemVerb.Name
            End If

            Set objFolderItemVerb = Nothing
        End If

        Set objVerbs = Nothing
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b7269-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b7269-120">Requirements</span></span>



| <span data-ttu-id="b7269-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b7269-121">Requirement</span></span> | <span data-ttu-id="b7269-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b7269-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7269-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7269-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b7269-124">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b7269-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b7269-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7269-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b7269-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b7269-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b7269-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b7269-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7269-128"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7269-128"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b7269-129">IDL</span><span class="sxs-lookup"><span data-stu-id="b7269-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b7269-130"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b7269-130"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b7269-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b7269-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7269-132"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="b7269-132"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
