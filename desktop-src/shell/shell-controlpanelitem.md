---
description: Запускает указанное приложение панели управления ( \* . cpl).
title: Метод Shell. ControlPanelItem (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ControlPanelItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 54979bbd-b36b-4b5b-a8a0-5f63e9526fa5
ms.openlocfilehash: 04d2493f5d0ec5b86d19689cb8e7c2a02a82e536
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841805"
---
# <a name="shellcontrolpanelitem-method"></a><span data-ttu-id="d70a3-103">Shell. ControlPanelItem, метод</span><span class="sxs-lookup"><span data-stu-id="d70a3-103">Shell.ControlPanelItem method</span></span>

<span data-ttu-id="d70a3-104">Запускает указанное приложение панели управления ( \* . cpl).</span><span class="sxs-lookup"><span data-stu-id="d70a3-104">Runs the specified Control Panel (\*.cpl) application.</span></span> <span data-ttu-id="d70a3-105">Если приложение уже открыто, будет активирован запущенный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="d70a3-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="d70a3-106">Начиная с Windows Vista, большинство приложений панели управления являются элементами оболочки и не могут быть открыты с помощью этой функции.</span><span class="sxs-lookup"><span data-stu-id="d70a3-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="d70a3-107">Чтобы открыть эти приложения панели управления, передайте каноническое имя в control.exe.</span><span class="sxs-lookup"><span data-stu-id="d70a3-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="d70a3-108">Пример:</span><span class="sxs-lookup"><span data-stu-id="d70a3-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="d70a3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d70a3-109">Syntax</span></span>


```JScript
Shell.ControlPanelItem(
  bstrDir
)
```


```VB

Shell.ControlPanelItem( _
  ByVal bstrDir As BSTR _
)
```





## <a name="parameters"></a><span data-ttu-id="d70a3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d70a3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d70a3-111">*бстрдир* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d70a3-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d70a3-112">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="d70a3-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="d70a3-113">Имя файла приложения панели управления.</span><span class="sxs-lookup"><span data-stu-id="d70a3-113">The Control Panel application's file name.</span></span> <span data-ttu-id="d70a3-114">Все приложения панели управления имеют расширение. cpl.</span><span class="sxs-lookup"><span data-stu-id="d70a3-114">All Control Panel applications have the .cpl extension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d70a3-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d70a3-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="d70a3-116">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="d70a3-116">JScript</span></span>

<span data-ttu-id="d70a3-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d70a3-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="d70a3-118">VB</span><span class="sxs-lookup"><span data-stu-id="d70a3-118">VB</span></span>

<span data-ttu-id="d70a3-119">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d70a3-119">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="d70a3-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="d70a3-120">Examples</span></span>

<span data-ttu-id="d70a3-121">В следующем примере **ControlPanelItem** используется для запуска элемента **Свойства дисплея** панели управления.</span><span class="sxs-lookup"><span data-stu-id="d70a3-121">The following example uses **ControlPanelItem** to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="d70a3-122">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d70a3-122">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d70a3-123">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="d70a3-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="d70a3-124">Сценариев</span><span class="sxs-lookup"><span data-stu-id="d70a3-124">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellControlPanelItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.ControlPanelItem("desk.cpl")
       
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="d70a3-125">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="d70a3-125">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="d70a3-126">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="d70a3-126">Requirements</span></span>



| <span data-ttu-id="d70a3-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d70a3-127">Requirement</span></span> | <span data-ttu-id="d70a3-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d70a3-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d70a3-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d70a3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d70a3-130">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d70a3-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d70a3-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d70a3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d70a3-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d70a3-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d70a3-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d70a3-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d70a3-134"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="d70a3-134"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d70a3-135">IDL</span><span class="sxs-lookup"><span data-stu-id="d70a3-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d70a3-136"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d70a3-136"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d70a3-137">DLL</span><span class="sxs-lookup"><span data-stu-id="d70a3-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d70a3-138"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="d70a3-138"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
