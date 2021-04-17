---
title: Интерфейс Иконнектионброкерклиент (Кбклиент. h)
description: Предоставляет методы, необходимые для использования клиента компонента подключение к удаленному рабочему столу Broker.
ms.assetid: AFFE0157-DEF5-480D-8CE0-D89E9EF70EAF
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Иконнектионброкерклиент
- Службы удаленных рабочих столов интерфейса Иконнектионброкерклиент, описание
topic_type:
- apiref
api_name:
- IConnectionBrokerClient
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a062059f7aa1f16e32514b3bacbfb31dc0a350f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492783"
---
# <a name="iconnectionbrokerclient-interface"></a><span data-ttu-id="f872d-105">Интерфейс Иконнектионброкерклиент</span><span class="sxs-lookup"><span data-stu-id="f872d-105">IConnectionBrokerClient interface</span></span>

<span data-ttu-id="f872d-106">Предоставляет методы, необходимые для использования клиента компонента подключение к удаленному рабочему столу Broker.</span><span class="sxs-lookup"><span data-stu-id="f872d-106">Provides the methods needed to use the Remote Desktop Connection Broker client.</span></span>

<span data-ttu-id="f872d-107">Этот интерфейс реализуется системой.</span><span class="sxs-lookup"><span data-stu-id="f872d-107">This interface is implemented by the system.</span></span> <span data-ttu-id="f872d-108">Чтобы получить экземпляр этого интерфейса, используйте функцию [**кбкреатеклиентинстанце**](cbcreateclientinstance.md) .</span><span class="sxs-lookup"><span data-stu-id="f872d-108">To obtain an instance of this interface, use the [**CBCreateClientInstance**](cbcreateclientinstance.md) function.</span></span>

## <a name="members"></a><span data-ttu-id="f872d-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="f872d-109">Members</span></span>

<span data-ttu-id="f872d-110">Интерфейс **иконнектионброкерклиент** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f872d-110">The **IConnectionBrokerClient** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f872d-111">**Иконнектионброкерклиент** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f872d-111">**IConnectionBrokerClient** also has these types of members:</span></span>

-   [<span data-ttu-id="f872d-112">Методы</span><span class="sxs-lookup"><span data-stu-id="f872d-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f872d-113">Методы</span><span class="sxs-lookup"><span data-stu-id="f872d-113">Methods</span></span>

<span data-ttu-id="f872d-114">Интерфейс **иконнектионброкерклиент** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f872d-114">The **IConnectionBrokerClient** interface has these methods.</span></span>



| <span data-ttu-id="f872d-115">Метод</span><span class="sxs-lookup"><span data-stu-id="f872d-115">Method</span></span>                                                         | <span data-ttu-id="f872d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="f872d-116">Description</span></span>                                                                                          |
|:---------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f872d-117">**жеттаржетинфо**</span><span class="sxs-lookup"><span data-stu-id="f872d-117">**GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md) | <span data-ttu-id="f872d-118">Запрашивает сведения о конечном компьютере, на котором должно быть перенаправлено подключение.</span><span class="sxs-lookup"><span data-stu-id="f872d-118">Requests information about the target computer where the connection should be redirected.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f872d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f872d-119">Requirements</span></span>



| <span data-ttu-id="f872d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f872d-120">Requirement</span></span> | <span data-ttu-id="f872d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f872d-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f872d-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f872d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f872d-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f872d-123">Windows 8</span></span><br/>                                                                       |
| <span data-ttu-id="f872d-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f872d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f872d-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f872d-125">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="f872d-126">Header</span><span class="sxs-lookup"><span data-stu-id="f872d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f872d-127"><dt>Кбклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="f872d-127"><dt>Cbclient.h</dt></span></span> </dl>      |
| <span data-ttu-id="f872d-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f872d-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="f872d-129"><dt>Кбклиент. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f872d-129"><dt>Cbclient.lib</dt></span></span> </dl>    |
| <span data-ttu-id="f872d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f872d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f872d-131"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f872d-131"><dt>Cbclient.dll</dt></span></span> </dl>    |
| <span data-ttu-id="f872d-132">IID</span><span class="sxs-lookup"><span data-stu-id="f872d-132">IID</span></span><br/>                      | <span data-ttu-id="f872d-133">IID \_ иконнектионброкерклиент определен как D6818DF2-8338-4EB7-AD77-DE210817987C</span><span class="sxs-lookup"><span data-stu-id="f872d-133">IID\_IConnectionBrokerClient is defined as D6818DF2-8338-4EB7-AD77-DE210817987C</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f872d-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f872d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f872d-135">**кбкреатеклиентинстанце**</span><span class="sxs-lookup"><span data-stu-id="f872d-135">**CBCreateClientInstance**</span></span>](cbcreateclientinstance.md)
</dt> </dl>

 

