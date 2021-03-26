---
description: 'Отображает диалоговое окно Поиск: все файлы. Это то же самое, что и при щелчке в меню Пуск, а затем выбрав поиск.'
ms.assetid: 6F588D5E-5B6E-4000-BAD5-B557FB975FCA
title: Ишеллдиспатч. Финдфилес, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FindFiles
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9a9ea407d0ceccfe7706ed481aa80bcda9405ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897914"
---
# <a name="ishelldispatchfindfiles-method"></a><span data-ttu-id="f0d3a-104">Ишеллдиспатч. Финдфилес, метод</span><span class="sxs-lookup"><span data-stu-id="f0d3a-104">IShellDispatch.FindFiles method</span></span>

<span data-ttu-id="f0d3a-105">Отображает диалоговое окно **Поиск: все файлы** .</span><span class="sxs-lookup"><span data-stu-id="f0d3a-105">Displays the **Find: All Files** dialog box.</span></span> <span data-ttu-id="f0d3a-106">Это то же самое, что и при щелчке в меню **Пуск** , а затем выбрав **Поиск**.</span><span class="sxs-lookup"><span data-stu-id="f0d3a-106">This is the same as clicking the **Start** menu and then selecting **Search**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0d3a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0d3a-107">Syntax</span></span>


```JScript
IShellDispatch.FindFiles()
```


```VB

IShellDispatch.FindFiles()
```





## <a name="parameters"></a><span data-ttu-id="f0d3a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0d3a-108">Parameters</span></span>

<span data-ttu-id="f0d3a-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="f0d3a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f0d3a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0d3a-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f0d3a-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="f0d3a-111">JScript</span></span>

<span data-ttu-id="f0d3a-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f0d3a-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="f0d3a-113">VB</span><span class="sxs-lookup"><span data-stu-id="f0d3a-113">VB</span></span>

<span data-ttu-id="f0d3a-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f0d3a-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0d3a-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="f0d3a-115">Remarks</span></span>

<span data-ttu-id="f0d3a-116">Этот метод реализован и доступен через метод [**Shell. финдфилес**](shell-findfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="f0d3a-116">This method is implemented and accessed through the [**Shell.FindFiles**](shell-findfiles.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="f0d3a-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="f0d3a-117">Examples</span></span>

<span data-ttu-id="f0d3a-118">В следующих примерах показано использование **финдфилес** в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f0d3a-118">The following examples show the use of **FindFiles** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f0d3a-119">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="f0d3a-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindFilesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindFiles();
    }
</script>
```



<span data-ttu-id="f0d3a-120">Сценариев</span><span class="sxs-lookup"><span data-stu-id="f0d3a-120">VBScript:</span></span>


```VB
<script language="VBScript">
   function fnShellFindFilesVB()
       dim objShell
       
       set objShell = CreateObject("shell.application")
       objshell.FindFiles

       set objShell = nothing
   end function
</script>
```



<span data-ttu-id="f0d3a-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="f0d3a-121">Visual Basic:</span></span>


```VB
Private Sub fnShellFindFilesVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindFiles

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f0d3a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="f0d3a-122">Requirements</span></span>



| <span data-ttu-id="f0d3a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="f0d3a-123">Requirement</span></span> | <span data-ttu-id="f0d3a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f0d3a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0d3a-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0d3a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f0d3a-126">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f0d3a-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f0d3a-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0d3a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f0d3a-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f0d3a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f0d3a-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f0d3a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0d3a-130"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0d3a-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f0d3a-131">IDL</span><span class="sxs-lookup"><span data-stu-id="f0d3a-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f0d3a-132"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f0d3a-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f0d3a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f0d3a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0d3a-134"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="f0d3a-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




