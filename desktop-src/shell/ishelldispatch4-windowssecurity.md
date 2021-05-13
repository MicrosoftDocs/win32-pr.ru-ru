---
description: IShellDispatch4. Виндовссекурити — отображает диалоговое окно "безопасность Windows".
title: IShellDispatch4. Виндовссекурити, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.WindowsSecurity
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 665c4644-7749-446e-8212-3ecc9901a035
ms.openlocfilehash: 6eadb580c73e5e56592c94e997bdc22c2cf894b4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843025"
---
# <a name="ishelldispatch4windowssecurity-method"></a><span data-ttu-id="cb72a-103">IShellDispatch4. Виндовссекурити, метод</span><span class="sxs-lookup"><span data-stu-id="cb72a-103">IShellDispatch4.WindowsSecurity method</span></span>

<span data-ttu-id="cb72a-104">Отображает диалоговое окно **Безопасность Windows** .</span><span class="sxs-lookup"><span data-stu-id="cb72a-104">Displays the **Windows Security** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb72a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb72a-105">Syntax</span></span>


```JScript
IShellDispatch4.WindowsSecurity()
```


```VB

IShellDispatch4.WindowsSecurity()
```





## <a name="parameters"></a><span data-ttu-id="cb72a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb72a-106">Parameters</span></span>

<span data-ttu-id="cb72a-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="cb72a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cb72a-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb72a-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="cb72a-109">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="cb72a-109">JScript</span></span>

<span data-ttu-id="cb72a-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cb72a-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="cb72a-111">VB</span><span class="sxs-lookup"><span data-stu-id="cb72a-111">VB</span></span>

<span data-ttu-id="cb72a-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cb72a-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb72a-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="cb72a-113">Remarks</span></span>

<span data-ttu-id="cb72a-114">Этот метод отображает диалоговое окно, показанное после нажатия клавиш CTRL + ALT + DELETE или с помощью параметра безопасность в меню **Пуск** .</span><span class="sxs-lookup"><span data-stu-id="cb72a-114">This method displays the dialog box shown after pressing CTRL+ALT+DELETE or using the security option on the **Start** menu.</span></span>

> [!Note]  
> <span data-ttu-id="cb72a-115">Этот метод можно использовать только при соединении сеанса терминала с сервером терминалов Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cb72a-115">This method can be used only when connected by a terminal session to Microsoft Terminal Server.</span></span>

 

## <a name="examples"></a><span data-ttu-id="cb72a-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="cb72a-116">Examples</span></span>

<span data-ttu-id="cb72a-117">В следующих примерах показано использование **виндовссекурити** для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cb72a-117">The following examples show the use of **WindowsSecurity** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="cb72a-118">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="cb72a-118">JScript:</span></span>


```JScript
<script language="JScript">
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.WindowsSecurity();
    }
</script>
```



<span data-ttu-id="cb72a-119">Сценариев</span><span class="sxs-lookup"><span data-stu-id="cb72a-119">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4WindowsSecurityVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objshell.WindowsSecurity
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="cb72a-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="cb72a-120">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4WindowsSecurityVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        objshell.WindowsSecurity
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="cb72a-121">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="cb72a-121">Requirements</span></span>



| <span data-ttu-id="cb72a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="cb72a-122">Requirement</span></span> | <span data-ttu-id="cb72a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="cb72a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb72a-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb72a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cb72a-125">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cb72a-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="cb72a-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb72a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cb72a-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cb72a-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="cb72a-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cb72a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb72a-129"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb72a-129"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="cb72a-130">IDL</span><span class="sxs-lookup"><span data-stu-id="cb72a-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cb72a-131"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cb72a-131"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="cb72a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="cb72a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb72a-133"><dt>Shell32.dll (версия 6,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="cb72a-133"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




