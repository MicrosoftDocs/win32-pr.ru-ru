---
title: Событие Вебвиевфолдерконтентс. SelectionChanged (Шлдисп. h)
description: Событие Вебвиевфолдерконтентс. SelectionChanged — происходит при изменении состояния выбора любого элемента или элементов в представлении.
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
ms.openlocfilehash: ea6176cb2a1703d48cd2ddec8069c65d7efc978f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102662"
---
# <a name="webviewfoldercontentsselectionchanged-event"></a><span data-ttu-id="6cd6b-104">Вебвиевфолдерконтентс. SelectionChanged, событие</span><span class="sxs-lookup"><span data-stu-id="6cd6b-104">WebViewFolderContents.SelectionChanged event</span></span>

<span data-ttu-id="6cd6b-105">Происходит при изменении состояния выбора любого элемента или элементов в представлении.</span><span class="sxs-lookup"><span data-stu-id="6cd6b-105">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cd6b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6cd6b-106">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
WebViewFolderContents.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="6cd6b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6cd6b-107">Parameters</span></span>

<span data-ttu-id="6cd6b-108">Этот обработчик событий не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="6cd6b-108">This event handler has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="6cd6b-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="6cd6b-109">Examples</span></span>

<span data-ttu-id="6cd6b-110">В следующем примере показано правильное использование этого события для JScript Embedded в HTML.</span><span class="sxs-lookup"><span data-stu-id="6cd6b-110">The following example shows the proper usage of this event for JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="6cd6b-111">Требования</span><span class="sxs-lookup"><span data-stu-id="6cd6b-111">Requirements</span></span>



| <span data-ttu-id="6cd6b-112">Требование</span><span class="sxs-lookup"><span data-stu-id="6cd6b-112">Requirement</span></span> | <span data-ttu-id="6cd6b-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6cd6b-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cd6b-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6cd6b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6cd6b-115">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6cd6b-115">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6cd6b-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6cd6b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6cd6b-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6cd6b-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6cd6b-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6cd6b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cd6b-119"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cd6b-119"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="6cd6b-120">IDL</span><span class="sxs-lookup"><span data-stu-id="6cd6b-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6cd6b-121"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6cd6b-121"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="6cd6b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6cd6b-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cd6b-123"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="6cd6b-123"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 





