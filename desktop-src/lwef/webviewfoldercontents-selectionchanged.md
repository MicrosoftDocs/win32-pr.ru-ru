---
title: Событие Вебвиевфолдерконтентс. SelectionChanged (Шлдисп. h)
description: Происходит при изменении состояния выбора любого элемента или элементов в представлении.
ms.assetid: 46dfceec-aa81-4950-81e5-526a6e621271
keywords:
- Устаревшие функции среды Windows для события SelectionChanged
topic_type:
- apiref
api_name:
- SelectionChanged
api_location:
- Shell32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8421e9d06ff9fd24256da8a23cdd100b5749968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535135"
---
# <a name="webviewfoldercontentsselectionchanged-event"></a><span data-ttu-id="316da-104">Вебвиевфолдерконтентс. SelectionChanged, событие</span><span class="sxs-lookup"><span data-stu-id="316da-104">WebViewFolderContents.SelectionChanged event</span></span>

<span data-ttu-id="316da-105">Происходит при изменении состояния выбора любого элемента или элементов в представлении.</span><span class="sxs-lookup"><span data-stu-id="316da-105">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="316da-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="316da-106">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
WebViewFolderContents.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="316da-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="316da-107">Parameters</span></span>

<span data-ttu-id="316da-108">Этот обработчик событий не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="316da-108">This event handler has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="316da-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="316da-109">Examples</span></span>

<span data-ttu-id="316da-110">В следующем примере показано правильное использование этого события для JScript Embedded в HTML.</span><span class="sxs-lookup"><span data-stu-id="316da-110">The following example shows the proper usage of this event for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectionChangedJ()
    {
        alert("SelectionChanged event was called");
    }
</script>

<script language="JavaScript" for="FileList" event="SelectionChanged">
    fnWebViewFolderContentsSelectionChangedJ();
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="316da-111">Требования</span><span class="sxs-lookup"><span data-stu-id="316da-111">Requirements</span></span>



| <span data-ttu-id="316da-112">Требование</span><span class="sxs-lookup"><span data-stu-id="316da-112">Requirement</span></span> | <span data-ttu-id="316da-113">Значение</span><span class="sxs-lookup"><span data-stu-id="316da-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="316da-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="316da-114">Minimum supported client</span></span><br/> | <span data-ttu-id="316da-115">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="316da-115">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="316da-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="316da-116">Minimum supported server</span></span><br/> | <span data-ttu-id="316da-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="316da-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="316da-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="316da-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="316da-119"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="316da-119"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="316da-120">IDL</span><span class="sxs-lookup"><span data-stu-id="316da-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="316da-121"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="316da-121"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="316da-122">DLL</span><span class="sxs-lookup"><span data-stu-id="316da-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="316da-123"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="316da-123"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 





