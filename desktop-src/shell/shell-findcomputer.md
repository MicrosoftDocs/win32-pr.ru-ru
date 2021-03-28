---
description: 'Отображает диалоговое окно Результаты поиска: компьютеры. В диалоговом окне отображается результат поиска указанного компьютера.'
ms.assetid: 0304b955-afde-4de4-824a-9ec9c9530360
title: Метод Shell. Финдкомпутер (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindComputer
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3824eeb98bfac11e007d1bf7dd9f89153a7b73ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985981"
---
# <a name="shellfindcomputer-method"></a><span data-ttu-id="76b5b-104">Shell. Финдкомпутер, метод</span><span class="sxs-lookup"><span data-stu-id="76b5b-104">Shell.FindComputer method</span></span>

<span data-ttu-id="76b5b-105">Отображает диалоговое окно **Результаты поиска: компьютеры** .</span><span class="sxs-lookup"><span data-stu-id="76b5b-105">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="76b5b-106">В диалоговом окне отображается результат поиска указанного компьютера.</span><span class="sxs-lookup"><span data-stu-id="76b5b-106">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="76b5b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76b5b-107">Syntax</span></span>


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="76b5b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="76b5b-108">Parameters</span></span>

<span data-ttu-id="76b5b-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="76b5b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="76b5b-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76b5b-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="76b5b-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="76b5b-111">JScript</span></span>

<span data-ttu-id="76b5b-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="76b5b-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="76b5b-113">VB</span><span class="sxs-lookup"><span data-stu-id="76b5b-113">VB</span></span>

<span data-ttu-id="76b5b-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="76b5b-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="76b5b-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="76b5b-115">Examples</span></span>

<span data-ttu-id="76b5b-116">В следующем примере показано использование **финдкомпутер** .</span><span class="sxs-lookup"><span data-stu-id="76b5b-116">The following example shows **FindComputer** in use.</span></span> <span data-ttu-id="76b5b-117">Результат этого кода аналогичен нажатию кнопки " **Пуск** ", нажатия кнопки " **Поиск**", " **Принтеры", "компьютеры" или "люди** ", а затем выбора **компьютера в сети**.</span><span class="sxs-lookup"><span data-stu-id="76b5b-117">The result of this code is the same as pressing the **Start** button, clicking **Search**, clicking the **Printers, computers, or people** option, then clicking **A computer on the network**.</span></span> <span data-ttu-id="76b5b-118">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="76b5b-118">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="76b5b-119">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="76b5b-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
    }
</script>
```



<span data-ttu-id="76b5b-120">Сценариев</span><span class="sxs-lookup"><span data-stu-id="76b5b-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="76b5b-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="76b5b-121">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="76b5b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="76b5b-122">Requirements</span></span>



| <span data-ttu-id="76b5b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="76b5b-123">Requirement</span></span> | <span data-ttu-id="76b5b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="76b5b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76b5b-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76b5b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="76b5b-126">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="76b5b-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="76b5b-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76b5b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="76b5b-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="76b5b-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="76b5b-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="76b5b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="76b5b-130"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="76b5b-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="76b5b-131">IDL</span><span class="sxs-lookup"><span data-stu-id="76b5b-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="76b5b-132"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="76b5b-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="76b5b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="76b5b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76b5b-134"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="76b5b-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




