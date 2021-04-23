---
title: Интерфейс Иконнектионброкеррекуест (Кбклиент. h)
description: Предоставляет методы, необходимые для получения результатов асинхронного метода Иконнектионброкерклиент Жеттаржетинфо.
ms.assetid: 20F42FDC-7026-468E-9B8D-25DFFBE229C1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Иконнектионброкеррекуест
- Службы удаленных рабочих столов интерфейса Иконнектионброкеррекуест, описание
topic_type:
- apiref
api_name:
- IConnectionBrokerRequest
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb95427aee37053b6979cb1a12ce7b5d1942c2fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803898"
---
# <a name="iconnectionbrokerrequest-interface"></a><span data-ttu-id="59856-105">Интерфейс Иконнектионброкеррекуест</span><span class="sxs-lookup"><span data-stu-id="59856-105">IConnectionBrokerRequest interface</span></span>

<span data-ttu-id="59856-106">Предоставляет методы, необходимые для получения результатов асинхронного метода [**иконнектионброкерклиент:: жеттаржетинфо**](iconnectionbrokerclient-gettargetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="59856-106">Provides the methods needed to obtain the results of the asynchronous [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

<span data-ttu-id="59856-107">Этот интерфейс реализуется системой.</span><span class="sxs-lookup"><span data-stu-id="59856-107">This interface is implemented by the system.</span></span> <span data-ttu-id="59856-108">Экземпляр этого интерфейса предоставляется вызывающему объекту с помощью метода [**иконнектионброкерклиент:: жеттаржетинфо**](iconnectionbrokerclient-gettargetinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="59856-108">An instance of this interface is provided to the caller with the [**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="59856-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="59856-109">Members</span></span>

<span data-ttu-id="59856-110">Интерфейс **иконнектионброкеррекуест** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="59856-110">The **IConnectionBrokerRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="59856-111">**Иконнектионброкеррекуест** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="59856-111">**IConnectionBrokerRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="59856-112">Методы</span><span class="sxs-lookup"><span data-stu-id="59856-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="59856-113">Методы</span><span class="sxs-lookup"><span data-stu-id="59856-113">Methods</span></span>

<span data-ttu-id="59856-114">Интерфейс **иконнектионброкеррекуест** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="59856-114">The **IConnectionBrokerRequest** interface has these methods.</span></span>



| <span data-ttu-id="59856-115">Метод</span><span class="sxs-lookup"><span data-stu-id="59856-115">Method</span></span>                                                      | <span data-ttu-id="59856-116">Описание</span><span class="sxs-lookup"><span data-stu-id="59856-116">Description</span></span>                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="59856-117">**CheckStatus**</span><span class="sxs-lookup"><span data-stu-id="59856-117">**CheckStatus**</span></span>](iconnectionbrokerrequest-checkstatus.md) | <span data-ttu-id="59856-118">Вызывается для определения состояния асинхронного запроса.</span><span class="sxs-lookup"><span data-stu-id="59856-118">Called to determine the status of an asynchronous request.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="59856-119">Требования</span><span class="sxs-lookup"><span data-stu-id="59856-119">Requirements</span></span>



| <span data-ttu-id="59856-120">Требование</span><span class="sxs-lookup"><span data-stu-id="59856-120">Requirement</span></span> | <span data-ttu-id="59856-121">Значение</span><span class="sxs-lookup"><span data-stu-id="59856-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="59856-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59856-122">Minimum supported client</span></span><br/> | <span data-ttu-id="59856-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="59856-123">Windows 8</span></span><br/>                                                                        |
| <span data-ttu-id="59856-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59856-124">Minimum supported server</span></span><br/> | <span data-ttu-id="59856-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="59856-125">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="59856-126">Header</span><span class="sxs-lookup"><span data-stu-id="59856-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="59856-127"><dt>Кбклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="59856-127"><dt>Cbclient.h</dt></span></span> </dl>       |
| <span data-ttu-id="59856-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="59856-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="59856-129"><dt>Кбклиент. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59856-129"><dt>Cbclient.lib</dt></span></span> </dl>     |
| <span data-ttu-id="59856-130">DLL</span><span class="sxs-lookup"><span data-stu-id="59856-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59856-131"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59856-131"><dt>Cbclient.dll</dt></span></span> </dl>     |
| <span data-ttu-id="59856-132">IID</span><span class="sxs-lookup"><span data-stu-id="59856-132">IID</span></span><br/>                      | <span data-ttu-id="59856-133">IID \_ иконнектионброкеррекуест определен как 25114427-ED5D-46A6-AF53-C62D33A4108E</span><span class="sxs-lookup"><span data-stu-id="59856-133">IID\_IConnectionBrokerRequest is defined as 25114427-ED5D-46A6-AF53-C62D33A4108E</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59856-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59856-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59856-135">**Иконнектионброкерклиент:: Жеттаржетинфо**</span><span class="sxs-lookup"><span data-stu-id="59856-135">**IConnectionBrokerClient::GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

