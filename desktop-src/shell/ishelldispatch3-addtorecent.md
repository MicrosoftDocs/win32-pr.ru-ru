---
description: IShellDispatch3. Аддторецент, метод — добавляет файл в список последних использованных файлов.
ms.assetid: aa5aef31-7f3f-4cc4-949d-1484de243ef3
title: IShellDispatch3. Аддторецент, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch3.AddToRecent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8d31d05e9eef889d9018e4806cf4c882dba3060e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116932"
---
# <a name="ishelldispatch3addtorecent-method"></a><span data-ttu-id="84556-103">IShellDispatch3. Аддторецент, метод</span><span class="sxs-lookup"><span data-stu-id="84556-103">IShellDispatch3.AddToRecent method</span></span>

<span data-ttu-id="84556-104">Добавляет файл в список последних использованных файлов (MRU).</span><span class="sxs-lookup"><span data-stu-id="84556-104">Adds a file to the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="84556-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84556-105">Syntax</span></span>


```JScript
IShellDispatch3.AddToRecent(
  varFile,
  [ bstrCategory ]
)
```


```VB

IShellDispatch3.AddToRecent( _
  ByVal varFile As Variant, _
  [ ByVal bstrCategory As BSTR ] _
)
```





## <a name="parameters"></a><span data-ttu-id="84556-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="84556-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84556-107">*варфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84556-107">*varFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84556-108">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="84556-108">Type: **Variant**</span></span>

<span data-ttu-id="84556-109">**Строка** , содержащая путь к файлу, добавляемому в список недавно использовавшихся документов.</span><span class="sxs-lookup"><span data-stu-id="84556-109">A **String** that contains the path of the file to add to the list of recently used documents.</span></span>

<span data-ttu-id="84556-110">**Windows Vista**: установите для этого параметра **значение NULL** , чтобы очистить папку недавние документы.</span><span class="sxs-lookup"><span data-stu-id="84556-110">**Windows Vista**: Set this parameter to **null** to clear the recent documents folder.</span></span>

</dd> <dt>

<span data-ttu-id="84556-111">*бстркатегори* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="84556-111">*bstrCategory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="84556-112">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="84556-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="84556-113">**Строка** , содержащая имя категории, в которую следует поместить файл.</span><span class="sxs-lookup"><span data-stu-id="84556-113">A **String** that contains the name of the category in which to place the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84556-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84556-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="84556-115">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="84556-115">JScript</span></span>

<span data-ttu-id="84556-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="84556-116">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="84556-117">VB</span><span class="sxs-lookup"><span data-stu-id="84556-117">VB</span></span>

<span data-ttu-id="84556-118">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="84556-118">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="84556-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="84556-119">Examples</span></span>

<span data-ttu-id="84556-120">В следующих примерах показано использование **аддторецент** для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="84556-120">The following examples show the use of **AddToRecent** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="84556-121">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="84556-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch3AddToRecentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("system.ini");
            if (objFolderItem != null)
            {
                objShell.AddToRecent(objFolderItem.Path);
            }
        }
    }
</script>
```



<span data-ttu-id="84556-122">Сценариев</span><span class="sxs-lookup"><span data-stu-id="84556-122">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch3AddToRecentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
            
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder.ParseName("system.ini")
                if (not objFolderItem is nothing) then
                    objShell.AddToRecent (objFolderItem.Path)
                end if
                set objFolderItem = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="84556-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="84556-123">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch3AddToRecent()
    Dim objShell  As Shell
    Dim objFolder As Folder
    Dim ssfWINDOWS As Long

    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem

        Set objFolderItem = objFolder.ParseName("system.ini")
        If (Not objFolderItem Is Nothing) Then
            objShell.AddToRecent (objFolderItem.Path)
        End If
        Set objFolderItem = Nothing
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="84556-124">Требования</span><span class="sxs-lookup"><span data-stu-id="84556-124">Requirements</span></span>



| <span data-ttu-id="84556-125">Требование</span><span class="sxs-lookup"><span data-stu-id="84556-125">Requirement</span></span> | <span data-ttu-id="84556-126">Значение</span><span class="sxs-lookup"><span data-stu-id="84556-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84556-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84556-127">Minimum supported client</span></span><br/> | <span data-ttu-id="84556-128">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="84556-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="84556-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84556-129">Minimum supported server</span></span><br/> | <span data-ttu-id="84556-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="84556-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="84556-131">Header</span><span class="sxs-lookup"><span data-stu-id="84556-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="84556-132"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="84556-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="84556-133">IDL</span><span class="sxs-lookup"><span data-stu-id="84556-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="84556-134"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="84556-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="84556-135">DLL</span><span class="sxs-lookup"><span data-stu-id="84556-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84556-136"><dt>Shell32.dll (версия 6,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="84556-136"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
