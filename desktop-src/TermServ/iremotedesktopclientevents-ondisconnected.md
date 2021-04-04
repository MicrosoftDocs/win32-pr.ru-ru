---
title: Метод Иремотедесктопклиентевентс с отключением
description: Вызывается, когда клиентский элемент управления был отключен от удаленного сеанса.
ms.assetid: EA26B530-0AA8-49D6-8E3C-E53179FC5104
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода OnDisconnection
- Службы удаленных рабочих столов метода ondisconnectо, интерфейс Иремотедесктопклиентевентс
- Интерфейс Иремотедесктопклиентевентс службы удаленных рабочих столов, отключенный метод
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd59b03fe9cb23309d53773289291c8a791935a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802938"
---
# <a name="iremotedesktopclienteventsondisconnected-method"></a><span data-ttu-id="9c469-106">Иремотедесктопклиентевентс:: ondisconnectный метод</span><span class="sxs-lookup"><span data-stu-id="9c469-106">IRemoteDesktopClientEvents::OnDisconnected method</span></span>

<span data-ttu-id="9c469-107">Вызывается, когда клиентский элемент управления был отключен от удаленного сеанса.</span><span class="sxs-lookup"><span data-stu-id="9c469-107">Called when the client control has been disconnected from a remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c469-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c469-108">Syntax</span></span>


```C++
void OnDisconnected(
  [in] long disconnectReason,
  [in] long ExtendedDisconnectReason,
  [in] BSTR disconnectErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="9c469-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c469-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c469-110">*дисконнектреасон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c469-110">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c469-111">Причина события Disconnect.</span><span class="sxs-lookup"><span data-stu-id="9c469-111">The reason for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="9c469-112">*Екстендеддисконнектреасон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c469-112">*ExtendedDisconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c469-113">Расширенные сведения о событии Disconnect.</span><span class="sxs-lookup"><span data-stu-id="9c469-113">Extended information for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="9c469-114">*дисконнектеррормессаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c469-114">*disconnectErrorMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c469-115">Сообщение об ошибке для события Disconnect.</span><span class="sxs-lookup"><span data-stu-id="9c469-115">The error message for the disconnect event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c469-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c469-116">Return value</span></span>

<span data-ttu-id="9c469-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9c469-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c469-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9c469-118">Requirements</span></span>



| <span data-ttu-id="9c469-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9c469-119">Requirement</span></span> | <span data-ttu-id="9c469-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9c469-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c469-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c469-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9c469-122">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9c469-122">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="9c469-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c469-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9c469-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9c469-124">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="9c469-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="9c469-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="9c469-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c469-126"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="9c469-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9c469-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c469-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c469-128"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="9c469-129">IID</span><span class="sxs-lookup"><span data-stu-id="9c469-129">IID</span></span><br/>                      | <span data-ttu-id="9c469-130">ДИИД \_ иремотедесктопклиентевентс определяется как 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="9c469-130">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9c469-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c469-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c469-132">**иремотедесктопклиентевентс**</span><span class="sxs-lookup"><span data-stu-id="9c469-132">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





