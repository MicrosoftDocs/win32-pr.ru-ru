---
title: Метод onconnected Имстскаксевентс
description: Вызывается, когда клиентский элемент управления находится в процессе установления соединения с сервером узла сеансов удаленный рабочий стол.
ms.assetid: 9c26d112-c070-4870-93d5-2fcc84a1331f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода onconnected
- Метод onconnected службы удаленных рабочих столов, интерфейс Имстскаксевентс
- Интерфейс Имстскаксевентс службы удаленных рабочих столов, метод onconnected
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d83a6a14f58a0704f0a3110532ad8cf8c0d7dc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802141"
---
# <a name="imstscaxeventsonconnected-method"></a><span data-ttu-id="e022e-106">Метод Имстскаксевентс:: onconnected</span><span class="sxs-lookup"><span data-stu-id="e022e-106">IMsTscAxEvents::OnConnected method</span></span>

<span data-ttu-id="e022e-107">Вызывается, когда клиентский элемент управления находится в процессе установления соединения с сервером узла сеансов удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="e022e-107">Called when the client control is in the process of establishing a connection with a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="e022e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e022e-108">Syntax</span></span>


```C++
void OnConnected();
```



## <a name="parameters"></a><span data-ttu-id="e022e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e022e-109">Parameters</span></span>

<span data-ttu-id="e022e-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="e022e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e022e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e022e-111">Return value</span></span>

<span data-ttu-id="e022e-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e022e-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e022e-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e022e-113">Remarks</span></span>

<span data-ttu-id="e022e-114">Реализуйте этот метод в приемнике событий, чтобы получить уведомление о том, что элемент управления установил подключение к серверу узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="e022e-114">Implement this method in your event sink to receive notification that the control has established a connection with an RD Session Host server.</span></span>

<span data-ttu-id="e022e-115">Дополнительные сведения о вызове этого метода см. в событии [**имстскаксевентс:: онлогинкомплете**](imstscaxevents-onlogincomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="e022e-115">Refer to the [**IMsTscAxEvents::OnLoginComplete**](imstscaxevents-onlogincomplete.md) event for more information on calling this method.</span></span>

<span data-ttu-id="e022e-116">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e022e-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e022e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e022e-117">Requirements</span></span>



| <span data-ttu-id="e022e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e022e-118">Requirement</span></span> | <span data-ttu-id="e022e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e022e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e022e-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e022e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e022e-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e022e-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e022e-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e022e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e022e-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e022e-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e022e-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e022e-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="e022e-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e022e-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e022e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e022e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e022e-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e022e-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e022e-128">IID</span><span class="sxs-lookup"><span data-stu-id="e022e-128">IID</span></span><br/>                      | <span data-ttu-id="e022e-129">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="e022e-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="e022e-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e022e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e022e-131">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="e022e-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





