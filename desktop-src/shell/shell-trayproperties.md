---
description: Отображает диалоговое окно Свойства панели задач и меню "Пуск". Этот метод действует так же, как и щелчком правой кнопкой мыши панели задач и выбора свойств.
ms.assetid: 0d82d847-9e6f-461e-b938-fe8fd49a636f
title: Метод Shell. Трайпропертиес (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TrayProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da3fbfdb2b6aa2517b275041856920c6b2cd1bb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985961"
---
# <a name="shelltrayproperties-method"></a><span data-ttu-id="051ff-104">Shell. Трайпропертиес, метод</span><span class="sxs-lookup"><span data-stu-id="051ff-104">Shell.TrayProperties method</span></span>

<span data-ttu-id="051ff-105">Отображает диалоговое окно **Свойства панели задач и меню "Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="051ff-105">Displays the **Taskbar and Start Menu Properties** dialog box.</span></span> <span data-ttu-id="051ff-106">Этот метод действует так же, как и щелчком правой кнопкой мыши панели задач и выбора **свойств**.</span><span class="sxs-lookup"><span data-stu-id="051ff-106">This method has the same effect as right-clicking the taskbar and selecting **Properties**.</span></span>

## <a name="syntax"></a><span data-ttu-id="051ff-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="051ff-107">Syntax</span></span>


```JScript
iRetVal = Shell.TrayProperties()
```


```VB

Shell.TrayProperties() As Integer
```





## <a name="parameters"></a><span data-ttu-id="051ff-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="051ff-108">Parameters</span></span>

<span data-ttu-id="051ff-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="051ff-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="051ff-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="051ff-110">Examples</span></span>

<span data-ttu-id="051ff-111">В следующем примере показано использование **трайпропертиес** .</span><span class="sxs-lookup"><span data-stu-id="051ff-111">The following example shows **TrayProperties** in use.</span></span> <span data-ttu-id="051ff-112">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="051ff-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="051ff-113">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="051ff-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TrayProperties();
    }
</script>
```



<span data-ttu-id="051ff-114">Сценариев</span><span class="sxs-lookup"><span data-stu-id="051ff-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TrayProperties

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="051ff-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="051ff-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TrayProperties

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="051ff-116">Требования</span><span class="sxs-lookup"><span data-stu-id="051ff-116">Requirements</span></span>



| <span data-ttu-id="051ff-117">Требование</span><span class="sxs-lookup"><span data-stu-id="051ff-117">Requirement</span></span> | <span data-ttu-id="051ff-118">Значение</span><span class="sxs-lookup"><span data-stu-id="051ff-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="051ff-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="051ff-119">Minimum supported client</span></span><br/> | <span data-ttu-id="051ff-120">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="051ff-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="051ff-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="051ff-121">Minimum supported server</span></span><br/> | <span data-ttu-id="051ff-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="051ff-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="051ff-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="051ff-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="051ff-124"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="051ff-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="051ff-125">IDL</span><span class="sxs-lookup"><span data-stu-id="051ff-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="051ff-126"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="051ff-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="051ff-127">DLL</span><span class="sxs-lookup"><span data-stu-id="051ff-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="051ff-128"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="051ff-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




