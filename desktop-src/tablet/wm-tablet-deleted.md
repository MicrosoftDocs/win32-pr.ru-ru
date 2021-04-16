---
description: Сообщение об удалении планшета WM отправляется \_ \_ при удалении планшетного устройства из Windows.
ms.assetid: af5be7f0-a213-49a1-800e-c922281522c8
title: Сообщение WM_TABLET_DELETED (Тпкшрд. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8ade03d199f8ee7a258b9db2aeea039fd725e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692236"
---
# <a name="wm_tablet_deleted-message"></a><span data-ttu-id="80269-103">\_ \_ Сообщение об удалении ПЛАНШЕТа WM</span><span class="sxs-lookup"><span data-stu-id="80269-103">WM\_TABLET\_DELETED message</span></span>

<span data-ttu-id="80269-104">Сообщение **об \_ \_ удалении** планшета WM отправляется при удалении планшетного устройства из Windows.</span><span class="sxs-lookup"><span data-stu-id="80269-104">The **WM\_TABLET\_DELETED** message is posted when a tablet device is removed from Windows.</span></span>


```C++
#define WM_TABLET_DEFBASE   0x02C0
#define WM_TABLET_DELETED   (WM_TABLET_DEFBASE + 9)     
```



## <a name="parameters"></a><span data-ttu-id="80269-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="80269-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80269-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="80269-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="80269-107">Индекс удаляемого устройства планшета.</span><span class="sxs-lookup"><span data-stu-id="80269-107">Index of tablet device being removed.</span></span>

</dd> <dt>

<span data-ttu-id="80269-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="80269-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="80269-109">Не используется.</span><span class="sxs-lookup"><span data-stu-id="80269-109">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80269-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80269-110">Remarks</span></span>

<span data-ttu-id="80269-111">Это сообщение отправляется всем окнам верхнего уровня в системе, включая отключенные или невидимые ненадлежащие окна, перекрывающиеся окна и всплывающие окна; но сообщение не отправляется в дочерние окна.</span><span class="sxs-lookup"><span data-stu-id="80269-111">This message is sent to all top-level windows in the system, including disabled or invisible unowned windows, overlapped windows, and pop-up windows; but the message is not sent to child windows.</span></span>

<span data-ttu-id="80269-112">Индексы, переданные в параметре *wParam* , связаны с индексом, используемым методом [**Итаблетманажер:: DataTable**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="80269-112">The indexes passed in *wParam* are related to the index used by the [**ITabletManager::GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="80269-113">Требования</span><span class="sxs-lookup"><span data-stu-id="80269-113">Requirements</span></span>



| <span data-ttu-id="80269-114">Требование</span><span class="sxs-lookup"><span data-stu-id="80269-114">Requirement</span></span> | <span data-ttu-id="80269-115">Значение</span><span class="sxs-lookup"><span data-stu-id="80269-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="80269-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80269-116">Minimum supported client</span></span><br/> | <span data-ttu-id="80269-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="80269-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="80269-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80269-118">Minimum supported server</span></span><br/> | <span data-ttu-id="80269-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="80269-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="80269-120">Header</span><span class="sxs-lookup"><span data-stu-id="80269-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="80269-121"><dt>Тпкшрд. h</dt></span><span class="sxs-lookup"><span data-stu-id="80269-121"><dt>Tpcshrd.h</dt></span></span> </dl> |



 

 
