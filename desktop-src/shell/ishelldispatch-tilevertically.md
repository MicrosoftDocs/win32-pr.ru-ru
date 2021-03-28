---
description: Располагает все окна на рабочем столе по вертикали. Этот метод оказывает тот же результат, что и щелчок правой кнопкой мыши панели задач и выбора параметра Показывать окна рядом.
ms.assetid: 63CB7E20-48E6-4cfe-B0BA-0D28A7B151BD
title: Ишеллдиспатч. Тилевертикалли, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileVertically
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 42f98ae99814495029c67d41b05e86182c6b8b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984700"
---
# <a name="ishelldispatchtilevertically-method"></a><span data-ttu-id="f71f7-104">Ишеллдиспатч. Тилевертикалли, метод</span><span class="sxs-lookup"><span data-stu-id="f71f7-104">IShellDispatch.TileVertically method</span></span>

<span data-ttu-id="f71f7-105">Располагает все окна на рабочем столе по вертикали.</span><span class="sxs-lookup"><span data-stu-id="f71f7-105">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="f71f7-106">Этот метод оказывает тот же результат, что и щелчок правой кнопкой мыши панели задач и выбора параметра **Показывать окна рядом**.</span><span class="sxs-lookup"><span data-stu-id="f71f7-106">This method has the same effect as right-clicking the taskbar and selecting **Show windows side by side**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f71f7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f71f7-107">Syntax</span></span>


```JScript
IShellDispatch.TileVertically()
```


```VB

IShellDispatch.TileVertically()
```





## <a name="parameters"></a><span data-ttu-id="f71f7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f71f7-108">Parameters</span></span>

<span data-ttu-id="f71f7-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="f71f7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f71f7-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f71f7-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f71f7-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="f71f7-111">JScript</span></span>

<span data-ttu-id="f71f7-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f71f7-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="f71f7-113">VB</span><span class="sxs-lookup"><span data-stu-id="f71f7-113">VB</span></span>

<span data-ttu-id="f71f7-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f71f7-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f71f7-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="f71f7-115">Remarks</span></span>

<span data-ttu-id="f71f7-116">Этот метод реализован и доступен через метод [**Shell. тилевертикалли**](shell-tilevertically.md) .</span><span class="sxs-lookup"><span data-stu-id="f71f7-116">This method is implemented and accessed through the [**Shell.TileVertically**](shell-tilevertically.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="f71f7-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="f71f7-117">Examples</span></span>

<span data-ttu-id="f71f7-118">В следующих примерах показано использование **тилевертикалли** в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f71f7-118">The following examples show the use of **TileVertically** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f71f7-119">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="f71f7-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileVertically();
    }
</script>
```



<span data-ttu-id="f71f7-120">Сценариев</span><span class="sxs-lookup"><span data-stu-id="f71f7-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileVerticallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileVertically

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="f71f7-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="f71f7-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTileVerticallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileVertically

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f71f7-122">Требования</span><span class="sxs-lookup"><span data-stu-id="f71f7-122">Requirements</span></span>



| <span data-ttu-id="f71f7-123">Требование</span><span class="sxs-lookup"><span data-stu-id="f71f7-123">Requirement</span></span> | <span data-ttu-id="f71f7-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f71f7-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f71f7-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f71f7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f71f7-126">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f71f7-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f71f7-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f71f7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f71f7-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f71f7-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f71f7-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f71f7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f71f7-130"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="f71f7-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f71f7-131">IDL</span><span class="sxs-lookup"><span data-stu-id="f71f7-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f71f7-132"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f71f7-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f71f7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f71f7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f71f7-134"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="f71f7-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




