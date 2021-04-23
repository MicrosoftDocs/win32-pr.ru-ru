---
description: Возвращает объект, представляющий родительский элемент для элемента.
ms.assetid: 612e76d8-d8bc-419c-b319-75b1f324840a
title: Свойство FolderItem. Parent (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Parent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f2da3504596c3b351318b33c929dad3b5a958165
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808021"
---
# <a name="folderitemparent-property"></a><span data-ttu-id="dea64-103">FolderItem. Parent, свойство</span><span class="sxs-lookup"><span data-stu-id="dea64-103">FolderItem.Parent property</span></span>

<span data-ttu-id="dea64-104">Возвращает объект, представляющий родительский элемент для элемента.</span><span class="sxs-lookup"><span data-stu-id="dea64-104">Gets an object that represents the parent of the item.</span></span>

<span data-ttu-id="dea64-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dea64-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dea64-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dea64-106">Syntax</span></span>


```JScript
objParent = FolderItem.Parent
```



## <a name="property-value"></a><span data-ttu-id="dea64-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dea64-107">Property value</span></span>

<span data-ttu-id="dea64-108">Переменная типа [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , которая получает родительский объект.</span><span class="sxs-lookup"><span data-stu-id="dea64-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the parent object.</span></span>

## <a name="examples"></a><span data-ttu-id="dea64-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="dea64-109">Examples</span></span>

<span data-ttu-id="dea64-110">В следующем примере показано правильное использование **родителя** для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="dea64-110">The following example shows the proper use of **Parent** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="dea64-111">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="dea64-111">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemParentJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;

        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;

            objFolderItem = objFolder2.Self;
            {
                var objParent;

                objParent = objFolderItem.Parent;
                if (objParent != null)
                {
                    alert("Got parent object");
                }
            }
        }
    }
</script>
```



<span data-ttu-id="dea64-112">Сценариев</span><span class="sxs-lookup"><span data-stu-id="dea64-112">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnFolderItemParentVB()
        dim objShell
        dim objFolder2
        dim ssfWINDOWS

        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem

                set objFolderItem = objFolder2.Self
                    if (not objFolderItem is nothing) then
                        dim objParent

                        set objParent = objFolderItem.Parent
                            if (not objParent is nothing) then
                                alert("Got parent object")
                            end if
                        set objParent = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder2 = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="dea64-113">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="dea64-113">Visual Basic:</span></span>


```VB
<script language="JScript">
    function fnFolderItemParentJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;

        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;

            objFolderItem = objFolder2.Self;
            {
                var objParent;

                objParent = objFolderItem.Parent;
                if (objParent != null)
                {
                    alert("Got parent object");
                }
            }
        }
    }
</script>
```



## <a name="requirements"></a><span data-ttu-id="dea64-114">Требования</span><span class="sxs-lookup"><span data-stu-id="dea64-114">Requirements</span></span>



| <span data-ttu-id="dea64-115">Требование</span><span class="sxs-lookup"><span data-stu-id="dea64-115">Requirement</span></span> | <span data-ttu-id="dea64-116">Значение</span><span class="sxs-lookup"><span data-stu-id="dea64-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea64-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dea64-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dea64-118">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dea64-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dea64-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dea64-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dea64-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dea64-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dea64-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="dea64-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="dea64-122"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="dea64-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="dea64-123">IDL</span><span class="sxs-lookup"><span data-stu-id="dea64-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dea64-124"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dea64-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="dea64-125">DLL</span><span class="sxs-lookup"><span data-stu-id="dea64-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dea64-126"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="dea64-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
