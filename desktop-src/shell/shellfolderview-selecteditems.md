---
description: Возвращает объект Фолдеритемс, представляющий все выбранные элементы в представлении.
title: Шеллфолдервиев. SelectedItems, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectedItems
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1ee3bf2e-f9c9-47d9-a0f2-efedd69770c5
ms.openlocfilehash: c6ade3a6e25d5de6bfa1661207473dac72ace2bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997867"
---
# <a name="shellfolderviewselecteditems-method"></a><span data-ttu-id="c3d1d-103">Шеллфолдервиев. SelectedItems, метод</span><span class="sxs-lookup"><span data-stu-id="c3d1d-103">ShellFolderView.SelectedItems method</span></span>

<span data-ttu-id="c3d1d-104">Возвращает объект [**фолдеритемс**](folderitems.md) , представляющий все выбранные элементы в представлении.</span><span class="sxs-lookup"><span data-stu-id="c3d1d-104">Gets a [**FolderItems**](folderitems.md) object that represents all of the selected items in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3d1d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3d1d-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.SelectedItems()
```



## <a name="parameters"></a><span data-ttu-id="c3d1d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3d1d-106">Parameters</span></span>

<span data-ttu-id="c3d1d-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="c3d1d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3d1d-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3d1d-108">Return value</span></span>

<span data-ttu-id="c3d1d-109">Тип: **[ **фолдеритемс**](folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c3d1d-109">Type: **[**FolderItems**](folderitems.md)\*\***</span></span>

<span data-ttu-id="c3d1d-110">Ссылка на объект [**фолдеритемс**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="c3d1d-110">An object reference to the [**FolderItems**](folderitems.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3d1d-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="c3d1d-111">Remarks</span></span>

<span data-ttu-id="c3d1d-112">**SelectedItems** может быть вызван только в локальной системе.</span><span class="sxs-lookup"><span data-stu-id="c3d1d-112">**SelectedItems** can only be called on the local system.</span></span> <span data-ttu-id="c3d1d-113">Он не будет работать при запуске на веб-странице по протоколу HTTP или UNC.</span><span class="sxs-lookup"><span data-stu-id="c3d1d-113">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="c3d1d-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="c3d1d-114">Examples</span></span>

<span data-ttu-id="c3d1d-115">В следующем примере показано правильное использование этого метода в JScript Embedded в HTML.</span><span class="sxs-lookup"><span data-stu-id="c3d1d-115">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectedItemsJ()
    {
        var objFolderItems;
        
        objFolderItems = WebOC.Document.SelectedItems();
        if (objFolderItems != null)
        {
            alert("Got FolderItems object.");
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
<INPUT id=SelectedItems 
       type=button 
       value=SelectedItems 
       name=SelectedItems 
       onclick="fnShellFolderViewSelectedItemsJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="c3d1d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c3d1d-116">Requirements</span></span>



| <span data-ttu-id="c3d1d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c3d1d-117">Requirement</span></span> | <span data-ttu-id="c3d1d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c3d1d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3d1d-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3d1d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c3d1d-120">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c3d1d-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c3d1d-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3d1d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c3d1d-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c3d1d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c3d1d-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c3d1d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3d1d-124"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3d1d-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c3d1d-125">IDL</span><span class="sxs-lookup"><span data-stu-id="c3d1d-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c3d1d-126"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c3d1d-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c3d1d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c3d1d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3d1d-128"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="c3d1d-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




