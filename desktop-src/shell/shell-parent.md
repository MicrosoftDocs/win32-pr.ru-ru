---
description: Возвращает объект, представляющий родительский объект текущего объекта.
ms.assetid: 76c2f72c-5ef6-4f2c-bdfc-62ced6dbc504
title: Свойство Shell. Parent (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Parent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a121e4f87be1163429156f22dfe7bd55f1345f43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985545"
---
# <a name="shellparent-property"></a><span data-ttu-id="a2ad2-103">Свойство Shell. Parent</span><span class="sxs-lookup"><span data-stu-id="a2ad2-103">Shell.Parent property</span></span>

<span data-ttu-id="a2ad2-104">Возвращает объект, представляющий родительский объект текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="a2ad2-104">Gets an object that represents the parent of the current object.</span></span>

<span data-ttu-id="a2ad2-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a2ad2-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2ad2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2ad2-106">Syntax</span></span>


```JScript
objParent = Shell.Parent
```


```VB

Property Parent As Object
```





## <a name="property-value"></a><span data-ttu-id="a2ad2-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a2ad2-107">Property value</span></span>

<span data-ttu-id="a2ad2-108">Переменная типа [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , которая получает родительский объект.</span><span class="sxs-lookup"><span data-stu-id="a2ad2-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the parent object.</span></span>

## <a name="examples"></a><span data-ttu-id="a2ad2-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="a2ad2-109">Examples</span></span>

<span data-ttu-id="a2ad2-110">В следующем примере показано правильное использование **родителя** для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a2ad2-110">The following example shows the proper use of **Parent** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a2ad2-111">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="a2ad2-111">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellParentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objParent;

        objParent = objShell.Parent;
        if (objParent != null)
        {
            alert("Got parent property");
        }
    }
</script>
```



<span data-ttu-id="a2ad2-112">Сценариев</span><span class="sxs-lookup"><span data-stu-id="a2ad2-112">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellParentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            if (not objShell is nothing) then
                dim objParent

                set objParent = objShell.Parent
                    if (not objParent is nothing) then
                        alert("Got parent property")
                    end if
                set objParent = nothing
            end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="a2ad2-113">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="a2ad2-113">Visual Basic:</span></span>


```VB
Private Sub fnShellParentVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        If (Not objShell Is Nothing) Then
            Dim objParent As Object
            
            Set objParent = objShell.Parent
                If (Not objParent Is Nothing) Then
                    Debug.Print "Got parent object"
                End If
            Set objParent = Nothing
        End If
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a2ad2-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a2ad2-114">Requirements</span></span>



| <span data-ttu-id="a2ad2-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a2ad2-115">Requirement</span></span> | <span data-ttu-id="a2ad2-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a2ad2-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2ad2-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2ad2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a2ad2-118">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a2ad2-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a2ad2-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2ad2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a2ad2-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a2ad2-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a2ad2-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a2ad2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2ad2-122"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2ad2-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a2ad2-123">IDL</span><span class="sxs-lookup"><span data-stu-id="a2ad2-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a2ad2-124"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a2ad2-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a2ad2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a2ad2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2ad2-126"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="a2ad2-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
