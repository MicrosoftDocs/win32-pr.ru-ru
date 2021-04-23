---
description: Запускает указанное приложение панели управления.
title: Ишеллдиспатч. ControlPanelItem, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.ControlPanelItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9A9B6B3F-FBBC-4e76-8018-8858B6392276
ms.openlocfilehash: 72164ff76cbcf15703bc91160e6211b38015f989
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543162"
---
# <a name="ishelldispatchcontrolpanelitem-method"></a><span data-ttu-id="4109e-103">Ишеллдиспатч. ControlPanelItem, метод</span><span class="sxs-lookup"><span data-stu-id="4109e-103">IShellDispatch.ControlPanelItem method</span></span>

<span data-ttu-id="4109e-104">Запускает указанное приложение панели управления.</span><span class="sxs-lookup"><span data-stu-id="4109e-104">Runs the specified Control Panel application.</span></span> <span data-ttu-id="4109e-105">Если приложение уже открыто, будет активирован запущенный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="4109e-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="4109e-106">Начиная с Windows Vista, большинство приложений панели управления являются элементами оболочки и не могут быть открыты с помощью этой функции.</span><span class="sxs-lookup"><span data-stu-id="4109e-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="4109e-107">Чтобы открыть эти приложения панели управления, передайте каноническое имя в control.exe.</span><span class="sxs-lookup"><span data-stu-id="4109e-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="4109e-108">Пример:</span><span class="sxs-lookup"><span data-stu-id="4109e-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="4109e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4109e-109">Syntax</span></span>


```JScript
IShellDispatch.ControlPanelItem(
  bstrDir
)
```


```VB

IShellDispatch.ControlPanelItem( _
  ByVal bstrDir As BSTR _
)
```





## <a name="parameters"></a><span data-ttu-id="4109e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4109e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4109e-111">*бстрдир* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4109e-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4109e-112">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="4109e-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="4109e-113">Имя файла приложения панели управления.</span><span class="sxs-lookup"><span data-stu-id="4109e-113">The Control Panel application's file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4109e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4109e-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="4109e-115">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="4109e-115">JScript</span></span>

<span data-ttu-id="4109e-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4109e-116">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="4109e-117">VB</span><span class="sxs-lookup"><span data-stu-id="4109e-117">VB</span></span>

<span data-ttu-id="4109e-118">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4109e-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4109e-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="4109e-119">Remarks</span></span>

<span data-ttu-id="4109e-120">Этот метод реализован и доступен через метод [**Shell. ControlPanelItem**](shell-controlpanelitem.md) .</span><span class="sxs-lookup"><span data-stu-id="4109e-120">This method is implemented and accessed through the [**Shell.ControlPanelItem**](shell-controlpanelitem.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="4109e-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="4109e-121">Examples</span></span>

<span data-ttu-id="4109e-122">В следующих примерах используется [**ControlPanelItem**](shell-controlpanelitem.md) для запуска элемента **Свойства дисплея** панели управления.</span><span class="sxs-lookup"><span data-stu-id="4109e-122">The following examples use [**ControlPanelItem**](shell-controlpanelitem.md) to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="4109e-123">Сведения об использовании представлены для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4109e-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="4109e-124">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="4109e-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Shell_ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="4109e-125">Сценариев</span><span class="sxs-lookup"><span data-stu-id="4109e-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellControlPanelItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Shell_ControlPanelItem("desk.cpl")
       
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="4109e-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="4109e-126">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Shell_ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="4109e-127">Требования</span><span class="sxs-lookup"><span data-stu-id="4109e-127">Requirements</span></span>



| <span data-ttu-id="4109e-128">Требование</span><span class="sxs-lookup"><span data-stu-id="4109e-128">Requirement</span></span> | <span data-ttu-id="4109e-129">Значение</span><span class="sxs-lookup"><span data-stu-id="4109e-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4109e-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4109e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4109e-131">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4109e-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4109e-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4109e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4109e-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4109e-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4109e-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4109e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4109e-135"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="4109e-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="4109e-136">IDL</span><span class="sxs-lookup"><span data-stu-id="4109e-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4109e-137"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4109e-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="4109e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4109e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4109e-139"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="4109e-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
