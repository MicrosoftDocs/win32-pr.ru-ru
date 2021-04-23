---
description: Связывает реализацию Итрансактионпрокси с текущим контекстом.
ms.assetid: 64009632-b536-41fb-95ac-b23e2cbf18da
title: 'Метод Иконтексттрансактионинфо:: Регистертрансактионпрокси'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.RegisterTransactionProxy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7b559453b0d4ed75f92f7a421be4c3a47e07fdf7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342392"
---
# <a name="icontexttransactioninforegistertransactionproxy-method"></a><span data-ttu-id="251a1-103">Метод Иконтексттрансактионинфо:: Регистертрансактионпрокси</span><span class="sxs-lookup"><span data-stu-id="251a1-103">IContextTransactionInfo::RegisterTransactionProxy method</span></span>

<span data-ttu-id="251a1-104">Связывает реализацию [**итрансактионпрокси**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) с текущим контекстом.</span><span class="sxs-lookup"><span data-stu-id="251a1-104">Associates an [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation with the current context.</span></span>

## <a name="syntax"></a><span data-ttu-id="251a1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="251a1-105">Syntax</span></span>


```C++
HRESULT RegisterTransactionProxy(
  [in]  ITransactionProxy *pProxy,
  [out] GUID              *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="251a1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="251a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="251a1-107">*ппрокси* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="251a1-107">*pProxy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="251a1-108">Реализация [**итрансактионпрокси**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) , связываемая с текущим контекстом.</span><span class="sxs-lookup"><span data-stu-id="251a1-108">An [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation to associate with the current context.</span></span>

</dd> <dt>

<span data-ttu-id="251a1-109">*пгуид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="251a1-109">*pGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="251a1-110">Идентификатор GUID, определяющий прокси транзакции.</span><span class="sxs-lookup"><span data-stu-id="251a1-110">A GUID that identifies the transaction proxy.</span></span> <span data-ttu-id="251a1-111">COM+ использует этот идентификатор GUID при вызове [**итрансактионпрокси:: Commit**](/windows/desktop/api/ComSvcs/nf-comsvcs-itransactionproxy-commit) на прокси транзакции.</span><span class="sxs-lookup"><span data-stu-id="251a1-111">COM+ uses this GUID when calling [**ITransactionProxy::Commit**](/windows/desktop/api/ComSvcs/nf-comsvcs-itransactionproxy-commit) on the transaction proxy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="251a1-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="251a1-112">Return value</span></span>

<span data-ttu-id="251a1-113">Этот метод может возвращать стандартные возвращаемые значения E \_ INVALIDARG, e \_ OUTOFMEMORY и e с \_ непредвиденными значениями, а также следующие значения.</span><span class="sxs-lookup"><span data-stu-id="251a1-113">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, and E\_UNEXPECTED, as well as the following values.</span></span>



| <span data-ttu-id="251a1-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="251a1-114">Return code</span></span>                                                                                                     | <span data-ttu-id="251a1-115">Описание</span><span class="sxs-lookup"><span data-stu-id="251a1-115">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="251a1-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="251a1-116"><dt>**S\_OK**</dt></span></span> </dl>                            | <span data-ttu-id="251a1-117">Метод завершился успешно.</span><span class="sxs-lookup"><span data-stu-id="251a1-117">The method completed successfully.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="251a1-118"><dt>**КОНТЕКСТ \_ E \_ алреадинтрансактион**</dt></span><span class="sxs-lookup"><span data-stu-id="251a1-118"><dt>**CONTEXT\_E\_ALREADYINTRANSACTION**</dt></span></span> </dl> | <span data-ttu-id="251a1-119">У текущего контекста уже есть связанная реализация [**итрансактионпрокси**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) .</span><span class="sxs-lookup"><span data-stu-id="251a1-119">The current context already has an associated [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation.</span></span><br/> |
| <dl> <span data-ttu-id="251a1-120"><dt>**E \_ нотимпл**</dt></span><span class="sxs-lookup"><span data-stu-id="251a1-120"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                       | <span data-ttu-id="251a1-121">В текущем контексте размещается транзакция "присвоить собственную транзакцию" (BYOT) или некорневая транзакция.</span><span class="sxs-lookup"><span data-stu-id="251a1-121">The current context is hosting a Bring Your Own Transaction (BYOT) transaction or a non-root transaction.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="251a1-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="251a1-122">Remarks</span></span>

<span data-ttu-id="251a1-123">Метод **регистертрансактионпрокси** может быть вызван только в том случае, если текущий контекст является корневым контекстом транзакции.</span><span class="sxs-lookup"><span data-stu-id="251a1-123">The **RegisterTransactionProxy** method can only be called if the current context is a root transaction context.</span></span> <span data-ttu-id="251a1-124">Он не может быть вызван, если в контексте размещается транзакция BYOT или некорневая транзакция.</span><span class="sxs-lookup"><span data-stu-id="251a1-124">It cannot be called if the context is hosting a BYOT transaction or a non-root transaction.</span></span>

## <a name="requirements"></a><span data-ttu-id="251a1-125">Требования</span><span class="sxs-lookup"><span data-stu-id="251a1-125">Requirements</span></span>



| <span data-ttu-id="251a1-126">Требование</span><span class="sxs-lookup"><span data-stu-id="251a1-126">Requirement</span></span> | <span data-ttu-id="251a1-127">Значение</span><span class="sxs-lookup"><span data-stu-id="251a1-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="251a1-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="251a1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="251a1-129">Только для настольных приложений Windows XP с пакетом обновления 2 \[\]</span><span class="sxs-lookup"><span data-stu-id="251a1-129">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="251a1-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="251a1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="251a1-131">Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="251a1-131">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="251a1-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="251a1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="251a1-133">**иконтексттрансактионинфо**</span><span class="sxs-lookup"><span data-stu-id="251a1-133">**IContextTransactionInfo**</span></span>](icontexttransactioninfo.md)
</dt> </dl>

 

 




