---
description: Создает диалоговое окно, которое позволяет пользователю выбрать папку, а затем возвращает объект папки выбранной папки.
title: Метод Shell. Бровсефорфолдер (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.BrowseForFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 4cc44e5a-3578-448b-9b19-1b71e1ae2cb9
ms.openlocfilehash: 7e14dffbfb9ab3e18bd4d8e11ffaf4768ad53131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081032"
---
# <a name="shellbrowseforfolder-method"></a><span data-ttu-id="9715c-103">Shell. Бровсефорфолдер, метод</span><span class="sxs-lookup"><span data-stu-id="9715c-103">Shell.BrowseForFolder method</span></span>

<span data-ttu-id="9715c-104">Создает диалоговое окно, которое позволяет пользователю выбрать папку, а затем возвращает объект [**папки**](folder.md) выбранной папки.</span><span class="sxs-lookup"><span data-stu-id="9715c-104">Creates a dialog box that enables the user to select a folder and then returns the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9715c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9715c-105">Syntax</span></span>


```JScript
retVal = Shell.BrowseForFolder(
  Hwnd,
  sTitle,
  iOptions,
  [ vRootFolder ]
)
```


```VB

Shell.BrowseForFolder( _
  ByVal Hwnd As Integer, _
  ByVal sTitle As BSTR, _
  ByVal iOptions As Integer, _
  [ ByVal vRootFolder As Variant ] _
) As FOLDER
```





## <a name="parameters"></a><span data-ttu-id="9715c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9715c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9715c-107">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9715c-107">*Hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9715c-108">Тип: **Integer**</span><span class="sxs-lookup"><span data-stu-id="9715c-108">Type: **Integer**</span></span>

<span data-ttu-id="9715c-109">Маркер родительского окна диалогового поля.</span><span class="sxs-lookup"><span data-stu-id="9715c-109">The handle to the parent window of the dialog box.</span></span> <span data-ttu-id="9715c-110">Это значение может быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="9715c-110">This value can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9715c-111">*ститле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9715c-111">*sTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9715c-112">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="9715c-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="9715c-113">**Строковое** значение, представляющее заголовок, отображаемый в диалоговом окне **Обзор** .</span><span class="sxs-lookup"><span data-stu-id="9715c-113">A **String** value that represents the title displayed inside the **Browse** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="9715c-114">*иоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9715c-114">*iOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9715c-115">Тип: **Integer**</span><span class="sxs-lookup"><span data-stu-id="9715c-115">Type: **Integer**</span></span>

<span data-ttu-id="9715c-116">**Целочисленное** значение, содержащее параметры для метода.</span><span class="sxs-lookup"><span data-stu-id="9715c-116">An **Integer** value that contains the options for the method.</span></span> <span data-ttu-id="9715c-117">Это может быть ноль или сочетание значений, перечисленных под элементом **улфлагс** структуры [**бровсеинфо**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) .</span><span class="sxs-lookup"><span data-stu-id="9715c-117">This can be zero or a combination of the values listed under the **ulFlags** member of the [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9715c-118">*врутфолдер* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="9715c-118">*vRootFolder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9715c-119">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="9715c-119">Type: **Variant**</span></span>

<span data-ttu-id="9715c-120">Корневая папка, используемая в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="9715c-120">The root folder to use in the dialog box.</span></span> <span data-ttu-id="9715c-121">Пользователь не может просматривать выше в дереве, чем эта папка.</span><span class="sxs-lookup"><span data-stu-id="9715c-121">The user cannot browse higher in the tree than this folder.</span></span> <span data-ttu-id="9715c-122">Если это значение не указано, в качестве корневой папки, используемой в диалоговом окне, используется рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="9715c-122">If this value is not specified, the root folder used in the dialog box is the desktop.</span></span> <span data-ttu-id="9715c-123">Это значение может быть строкой, указывающей путь к папке или одно из значений [**шеллспеЦиалфолдерконстантс**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="9715c-123">This value can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="9715c-124">Обратите внимание, что имена констант, найденные в **шеллспеЦиалфолдерконстантс** , доступны в Visual Basic, но не в VBScript или JScript.</span><span class="sxs-lookup"><span data-stu-id="9715c-124">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="9715c-125">В таких случаях необходимо использовать числовые значения на своем месте.</span><span class="sxs-lookup"><span data-stu-id="9715c-125">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9715c-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9715c-126">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="9715c-127">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="9715c-127">JScript</span></span>

<span data-ttu-id="9715c-128">Тип: **Папка \* \***</span><span class="sxs-lookup"><span data-stu-id="9715c-128">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="9715c-129">Ссылка на объект [**папки**](folder.md) выбранной папки.</span><span class="sxs-lookup"><span data-stu-id="9715c-129">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="9715c-130">VB</span><span class="sxs-lookup"><span data-stu-id="9715c-130">VB</span></span>

<span data-ttu-id="9715c-131">Тип: **Папка \* \***</span><span class="sxs-lookup"><span data-stu-id="9715c-131">Type: **FOLDER\*\***</span></span>

<span data-ttu-id="9715c-132">Ссылка на объект [**папки**](folder.md) выбранной папки.</span><span class="sxs-lookup"><span data-stu-id="9715c-132">An object reference to the selected folder's [**Folder**](folder.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="9715c-133">Примеры</span><span class="sxs-lookup"><span data-stu-id="9715c-133">Examples</span></span>

<span data-ttu-id="9715c-134">В следующем примере используется **бровсефорфолдер** для вывода окна обзора, озаглавленного "example", в папке Windows.</span><span class="sxs-lookup"><span data-stu-id="9715c-134">The following example uses **BrowseForFolder** to display a browse window titled "Example" rooted at the Windows folder.</span></span> <span data-ttu-id="9715c-135">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9715c-135">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="9715c-136">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="9715c-136">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellBrowseForFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS);
        if (objFolder != null)
        {
            // Add code here.
        }
    }
</script>
```



<span data-ttu-id="9715c-137">Сценариев</span><span class="sxs-lookup"><span data-stu-id="9715c-137">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellBrowseForFolderVB()
        dim objShell
        dim ssfWINDOWS
        dim objFolder
        
        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
            set objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
                if (not objFolder is nothing) then
                    'Add code here.
                end if
            set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="9715c-138">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="9715c-138">Visual Basic:</span></span>


```VB
Private Sub fnShellBrowseForFolderVB()
    Dim objShell   As Shell
    Dim ssfWINDOWS As Long
    Dim objFolder  As Folder
    
    ssfWINDOWS = 36
    Set objShell = New Shell
        Set objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
            If (Not objFolder Is Nothing) Then
                'Add code here
            End If
        Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="9715c-139">Требования</span><span class="sxs-lookup"><span data-stu-id="9715c-139">Requirements</span></span>



| <span data-ttu-id="9715c-140">Требование</span><span class="sxs-lookup"><span data-stu-id="9715c-140">Requirement</span></span> | <span data-ttu-id="9715c-141">Значение</span><span class="sxs-lookup"><span data-stu-id="9715c-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9715c-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9715c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9715c-143">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9715c-143">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9715c-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9715c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9715c-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9715c-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9715c-146">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9715c-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="9715c-147"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="9715c-147"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="9715c-148">IDL</span><span class="sxs-lookup"><span data-stu-id="9715c-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9715c-149"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9715c-149"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="9715c-150">DLL</span><span class="sxs-lookup"><span data-stu-id="9715c-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9715c-151"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="9715c-151"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
