---
description: Мозаичное отображение всех окон на рабочем столе по горизонтали. Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбора пункта Показывать окна с накоплением.
ms.assetid: 85785510-6B75-450a-A9BB-6C3B4F6194E2
title: Ишеллдиспатч. Тилехоризонталли, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 06491f797de4a9fcb5c431d85cff71fbc78d605c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154938"
---
# <a name="ishelldispatchtilehorizontally-method"></a><span data-ttu-id="76562-104">Ишеллдиспатч. Тилехоризонталли, метод</span><span class="sxs-lookup"><span data-stu-id="76562-104">IShellDispatch.TileHorizontally method</span></span>

<span data-ttu-id="76562-105">Мозаичное отображение всех окон на рабочем столе по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="76562-105">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="76562-106">Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбора пункта **Показывать окна с накоплением**.</span><span class="sxs-lookup"><span data-stu-id="76562-106">This method has the same effect as right-clicking the taskbar and selecting **Show windows stacked**.</span></span>

## <a name="syntax"></a><span data-ttu-id="76562-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76562-107">Syntax</span></span>


```JScript
IShellDispatch.TileHorizontally()
```


```VB

IShellDispatch.TileHorizontally()
```





## <a name="parameters"></a><span data-ttu-id="76562-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="76562-108">Parameters</span></span>

<span data-ttu-id="76562-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="76562-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="76562-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76562-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="76562-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="76562-111">JScript</span></span>

<span data-ttu-id="76562-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="76562-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="76562-113">VB</span><span class="sxs-lookup"><span data-stu-id="76562-113">VB</span></span>

<span data-ttu-id="76562-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="76562-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="76562-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="76562-115">Remarks</span></span>

<span data-ttu-id="76562-116">Этот метод реализован и доступен через метод [**Shell. тилехоризонталли**](shell-tilehorizontally.md) .</span><span class="sxs-lookup"><span data-stu-id="76562-116">This method is implemented and accessed through the [**Shell.TileHorizontally**](shell-tilehorizontally.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="76562-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="76562-117">Examples</span></span>

<span data-ttu-id="76562-118">В следующем примере показано использование **тилехоризонталли** в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="76562-118">The following example shows the use of **TileHorizontally** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="76562-119">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="76562-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileHorizontally();
    }
</script>
```



<span data-ttu-id="76562-120">Сценариев</span><span class="sxs-lookup"><span data-stu-id="76562-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="76562-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="76562-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileHorizontally

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="76562-122">Требования</span><span class="sxs-lookup"><span data-stu-id="76562-122">Requirements</span></span>



| <span data-ttu-id="76562-123">Требование</span><span class="sxs-lookup"><span data-stu-id="76562-123">Requirement</span></span> | <span data-ttu-id="76562-124">Значение</span><span class="sxs-lookup"><span data-stu-id="76562-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76562-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76562-125">Minimum supported client</span></span><br/> | <span data-ttu-id="76562-126">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="76562-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="76562-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76562-127">Minimum supported server</span></span><br/> | <span data-ttu-id="76562-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="76562-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="76562-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="76562-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="76562-130"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="76562-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="76562-131">IDL</span><span class="sxs-lookup"><span data-stu-id="76562-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="76562-132"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="76562-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="76562-133">DLL</span><span class="sxs-lookup"><span data-stu-id="76562-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76562-134"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="76562-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




