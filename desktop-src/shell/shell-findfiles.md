---
description: 'Отображает диалоговое окно Поиск: все файлы. Это то же самое, что и при нажатии кнопки «Пуск», а затем при выборе поиска (или его эквивалента в системах, предшествующих Windows XP.'
ms.assetid: cccdd3ea-b52a-4fbe-b4c5-1efc1dd6d770
title: Метод Shell. Финдфилес (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindFiles
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f3e6551dc41fd8d6a040ada8000f0b46e81a5dd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266178"
---
# <a name="shellfindfiles-method"></a><span data-ttu-id="b6b6f-104">Shell. Финдфилес, метод</span><span class="sxs-lookup"><span data-stu-id="b6b6f-104">Shell.FindFiles method</span></span>

<span data-ttu-id="b6b6f-105">Отображает диалоговое окно **Поиск: все файлы** .</span><span class="sxs-lookup"><span data-stu-id="b6b6f-105">Displays the **Find: All Files** dialog box.</span></span> <span data-ttu-id="b6b6f-106">Это то же самое, что и при нажатии кнопки « **Пуск** », а затем при выборе **поиска** (или его эквивалента в системах, предшествующих Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b6b6f-106">This is the same as clicking the **Start** menu and then selecting **Search** (or its equivalent under systems earlier than Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6b6f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6b6f-107">Syntax</span></span>


```JScript
Shell.FindFiles()
```


```VB

Shell.FindFiles()
```





## <a name="parameters"></a><span data-ttu-id="b6b6f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6b6f-108">Parameters</span></span>

<span data-ttu-id="b6b6f-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b6b6f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b6b6f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6b6f-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b6b6f-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="b6b6f-111">JScript</span></span>

<span data-ttu-id="b6b6f-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b6b6f-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="b6b6f-113">VB</span><span class="sxs-lookup"><span data-stu-id="b6b6f-113">VB</span></span>

<span data-ttu-id="b6b6f-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b6b6f-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="b6b6f-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="b6b6f-115">Examples</span></span>

<span data-ttu-id="b6b6f-116">В следующем примере показано использование **финдфилес** .</span><span class="sxs-lookup"><span data-stu-id="b6b6f-116">The following example shows **FindFiles** in use.</span></span> <span data-ttu-id="b6b6f-117">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b6b6f-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b6b6f-118">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="b6b6f-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindFilesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Shell_FindFiles();
    }
</script>
```



<span data-ttu-id="b6b6f-119">Сценариев</span><span class="sxs-lookup"><span data-stu-id="b6b6f-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFindFilesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.FindFiles

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="b6b6f-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b6b6f-120">Visual Basic:</span></span>


```VB
Private Sub fnShellFindFilesVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindFiles

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b6b6f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b6b6f-121">Requirements</span></span>



| <span data-ttu-id="b6b6f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b6b6f-122">Requirement</span></span> | <span data-ttu-id="b6b6f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b6b6f-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6b6f-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6b6f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b6b6f-125">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b6b6f-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b6b6f-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6b6f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b6b6f-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b6b6f-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b6b6f-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b6b6f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6b6f-129"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6b6f-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b6b6f-130">IDL</span><span class="sxs-lookup"><span data-stu-id="b6b6f-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b6b6f-131"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b6b6f-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b6b6f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b6b6f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6b6f-133"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="b6b6f-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




