---
description: Отображает диалоговое окно Свойства панели задач и меню "Пуск". Этот метод действует так же, как и щелчком правой кнопкой мыши панели задач и выбора свойств.
ms.assetid: 8E0AC08E-1132-4312-9B75-E7686B91AB02
title: Ишеллдиспатч. Трайпропертиес, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TrayProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5f5e22dd48b77035aab3754a4c8e3d2c414ec606
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991315"
---
# <a name="ishelldispatchtrayproperties-method"></a><span data-ttu-id="36c47-104">Ишеллдиспатч. Трайпропертиес, метод</span><span class="sxs-lookup"><span data-stu-id="36c47-104">IShellDispatch.TrayProperties method</span></span>

<span data-ttu-id="36c47-105">Отображает диалоговое окно **Свойства панели задач и меню "Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="36c47-105">Displays the **Taskbar and Start Menu Properties** dialog box.</span></span> <span data-ttu-id="36c47-106">Этот метод действует так же, как и щелчком правой кнопкой мыши панели задач и выбора **свойств**.</span><span class="sxs-lookup"><span data-stu-id="36c47-106">This method has the same effect as right-clicking the taskbar and selecting **Properties**.</span></span>

## <a name="syntax"></a><span data-ttu-id="36c47-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36c47-107">Syntax</span></span>


```JScript
IShellDispatch.TrayProperties()
```


```VB

IShellDispatch.TrayProperties()
```





## <a name="parameters"></a><span data-ttu-id="36c47-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="36c47-108">Parameters</span></span>

<span data-ttu-id="36c47-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="36c47-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="36c47-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36c47-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="36c47-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="36c47-111">JScript</span></span>

<span data-ttu-id="36c47-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="36c47-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="36c47-113">VB</span><span class="sxs-lookup"><span data-stu-id="36c47-113">VB</span></span>

<span data-ttu-id="36c47-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="36c47-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="36c47-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="36c47-115">Remarks</span></span>

<span data-ttu-id="36c47-116">Этот метод реализован и доступен через метод [**Shell. трайпропертиес**](shell-trayproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="36c47-116">This method is implemented and accessed through the [**Shell.TrayProperties**](shell-trayproperties.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="36c47-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="36c47-117">Examples</span></span>

<span data-ttu-id="36c47-118">В следующих примерах показано использование **трайпропертиес** в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="36c47-118">The following examples show the use of **TrayProperties** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="36c47-119">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="36c47-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TrayProperties();
    }
</script>
```



<span data-ttu-id="36c47-120">Сценариев</span><span class="sxs-lookup"><span data-stu-id="36c47-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TrayProperties

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="36c47-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="36c47-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TrayProperties

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="36c47-122">Требования</span><span class="sxs-lookup"><span data-stu-id="36c47-122">Requirements</span></span>



| <span data-ttu-id="36c47-123">Требование</span><span class="sxs-lookup"><span data-stu-id="36c47-123">Requirement</span></span> | <span data-ttu-id="36c47-124">Значение</span><span class="sxs-lookup"><span data-stu-id="36c47-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36c47-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36c47-125">Minimum supported client</span></span><br/> | <span data-ttu-id="36c47-126">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="36c47-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="36c47-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36c47-127">Minimum supported server</span></span><br/> | <span data-ttu-id="36c47-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="36c47-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="36c47-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="36c47-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="36c47-130"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="36c47-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="36c47-131">IDL</span><span class="sxs-lookup"><span data-stu-id="36c47-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="36c47-132"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="36c47-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="36c47-133">DLL</span><span class="sxs-lookup"><span data-stu-id="36c47-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36c47-134"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="36c47-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




