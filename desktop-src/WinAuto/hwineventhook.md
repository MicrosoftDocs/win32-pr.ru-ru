---
title: ХВИНЕВЕНСУК (Виндеф. h)
description: Используется для объявления функции обработчика событий окна.
ms.assetid: fa193e8e-46a8-46d4-83e1-e6274276b218
keywords:
- хвиневенсук
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf526846916dfdd701f4f5ee98778dbbe9e66d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691848"
---
# <a name="hwineventhook"></a><span data-ttu-id="64d7a-104">хвиневенсук</span><span class="sxs-lookup"><span data-stu-id="64d7a-104">HWINEVENTHOOK</span></span>

<span data-ttu-id="64d7a-105">Используется для объявления функции обработчика событий окна.</span><span class="sxs-lookup"><span data-stu-id="64d7a-105">Used to declare a window event hook function.</span></span>


```C++
typedef HANDLE HWINEVENTHOOK;
```



## <a name="remarks"></a><span data-ttu-id="64d7a-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64d7a-106">Remarks</span></span>

<span data-ttu-id="64d7a-107">Этот тип данных используется с функцией обратного вызова [*виневентпрок*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) и функциями [**сетвиневенсук**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) и [**унхуквиневент**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) .</span><span class="sxs-lookup"><span data-stu-id="64d7a-107">This data type is used with the [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) callback function and the [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) and [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="64d7a-108">Требования</span><span class="sxs-lookup"><span data-stu-id="64d7a-108">Requirements</span></span>



| <span data-ttu-id="64d7a-109">Требование</span><span class="sxs-lookup"><span data-stu-id="64d7a-109">Requirement</span></span> | <span data-ttu-id="64d7a-110">Значение</span><span class="sxs-lookup"><span data-stu-id="64d7a-110">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64d7a-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="64d7a-111">Minimum supported client</span></span><br/> | <span data-ttu-id="64d7a-112">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="64d7a-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="64d7a-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="64d7a-113">Minimum supported server</span></span><br/> | <span data-ttu-id="64d7a-114">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="64d7a-114">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                          |
| <span data-ttu-id="64d7a-115">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="64d7a-115">Redistributable</span></span><br/>          | <span data-ttu-id="64d7a-116">Active Accessibility 1,3 RDK в Windows NT 4,0 с пакетом обновления SP6 и более поздней версии и Windows 95</span><span class="sxs-lookup"><span data-stu-id="64d7a-116">Active Accessibility 1.3 RDK on Windows NT 4.0 with SP6 and later and Windows 95</span></span><br/>                                   |
| <span data-ttu-id="64d7a-117">Header</span><span class="sxs-lookup"><span data-stu-id="64d7a-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="64d7a-118"><dt>Виндеф. h (WINVER >= 0x0500) (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="64d7a-118"><dt>Windef.h (WINVER >= 0x0500) (include Windows.h)</dt></span></span> </dl> |



 

 





