---
<span data-ttu-id="0d0df-101">Описание: Ишеллдиспатч. Финдкомпутер method-"отображает диалоговое окно" результаты поиска: компьютеры ".</span><span class="sxs-lookup"><span data-stu-id="0d0df-101">description: IShellDispatch.FindComputer method - 'Displays the Search Results: Computers dialog box.</span></span> <span data-ttu-id="0d0df-102">В диалоговом окне отображается результат поиска указанного компьютера.</span><span class="sxs-lookup"><span data-stu-id="0d0df-102">The dialog box shows the result of the search for a specified computer.'</span></span>
<span data-ttu-id="0d0df-103">MS. AssetID: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257 Title: метод Ишеллдиспатч. Финдкомпутер (Шлдисп. h) MS. Topic: ссылка на MS. Date: 05/31/2018 topic_type:</span><span class="sxs-lookup"><span data-stu-id="0d0df-103">ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257 title: IShellDispatch.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type:</span></span> 
- <span data-ttu-id="0d0df-104">апиреф</span><span class="sxs-lookup"><span data-stu-id="0d0df-104">APIRef</span></span>
- <span data-ttu-id="0d0df-105">api_name Кбсинтакс:</span><span class="sxs-lookup"><span data-stu-id="0d0df-105">kbSyntax api_name:</span></span> 
- <span data-ttu-id="0d0df-106">Api_type Ишеллдиспатч. Финдкомпутер:</span><span class="sxs-lookup"><span data-stu-id="0d0df-106">IShellDispatch.FindComputer api_type:</span></span> 
- <span data-ttu-id="0d0df-107">Api_location COM:</span><span class="sxs-lookup"><span data-stu-id="0d0df-107">COM api_location:</span></span> 
- <span data-ttu-id="0d0df-108">Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="0d0df-108">Shell32.dll</span></span>
---

# <a name="ishelldispatchfindcomputer-method"></a><span data-ttu-id="0d0df-109">Ишеллдиспатч. Финдкомпутер, метод</span><span class="sxs-lookup"><span data-stu-id="0d0df-109">IShellDispatch.FindComputer method</span></span>

<span data-ttu-id="0d0df-110">Отображает диалоговое окно **Результаты поиска: компьютеры** .</span><span class="sxs-lookup"><span data-stu-id="0d0df-110">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="0d0df-111">В диалоговом окне отображается результат поиска указанного компьютера.</span><span class="sxs-lookup"><span data-stu-id="0d0df-111">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d0df-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d0df-112">Syntax</span></span>


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="0d0df-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d0df-113">Parameters</span></span>

<span data-ttu-id="0d0df-114">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0d0df-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0d0df-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d0df-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="0d0df-116">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="0d0df-116">JScript</span></span>

<span data-ttu-id="0d0df-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0d0df-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="0d0df-118">VB</span><span class="sxs-lookup"><span data-stu-id="0d0df-118">VB</span></span>

<span data-ttu-id="0d0df-119">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0d0df-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d0df-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="0d0df-120">Remarks</span></span>

<span data-ttu-id="0d0df-121">Этот метод реализован и доступен через метод [**Shell. финдкомпутер**](shell-findcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="0d0df-121">This method is implemented and accessed through the [**Shell.FindComputer**](shell-findcomputer.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="0d0df-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="0d0df-122">Examples</span></span>

<span data-ttu-id="0d0df-123">В следующих примерах показано использование **финдкомпутер** в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0d0df-123">The following examples show the use of **FindComputer** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="0d0df-124">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="0d0df-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
    }
</script>
```



<span data-ttu-id="0d0df-125">Сценариев</span><span class="sxs-lookup"><span data-stu-id="0d0df-125">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="0d0df-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="0d0df-126">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="0d0df-127">Требования</span><span class="sxs-lookup"><span data-stu-id="0d0df-127">Requirements</span></span>



| <span data-ttu-id="0d0df-128">Требование</span><span class="sxs-lookup"><span data-stu-id="0d0df-128">Requirement</span></span> | <span data-ttu-id="0d0df-129">Значение</span><span class="sxs-lookup"><span data-stu-id="0d0df-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d0df-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d0df-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0d0df-131">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0d0df-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0d0df-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d0df-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0d0df-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0d0df-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0d0df-134">Header</span><span class="sxs-lookup"><span data-stu-id="0d0df-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d0df-135"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d0df-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="0d0df-136">IDL</span><span class="sxs-lookup"><span data-stu-id="0d0df-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0d0df-137"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0d0df-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="0d0df-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0d0df-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d0df-139"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="0d0df-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




