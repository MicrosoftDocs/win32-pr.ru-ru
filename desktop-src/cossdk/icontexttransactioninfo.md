---
description: Предоставляет доступ к свойствам объекта контекста, которые связаны с транзакциями.
ms.assetid: 3b309153-be7d-444e-be23-777887f1ee95
title: Интерфейс Иконтексттрансактионинфо
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 499ab2371eda6dda6512b5fddb097d3adc2a6f05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496332"
---
# <a name="icontexttransactioninfo-interface"></a><span data-ttu-id="958da-103">Интерфейс Иконтексттрансактионинфо</span><span class="sxs-lookup"><span data-stu-id="958da-103">IContextTransactionInfo interface</span></span>

<span data-ttu-id="958da-104">Предоставляет доступ к свойствам объекта контекста, которые связаны с транзакциями.</span><span class="sxs-lookup"><span data-stu-id="958da-104">Provides access to context object properties that relate to transactions.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="958da-105">Когда следует реализовывать</span><span class="sxs-lookup"><span data-stu-id="958da-105">When to implement</span></span>

<span data-ttu-id="958da-106">Не следует реализовывать этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="958da-106">You should not implement this interface.</span></span> <span data-ttu-id="958da-107">Стандартная реализация предоставляет полную функциональность.</span><span class="sxs-lookup"><span data-stu-id="958da-107">The standard implementation provides complete functionality.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="958da-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="958da-108">When to use</span></span>

<span data-ttu-id="958da-109">Этот интерфейс используется для доступа к свойствам объекта контекста, которые связаны с транзакциями.</span><span class="sxs-lookup"><span data-stu-id="958da-109">Use this interface to access context object properties that relate to transactions.</span></span>

## <a name="members"></a><span data-ttu-id="958da-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="958da-110">Members</span></span>

<span data-ttu-id="958da-111">Интерфейс **иконтексттрансактионинфо** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="958da-111">The **IContextTransactionInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="958da-112">**Иконтексттрансактионинфо** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="958da-112">**IContextTransactionInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="958da-113">Методы</span><span class="sxs-lookup"><span data-stu-id="958da-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="958da-114">Методы</span><span class="sxs-lookup"><span data-stu-id="958da-114">Methods</span></span>

<span data-ttu-id="958da-115">Интерфейс **иконтексттрансактионинфо** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="958da-115">The **IContextTransactionInfo** interface has these methods.</span></span>



| <span data-ttu-id="958da-116">Метод</span><span class="sxs-lookup"><span data-stu-id="958da-116">Method</span></span>                                                                                         | <span data-ttu-id="958da-117">Описание</span><span class="sxs-lookup"><span data-stu-id="958da-117">Description</span></span>                                                                                                                 |
|:-----------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="958da-118">**фетчтрансактион**</span><span class="sxs-lookup"><span data-stu-id="958da-118">**FetchTransaction**</span></span>](icontexttransactioninfo-registertransactionproxy.md)                   | <span data-ttu-id="958da-119">Возвращает учетную запись-посредник транзакции или транзакции, связанную с текущим контекстом, если таковая имеется.</span><span class="sxs-lookup"><span data-stu-id="958da-119">Retrieves the transaction or transaction proxy that is associated with the current context, if any.</span></span><br/>              |
| [<span data-ttu-id="958da-120">**жеттксисолатионлевеландтимеаут**</span><span class="sxs-lookup"><span data-stu-id="958da-120">**GetTxIsolationLevelAndTimeout**</span></span>](icontexttransactioninfo-gettxisolationlevelandtimeout.md) | <span data-ttu-id="958da-121">Возвращает уровень изоляции и значение времени ожидания транзакции, размещенной в корневом контексте транзакции.</span><span class="sxs-lookup"><span data-stu-id="958da-121">Retrieves the isolation level and timeout value of a transaction that is hosted in the root transaction context.</span></span><br/> |
| [<span data-ttu-id="958da-122">**регистертрансактионпрокси**</span><span class="sxs-lookup"><span data-stu-id="958da-122">**RegisterTransactionProxy**</span></span>](icontexttransactioninfo-fetchtransaction.md)                   | <span data-ttu-id="958da-123">Связывает реализацию [**итрансактионпрокси**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) с текущим контекстом.</span><span class="sxs-lookup"><span data-stu-id="958da-123">Associates an [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation with the current context.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="958da-124">Требования</span><span class="sxs-lookup"><span data-stu-id="958da-124">Requirements</span></span>



| <span data-ttu-id="958da-125">Требование</span><span class="sxs-lookup"><span data-stu-id="958da-125">Requirement</span></span> | <span data-ttu-id="958da-126">Значение</span><span class="sxs-lookup"><span data-stu-id="958da-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="958da-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="958da-127">Minimum supported client</span></span><br/> | <span data-ttu-id="958da-128">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="958da-128">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="958da-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="958da-129">Minimum supported server</span></span><br/> | <span data-ttu-id="958da-130">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="958da-130">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



 

