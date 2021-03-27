---
description: Указывает, что состояние выбора одного или нескольких элементов в представлении изменилось.
title: Событие Шеллфолдервиевок. SelectionChanged (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectionChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 85c37f4e-229f-4383-8218-10f8c2b0b8a0
ms.openlocfilehash: 3f88ad698b990847a9b7f2fa1b74cc5b53ec7beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347922"
---
# <a name="shellfolderviewocselectionchanged-event"></a><span data-ttu-id="b6112-103">Шеллфолдервиевок. SelectionChanged, событие</span><span class="sxs-lookup"><span data-stu-id="b6112-103">ShellFolderViewOC.SelectionChanged event</span></span>

<span data-ttu-id="b6112-104">Указывает, что состояние выбора одного или нескольких элементов в представлении изменилось.</span><span class="sxs-lookup"><span data-stu-id="b6112-104">Indicates that the selection state of one or more items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6112-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6112-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="b6112-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6112-106">Parameters</span></span>

<span data-ttu-id="b6112-107">Этот обработчик событий не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b6112-107">This event handler has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6112-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="b6112-108">Remarks</span></span>

<span data-ttu-id="b6112-109">Укажите код обработки событий для этого события, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="b6112-109">Provide event handling code for this event as shown here.</span></span>


```
 
Private Sub object_SelectionChanged()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a><span data-ttu-id="b6112-110">Требования</span><span class="sxs-lookup"><span data-stu-id="b6112-110">Requirements</span></span>



| <span data-ttu-id="b6112-111">Требование</span><span class="sxs-lookup"><span data-stu-id="b6112-111">Requirement</span></span> | <span data-ttu-id="b6112-112">Значение</span><span class="sxs-lookup"><span data-stu-id="b6112-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6112-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6112-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b6112-114">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b6112-114">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6112-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6112-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b6112-116">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b6112-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b6112-117">Header</span><span class="sxs-lookup"><span data-stu-id="b6112-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6112-118"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6112-118"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="b6112-119">IDL</span><span class="sxs-lookup"><span data-stu-id="b6112-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b6112-120"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b6112-120"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="b6112-121">DLL</span><span class="sxs-lookup"><span data-stu-id="b6112-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6112-122"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="b6112-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6112-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6112-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6112-124">**шеллфолдервиевок**</span><span class="sxs-lookup"><span data-stu-id="b6112-124">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)
</dt> </dl>

 

 




