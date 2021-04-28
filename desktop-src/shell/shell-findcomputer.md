---
<span data-ttu-id="7b8c5-101">Описание: Shell. Финдкомпутер method-"отображает диалоговое окно" результаты поиска: компьютеры ".</span><span class="sxs-lookup"><span data-stu-id="7b8c5-101">description: Shell.FindComputer method - 'Displays the Search Results: Computers dialog box.</span></span> <span data-ttu-id="7b8c5-102">В диалоговом окне отображается результат поиска указанного компьютера.</span><span class="sxs-lookup"><span data-stu-id="7b8c5-102">The dialog box shows the result of the search for a specified computer.'</span></span>
<span data-ttu-id="7b8c5-103">MS. AssetID: 0304b955-afde-4de4-824a-9ec9c9530360 Title: метод Shell. Финдкомпутер (Шлдисп. h) MS. Topic: ссылка на MS. Date: 05/31/2018 topic_type:</span><span class="sxs-lookup"><span data-stu-id="7b8c5-103">ms.assetid: 0304b955-afde-4de4-824a-9ec9c9530360 title: Shell.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type:</span></span> 
- <span data-ttu-id="7b8c5-104">апиреф</span><span class="sxs-lookup"><span data-stu-id="7b8c5-104">APIRef</span></span>
- <span data-ttu-id="7b8c5-105">api_name Кбсинтакс:</span><span class="sxs-lookup"><span data-stu-id="7b8c5-105">kbSyntax api_name:</span></span> 
- <span data-ttu-id="7b8c5-106">Api_type Shell. Финдкомпутер:</span><span class="sxs-lookup"><span data-stu-id="7b8c5-106">Shell.FindComputer api_type:</span></span> 
- <span data-ttu-id="7b8c5-107">Api_location COM:</span><span class="sxs-lookup"><span data-stu-id="7b8c5-107">COM api_location:</span></span> 
- <span data-ttu-id="7b8c5-108">Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="7b8c5-108">Shell32.dll</span></span>
---

# <a name="shellfindcomputer-method"></a><span data-ttu-id="7b8c5-109">Shell. Финдкомпутер, метод</span><span class="sxs-lookup"><span data-stu-id="7b8c5-109">Shell.FindComputer method</span></span>

<span data-ttu-id="7b8c5-110">Отображает диалоговое окно **Результаты поиска: компьютеры** .</span><span class="sxs-lookup"><span data-stu-id="7b8c5-110">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="7b8c5-111">В диалоговом окне отображается результат поиска указанного компьютера.</span><span class="sxs-lookup"><span data-stu-id="7b8c5-111">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b8c5-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b8c5-112">Syntax</span></span>


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="7b8c5-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b8c5-113">Parameters</span></span>

<span data-ttu-id="7b8c5-114">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7b8c5-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7b8c5-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b8c5-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="7b8c5-116">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="7b8c5-116">JScript</span></span>

<span data-ttu-id="7b8c5-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7b8c5-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="7b8c5-118">VB</span><span class="sxs-lookup"><span data-stu-id="7b8c5-118">VB</span></span>

<span data-ttu-id="7b8c5-119">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7b8c5-119">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="7b8c5-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="7b8c5-120">Examples</span></span>

<span data-ttu-id="7b8c5-121">В следующем примере показано использование **финдкомпутер** .</span><span class="sxs-lookup"><span data-stu-id="7b8c5-121">The following example shows **FindComputer** in use.</span></span> <span data-ttu-id="7b8c5-122">Результат этого кода аналогичен нажатию кнопки " **Пуск** ", нажатия кнопки " **Поиск**", " **Принтеры", "компьютеры" или "люди** ", а затем выбора **компьютера в сети**.</span><span class="sxs-lookup"><span data-stu-id="7b8c5-122">The result of this code is the same as pressing the **Start** button, clicking **Search**, clicking the **Printers, computers, or people** option, then clicking **A computer on the network**.</span></span> <span data-ttu-id="7b8c5-123">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7b8c5-123">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7b8c5-124">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="7b8c5-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
    }
</script>
```



<span data-ttu-id="7b8c5-125">Сценариев</span><span class="sxs-lookup"><span data-stu-id="7b8c5-125">VBScript:</span></span>


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



<span data-ttu-id="7b8c5-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="7b8c5-126">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="7b8c5-127">Требования</span><span class="sxs-lookup"><span data-stu-id="7b8c5-127">Requirements</span></span>



| <span data-ttu-id="7b8c5-128">Требование</span><span class="sxs-lookup"><span data-stu-id="7b8c5-128">Requirement</span></span> | <span data-ttu-id="7b8c5-129">Значение</span><span class="sxs-lookup"><span data-stu-id="7b8c5-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b8c5-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b8c5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7b8c5-131">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7b8c5-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7b8c5-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b8c5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7b8c5-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7b8c5-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7b8c5-134">Header</span><span class="sxs-lookup"><span data-stu-id="7b8c5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b8c5-135"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b8c5-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7b8c5-136">IDL</span><span class="sxs-lookup"><span data-stu-id="7b8c5-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7b8c5-137"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7b8c5-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7b8c5-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7b8c5-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b8c5-139"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="7b8c5-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




