---
title: Имстскаксевентс Онлогинкомплете, метод
description: Вызывается, когда клиентский элемент управления успешно выполнил вход на сервер узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов), как показано в диалоговом окне входа в систему Windows.
ms.assetid: acb345a6-3153-4b8f-ac51-fe0c19fa750a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онлогинкомплете
- Службы удаленных рабочих столов метода Онлогинкомплете, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онлогинкомплете
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLoginComplete
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74d6b63f74ed99c8af939bafdc8a55a41e33b404
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534442"
---
# <a name="imstscaxeventsonlogincomplete-method"></a><span data-ttu-id="6285a-106">Метод Имстскаксевентс:: Онлогинкомплете</span><span class="sxs-lookup"><span data-stu-id="6285a-106">IMsTscAxEvents::OnLoginComplete method</span></span>

<span data-ttu-id="6285a-107">Вызывается, когда клиентский элемент управления успешно выполнил вход на сервер узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов), как показано в диалоговом окне входа в систему Windows.</span><span class="sxs-lookup"><span data-stu-id="6285a-107">Called when the client control has successfully logged on to a Remote Desktop Session Host (RD Session Host) server, following the display of the Windows Logon dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="6285a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6285a-108">Syntax</span></span>


```C++
void OnLoginComplete();
```



## <a name="parameters"></a><span data-ttu-id="6285a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6285a-109">Parameters</span></span>

<span data-ttu-id="6285a-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="6285a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6285a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6285a-111">Return value</span></span>

<span data-ttu-id="6285a-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6285a-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6285a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6285a-113">Remarks</span></span>

<span data-ttu-id="6285a-114">Реализуйте этот метод в приемнике событий, чтобы получить уведомление о том, что элемент управления выполнил вход.</span><span class="sxs-lookup"><span data-stu-id="6285a-114">Implement this method in your event sink to receive notification that the control has completed logon.</span></span>

## <a name="examples"></a><span data-ttu-id="6285a-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="6285a-115">Examples</span></span>

<span data-ttu-id="6285a-116">В следующем примере показано, как справиться с этим событием с помощью Visual Basic кода скрипта.</span><span class="sxs-lookup"><span data-stu-id="6285a-116">The following example shows how to handle this event by using Visual Basic Scripting code.</span></span> <span data-ttu-id="6285a-117">В этом примере предполагается, что управляющий объект называется "Мсрдпклиент".</span><span class="sxs-lookup"><span data-stu-id="6285a-117">The assumption in this example is that your control object is named "MsRdpClient".</span></span>

<span data-ttu-id="6285a-118">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6285a-118">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>


```VB
Sub MsRdpClient.OnLoginComplete()
    Msgbox("Login has completed")
End sub
```



## <a name="requirements"></a><span data-ttu-id="6285a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="6285a-119">Requirements</span></span>



| <span data-ttu-id="6285a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="6285a-120">Requirement</span></span> | <span data-ttu-id="6285a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="6285a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6285a-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6285a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6285a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6285a-123">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6285a-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6285a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6285a-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6285a-125">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6285a-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="6285a-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="6285a-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6285a-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6285a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6285a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6285a-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6285a-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6285a-130">IID</span><span class="sxs-lookup"><span data-stu-id="6285a-130">IID</span></span><br/>                      | <span data-ttu-id="6285a-131">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="6285a-131">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="6285a-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6285a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6285a-133">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="6285a-133">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





