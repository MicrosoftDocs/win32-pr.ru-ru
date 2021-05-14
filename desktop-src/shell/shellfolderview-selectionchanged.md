---
description: Событие Шеллфолдервиев. SelectionChanged — происходит при изменении состояния выбора любого элемента или элементов в представлении.
title: Событие Шеллфолдервиев. SelectionChanged (Шлдисп. h)
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
ms.assetid: e91b72fd-fd26-4e38-8e80-41febec3ca03
ms.openlocfilehash: f029ffb217249909e966b592280abf38b2ba2edd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842575"
---
# <a name="shellfolderviewselectionchanged-event"></a><span data-ttu-id="9e8f5-103">Шеллфолдервиев. SelectionChanged, событие</span><span class="sxs-lookup"><span data-stu-id="9e8f5-103">ShellFolderView.SelectionChanged event</span></span>

<span data-ttu-id="9e8f5-104">Происходит при изменении состояния выбора любого элемента или элементов в представлении.</span><span class="sxs-lookup"><span data-stu-id="9e8f5-104">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e8f5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e8f5-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderView.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="9e8f5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e8f5-106">Parameters</span></span>

<span data-ttu-id="9e8f5-107">Этот обработчик событий не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9e8f5-107">This event handler has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e8f5-108">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="9e8f5-108">Requirements</span></span>



| <span data-ttu-id="9e8f5-109">Требование</span><span class="sxs-lookup"><span data-stu-id="9e8f5-109">Requirement</span></span> | <span data-ttu-id="9e8f5-110">Значение</span><span class="sxs-lookup"><span data-stu-id="9e8f5-110">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e8f5-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9e8f5-111">Minimum supported client</span></span><br/> | <span data-ttu-id="9e8f5-112">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9e8f5-112">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9e8f5-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9e8f5-113">Minimum supported server</span></span><br/> | <span data-ttu-id="9e8f5-114">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9e8f5-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9e8f5-115">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9e8f5-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e8f5-116"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e8f5-116"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="9e8f5-117">IDL</span><span class="sxs-lookup"><span data-stu-id="9e8f5-117">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9e8f5-118"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9e8f5-118"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="9e8f5-119">DLL</span><span class="sxs-lookup"><span data-stu-id="9e8f5-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e8f5-120"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="9e8f5-120"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




