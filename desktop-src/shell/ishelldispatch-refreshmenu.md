---
description: Обновляет содержимое меню "Пуск". Используется только с системами, предшествующими Windows XP.
ms.assetid: D36FA5A0-AF03-4627-86E0-869BF1440958
title: Ишеллдиспатч. Рефрешмену, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 98728ef48ffb9ef4383cf9ba567606758b7a015c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984708"
---
# <a name="ishelldispatchrefreshmenu-method"></a><span data-ttu-id="a6722-104">Ишеллдиспатч. Рефрешмену, метод</span><span class="sxs-lookup"><span data-stu-id="a6722-104">IShellDispatch.RefreshMenu method</span></span>

<span data-ttu-id="a6722-105">Обновляет содержимое меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="a6722-105">Refreshes the contents of the **Start** menu.</span></span> <span data-ttu-id="a6722-106">Используется только с системами, предшествующими Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a6722-106">Used only with systems preceding Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6722-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6722-107">Syntax</span></span>


```JScript
IShellDispatch.RefreshMenu()
```


```VB

IShellDispatch.RefreshMenu()
```





## <a name="parameters"></a><span data-ttu-id="a6722-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6722-108">Parameters</span></span>

<span data-ttu-id="a6722-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a6722-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a6722-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a6722-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a6722-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="a6722-111">JScript</span></span>

<span data-ttu-id="a6722-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a6722-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="a6722-113">VB</span><span class="sxs-lookup"><span data-stu-id="a6722-113">VB</span></span>

<span data-ttu-id="a6722-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a6722-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6722-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="a6722-115">Remarks</span></span>

<span data-ttu-id="a6722-116">Этот метод реализован и доступен через метод [**Shell. трайпропертиес**](shell-trayproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="a6722-116">This method is implemented and accessed through the [**Shell.TrayProperties**](shell-trayproperties.md) method.</span></span>

<span data-ttu-id="a6722-117">Функциональные возможности, предоставляемые **рефрешмену** , автоматически обрабатываются в Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a6722-117">The functionality that **RefreshMenu** provides is handled automatically under Windows XP or later.</span></span> <span data-ttu-id="a6722-118">Не вызывайте этот метод в Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a6722-118">Do not call this method on Windows XP or later.</span></span>

## <a name="examples"></a><span data-ttu-id="a6722-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="a6722-119">Examples</span></span>

<span data-ttu-id="a6722-120">В следующих примерах показано использование **рефрешмену** в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a6722-120">The following examples show the use of **RefreshMenu** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a6722-121">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="a6722-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.RefreshMenu();
    }
</script>
```



<span data-ttu-id="a6722-122">Сценариев</span><span class="sxs-lookup"><span data-stu-id="a6722-122">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="a6722-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="a6722-123">Visual Basic:</span></span>


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a6722-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a6722-124">Requirements</span></span>



| <span data-ttu-id="a6722-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a6722-125">Requirement</span></span> | <span data-ttu-id="a6722-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a6722-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6722-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a6722-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a6722-128">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a6722-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a6722-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a6722-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a6722-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a6722-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a6722-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a6722-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6722-132"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6722-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a6722-133">IDL</span><span class="sxs-lookup"><span data-stu-id="a6722-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a6722-134"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a6722-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a6722-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a6722-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6722-136"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="a6722-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




