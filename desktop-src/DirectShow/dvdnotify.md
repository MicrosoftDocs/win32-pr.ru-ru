---
description: Событие Двднотифи уведомляет приложение о различных событиях и дисках DVD.
ms.assetid: 8e7d85fb-95c0-472d-ab17-a82da303b68f
title: Двднотифи (сегмент. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b31a2974bec428cb8ffe290edc9a384445e42070
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675756"
---
# <a name="dvdnotify"></a><span data-ttu-id="61a1b-103">двднотифи</span><span class="sxs-lookup"><span data-stu-id="61a1b-103">DVDNotify</span></span>

> [!Note]  
> <span data-ttu-id="61a1b-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="61a1b-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="61a1b-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="61a1b-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="61a1b-106">Это `DVDNotify` событие уведомляет приложение о различных событиях и дисках DVD.</span><span class="sxs-lookup"><span data-stu-id="61a1b-106">The `DVDNotify` event notifies an application of many different DVD events and disc instructions.</span></span>

``` syntax
DVDNotify(EventCode, Param1, Param2)
```

## <a name="parameters"></a><span data-ttu-id="61a1b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="61a1b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61a1b-108"><span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*</span><span class="sxs-lookup"><span data-stu-id="61a1b-108"><span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*</span></span>
</dt> <dd>

<span data-ttu-id="61a1b-109">Указывает код уведомления о событии DVD.</span><span class="sxs-lookup"><span data-stu-id="61a1b-109">Specifies the DVD event notification code.</span></span>

</dd> <dt>

<span data-ttu-id="61a1b-110"><span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="61a1b-110"><span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Param1*</span></span>
</dt> <dd>

<span data-ttu-id="61a1b-111">Может содержать дополнительные сведения, относящиеся к событию.</span><span class="sxs-lookup"><span data-stu-id="61a1b-111">Can contain additional information related to the event.</span></span>

</dd> <dt>

<span data-ttu-id="61a1b-112"><span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*</span><span class="sxs-lookup"><span data-stu-id="61a1b-112"><span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*</span></span>
</dt> <dd>

<span data-ttu-id="61a1b-113">Может содержать дополнительные сведения, относящиеся к событию.</span><span class="sxs-lookup"><span data-stu-id="61a1b-113">Can contain additional information related to the event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61a1b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="61a1b-114">Remarks</span></span>

<span data-ttu-id="61a1b-115">[Коды уведомлений о событиях DVD](dvd-notification-codes.md) предоставляют полное описание всех кодов уведомлений о событиях DVD и их параметров.</span><span class="sxs-lookup"><span data-stu-id="61a1b-115">[DVD Event Notification Codes](dvd-notification-codes.md) gives a full explanation of all DVD event notification codes and their parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="61a1b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="61a1b-116">Requirements</span></span>



| <span data-ttu-id="61a1b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="61a1b-117">Requirement</span></span> | <span data-ttu-id="61a1b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="61a1b-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="61a1b-119">Header</span><span class="sxs-lookup"><span data-stu-id="61a1b-119">Header</span></span><br/> | <dl> <span data-ttu-id="61a1b-120"><dt>Сегмент. h</dt></span><span class="sxs-lookup"><span data-stu-id="61a1b-120"><dt>Segment.h</dt></span></span> </dl> |



 

 




