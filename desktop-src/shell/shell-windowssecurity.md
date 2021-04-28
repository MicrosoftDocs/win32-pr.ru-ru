---
description: Shell. Виндовссекурити-метод — отображает диалоговое окно Безопасность Windows.
title: Метод Shell. Виндовссекурити (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.WindowsSecurity
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 94916E29-5960-4010-B2C6-0FAA1E4BF72D
ms.openlocfilehash: 7e04cc6d3a1a25f459da9f533fc562b1fc9d0b06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083602"
---
# <a name="shellwindowssecurity-method"></a><span data-ttu-id="64f7d-103">Shell. Виндовссекурити, метод</span><span class="sxs-lookup"><span data-stu-id="64f7d-103">Shell.WindowsSecurity method</span></span>

<span data-ttu-id="64f7d-104">Отображает диалоговое окно **Безопасность Windows** .</span><span class="sxs-lookup"><span data-stu-id="64f7d-104">Displays the **Windows Security** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="64f7d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64f7d-105">Syntax</span></span>


```JScript
Shell.WindowsSecurity()
```


```VB

Shell.WindowsSecurity()
```





## <a name="parameters"></a><span data-ttu-id="64f7d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="64f7d-106">Parameters</span></span>

<span data-ttu-id="64f7d-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="64f7d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="64f7d-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="64f7d-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="64f7d-109">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="64f7d-109">JScript</span></span>

<span data-ttu-id="64f7d-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="64f7d-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="64f7d-111">VB</span><span class="sxs-lookup"><span data-stu-id="64f7d-111">VB</span></span>

<span data-ttu-id="64f7d-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="64f7d-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="64f7d-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="64f7d-113">Remarks</span></span>

<span data-ttu-id="64f7d-114">Этот метод отображает диалоговое окно, показанное после нажатия клавиш CTRL + ALT + DELETE или с помощью параметра безопасность в меню **Пуск** .</span><span class="sxs-lookup"><span data-stu-id="64f7d-114">This method displays the dialog box shown after pressing CTRL+ALT+DELETE or using the security option on the **Start** menu.</span></span>

> [!Note]  
> <span data-ttu-id="64f7d-115">Этот метод можно использовать только при соединении сеанса терминала с сервером терминалов Microsoft.</span><span class="sxs-lookup"><span data-stu-id="64f7d-115">This method can be used only when connected by a terminal session to Microsoft Terminal Server.</span></span>

 

## <a name="examples"></a><span data-ttu-id="64f7d-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="64f7d-116">Examples</span></span>

<span data-ttu-id="64f7d-117">В следующих примерах показано использование **виндовссекурити** для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="64f7d-117">The following examples show the use of **WindowsSecurity** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="64f7d-118">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="64f7d-118">JScript:</span></span>


```JScript
<script language="JScript">
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.WindowsSecurity();
    }
</script>
```



<span data-ttu-id="64f7d-119">Сценариев</span><span class="sxs-lookup"><span data-stu-id="64f7d-119">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4WindowsSecurityVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objShell.WindowsSecurity
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="64f7d-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="64f7d-120">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4WindowsSecurityVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        objShell.WindowsSecurity
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="64f7d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="64f7d-121">Requirements</span></span>



| <span data-ttu-id="64f7d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="64f7d-122">Requirement</span></span> | <span data-ttu-id="64f7d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="64f7d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64f7d-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="64f7d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="64f7d-125">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="64f7d-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="64f7d-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="64f7d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="64f7d-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="64f7d-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="64f7d-128">Header</span><span class="sxs-lookup"><span data-stu-id="64f7d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="64f7d-129"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="64f7d-129"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="64f7d-130">IDL</span><span class="sxs-lookup"><span data-stu-id="64f7d-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="64f7d-131"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="64f7d-131"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="64f7d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="64f7d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64f7d-133"><dt>Shell32.dll (версия 6,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="64f7d-133"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




