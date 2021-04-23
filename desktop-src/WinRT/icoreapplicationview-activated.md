---
description: Происходит при активации приложения для Магазина Windows.
ms.assetid: CA0DB2D4-3417-48F5-8455-D87D0F323A1E
title: 'Событие Икореаппликатионвиев:: Activated (Windows. ApplicationModel. Core. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612f7110aa149396b18815afe664ee404c70fc52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263085"
---
# <a name="icoreapplicationviewactivated-event"></a><span data-ttu-id="67a5a-103">Событие Икореаппликатионвиев:: Activated</span><span class="sxs-lookup"><span data-stu-id="67a5a-103">ICoreApplicationView::Activated event</span></span>

<span data-ttu-id="67a5a-104">Происходит при активации приложения для Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="67a5a-104">Occurs when a Windows Store app is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="67a5a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67a5a-105">Syntax</span></span>


```C++
void Activated(
  [in] ITypedEventHandler<ICoreApplicationView*, IActivatedEventArgs*> handler
);
```



## <a name="parameters"></a><span data-ttu-id="67a5a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="67a5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67a5a-107">*обработчик событий* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="67a5a-107">*handler* \[in\]</span></span>
<span data-ttu-id="67a5a-108"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="67a5a-108"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="67a5a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="67a5a-109">Return value</span></span>

<span data-ttu-id="67a5a-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="67a5a-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67a5a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="67a5a-111">Remarks</span></span>

<span data-ttu-id="67a5a-112">Не вызывайте метод [**Exit**](/previous-versions//hh438368(v=vs.85)) из *обработчика*.</span><span class="sxs-lookup"><span data-stu-id="67a5a-112">Do not call the [**Exit**](/previous-versions//hh438368(v=vs.85)) method from within *handler*.</span></span>

## <a name="requirements"></a><span data-ttu-id="67a5a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="67a5a-113">Requirements</span></span>



| <span data-ttu-id="67a5a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="67a5a-114">Requirement</span></span> | <span data-ttu-id="67a5a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="67a5a-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67a5a-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="67a5a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="67a5a-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="67a5a-117">Windows 8</span></span><br/>                                                                                         |
| <span data-ttu-id="67a5a-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="67a5a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="67a5a-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="67a5a-119">Windows Server 2012</span></span><br/>                                                                               |
| <span data-ttu-id="67a5a-120">Header</span><span class="sxs-lookup"><span data-stu-id="67a5a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="67a5a-121"><dt>Windows. ApplicationModel. Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="67a5a-121"><dt>Windows.ApplicationModel.Core.h</dt></span></span> </dl>   |
| <span data-ttu-id="67a5a-122">IDL</span><span class="sxs-lookup"><span data-stu-id="67a5a-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="67a5a-123"><dt>Windows. ApplicationModel. Core. idl</dt></span><span class="sxs-lookup"><span data-stu-id="67a5a-123"><dt>Windows.ApplicationModel.Core.idl</dt></span></span> </dl> |



 

 
