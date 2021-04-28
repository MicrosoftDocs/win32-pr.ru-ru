---
description: Шеллфолдервиев. Фокуседитем Property — возвращает объект FolderItem, представляющий элемент, имеющий фокус ввода.
ms.assetid: ca88801d-c8fa-4c1c-9294-f52eada40ff6
title: Свойство Шеллфолдервиев. Фокуседитем (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.FocusedItem
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4f661f555f1492a3323fa3749a8dffd6f00f411d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104012"
---
# <a name="shellfolderviewfocuseditem-property"></a><span data-ttu-id="d7015-103">Шеллфолдервиев. Фокуседитем, свойство</span><span class="sxs-lookup"><span data-stu-id="d7015-103">ShellFolderView.FocusedItem property</span></span>

<span data-ttu-id="d7015-104">Возвращает объект [**FolderItem**](folderitem.md) , представляющий элемент, имеющий фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="d7015-104">Gets a [**FolderItem**](folderitem.md) object that represents the item that has the input focus.</span></span>

<span data-ttu-id="d7015-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d7015-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7015-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7015-106">Syntax</span></span>


```JScript
objFocusedItem = ShellFolderView.FocusedItem
```



## <a name="property-value"></a><span data-ttu-id="d7015-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d7015-107">Property value</span></span>

<span data-ttu-id="d7015-108">Переменная типа [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , получающая объект элемента с сортировкой.</span><span class="sxs-lookup"><span data-stu-id="d7015-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the focused item object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7015-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="d7015-109">Remarks</span></span>

<span data-ttu-id="d7015-110">**Фокуседитем** может быть вызван только в локальной системе.</span><span class="sxs-lookup"><span data-stu-id="d7015-110">**FocusedItem** can only be called on the local system.</span></span> <span data-ttu-id="d7015-111">Он не будет работать при запуске на веб-странице по протоколу HTTP или UNC.</span><span class="sxs-lookup"><span data-stu-id="d7015-111">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="d7015-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="d7015-112">Examples</span></span>

<span data-ttu-id="d7015-113">В следующем примере показано правильное использование этого метода в JScript Embedded в HTML.</span><span class="sxs-lookup"><span data-stu-id="d7015-113">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFocusedItemJ()
    {
        var objFolderItem;
        
        objFolderItem = WebOC.Document.FocusedItem;
        if (objFolderItem != null)
        {
            alert("Got FolderItem object.");
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC"
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400>
</object>
<br><br>
<INPUT id=FocusedItem 
       type=button 
       value=FocusedItem 
       name=FocusedItem 
       onclick="fnShellFolderViewFocusedItemJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="d7015-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d7015-114">Requirements</span></span>



| <span data-ttu-id="d7015-115">Требование</span><span class="sxs-lookup"><span data-stu-id="d7015-115">Requirement</span></span> | <span data-ttu-id="d7015-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d7015-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7015-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7015-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d7015-118">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d7015-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d7015-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7015-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d7015-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d7015-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d7015-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d7015-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7015-122"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7015-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d7015-123">IDL</span><span class="sxs-lookup"><span data-stu-id="d7015-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d7015-124"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d7015-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d7015-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d7015-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7015-126"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="d7015-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
