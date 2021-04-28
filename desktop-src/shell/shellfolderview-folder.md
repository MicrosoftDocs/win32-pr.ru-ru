---
description: Свойство Шеллфолдервиев. Folder — получает объект Folder, представляющий представление.
ms.assetid: 8f3e7827-f2a0-4ce9-b3e9-e6316ec58863
title: Свойство Шеллфолдервиев. Folder (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Folder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 370fddc1428c8f77edb77cdac2dc04123fc5211f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083422"
---
# <a name="shellfolderviewfolder-property"></a><span data-ttu-id="e1490-103">Шеллфолдервиев. Folder, свойство</span><span class="sxs-lookup"><span data-stu-id="e1490-103">ShellFolderView.Folder property</span></span>

<span data-ttu-id="e1490-104">Возвращает объект [**Folder**](folder.md) , представляющий представление.</span><span class="sxs-lookup"><span data-stu-id="e1490-104">Gets a [**Folder**](folder.md) object that represents the view.</span></span>

<span data-ttu-id="e1490-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e1490-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1490-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1490-106">Syntax</span></span>


```JScript
Folder = ShellFolderView.Folder
```



## <a name="property-value"></a><span data-ttu-id="e1490-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e1490-107">Property value</span></span>

<span data-ttu-id="e1490-108">Объект, получающий объект [**Folder**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="e1490-108">Object that receives the [**Folder**](folder.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1490-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="e1490-109">Remarks</span></span>

<span data-ttu-id="e1490-110">**Папка** может быть вызвана только в локальной системе.</span><span class="sxs-lookup"><span data-stu-id="e1490-110">**Folder** can only be called on the local system.</span></span> <span data-ttu-id="e1490-111">Он не будет работать при запуске на веб-странице по протоколу HTTP или UNC.</span><span class="sxs-lookup"><span data-stu-id="e1490-111">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="e1490-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="e1490-112">Examples</span></span>

<span data-ttu-id="e1490-113">В следующем примере показано правильное использование этого свойства для JScript Embedded в HTML.</span><span class="sxs-lookup"><span data-stu-id="e1490-113">The following example shows the proper usage of this property for JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFolderJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            alert("Got Folder object");
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
        height=400 VIEWASTEXT>
</object>
<br><br>
<INPUT id=Folder 
       type=button 
       value=Folder 
       name=Folder 
       onclick="fnShellFolderViewFolderJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="e1490-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e1490-114">Requirements</span></span>



| <span data-ttu-id="e1490-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e1490-115">Requirement</span></span> | <span data-ttu-id="e1490-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e1490-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1490-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e1490-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e1490-118">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e1490-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e1490-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e1490-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e1490-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e1490-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e1490-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e1490-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1490-122"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1490-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e1490-123">IDL</span><span class="sxs-lookup"><span data-stu-id="e1490-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e1490-124"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e1490-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e1490-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e1490-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1490-126"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="e1490-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




