---
description: Извлекает объект, представляющий родителя текущего объекта.
ms.assetid: 2FDEF8D3-3F5B-43ae-9812-83B4249D9CBB
title: Свойство Ишеллдиспатч. Parent (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Parent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 051e6f323b9663b692410d81d85e55a404e99d56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154939"
---
# <a name="ishelldispatchparent-property"></a><span data-ttu-id="93eee-103">Ишеллдиспатч. Parent, свойство</span><span class="sxs-lookup"><span data-stu-id="93eee-103">IShellDispatch.Parent property</span></span>

<span data-ttu-id="93eee-104">Извлекает объект, представляющий родителя текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="93eee-104">Retrieves an object that represents the parent of the current object.</span></span>

<span data-ttu-id="93eee-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="93eee-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="93eee-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93eee-106">Syntax</span></span>


```JScript
objParent = IShellDispatch.Parent
```


```VB

Property Parent As Object
```





## <a name="property-value"></a><span data-ttu-id="93eee-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="93eee-107">Property value</span></span>

<span data-ttu-id="93eee-108">Переменная типа [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , которая получает родительский объект.</span><span class="sxs-lookup"><span data-stu-id="93eee-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the parent object.</span></span>

## <a name="remarks"></a><span data-ttu-id="93eee-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="93eee-109">Remarks</span></span>

<span data-ttu-id="93eee-110">Это свойство реализовано и доступно через свойство [**Shell. Parent**](shell-parent.md) .</span><span class="sxs-lookup"><span data-stu-id="93eee-110">This property is implemented and accessed through the [**Shell.Parent**](shell-parent.md) property.</span></span>

## <a name="examples"></a><span data-ttu-id="93eee-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="93eee-111">Examples</span></span>

<span data-ttu-id="93eee-112">В следующих примерах показано использование **родителя** в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="93eee-112">The following examples show the use of **Parent** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="93eee-113">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="93eee-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellParentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objParent;

        objParent = objshell.Shell_Parent;
        if (objParent != null)
        {
            alert("Got parent property");
        }
    }
</script>
```



<span data-ttu-id="93eee-114">Сценариев</span><span class="sxs-lookup"><span data-stu-id="93eee-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellParentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            if (not objShell is nothing) then
                dim objParent

                set objParent = objshell.Parent
                    if (not objParent is nothing) then
                        alert("Got parent property")
                    end if
                set objParent = nothing
            end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="93eee-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="93eee-115">Visual Basic:</span></span>


```VB
Private Sub fnShellParentVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        If (Not objShell Is Nothing) Then
            Dim objParent As Object
            
            Set objParent = objshell.Parent
                If (Not objParent Is Nothing) Then
                    Debug.Print "Got parent object"
                End If
            Set objParent = Nothing
        End If
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="93eee-116">Требования</span><span class="sxs-lookup"><span data-stu-id="93eee-116">Requirements</span></span>



| <span data-ttu-id="93eee-117">Требование</span><span class="sxs-lookup"><span data-stu-id="93eee-117">Requirement</span></span> | <span data-ttu-id="93eee-118">Значение</span><span class="sxs-lookup"><span data-stu-id="93eee-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93eee-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93eee-119">Minimum supported client</span></span><br/> | <span data-ttu-id="93eee-120">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="93eee-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="93eee-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93eee-121">Minimum supported server</span></span><br/> | <span data-ttu-id="93eee-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="93eee-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="93eee-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="93eee-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="93eee-124"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="93eee-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="93eee-125">IDL</span><span class="sxs-lookup"><span data-stu-id="93eee-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="93eee-126"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="93eee-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="93eee-127">DLL</span><span class="sxs-lookup"><span data-stu-id="93eee-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93eee-128"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="93eee-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
