---
description: Создает универсальный объект транзакции, который начинает транзакцию. Вызывая методы этого класса, можно составить работу нескольких COM-объектов в одной транзакции и явно зафиксировать или прервать транзакцию.
ms.assetid: 5f3f83e0-33fc-4c43-9327-59485c0d8bd3
title: Класс Трансактионконтекстекс (Комсвкс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContextEx
api_type:
- COM
ms.openlocfilehash: 8cf5c3aaa7ffe126124a909498a7c54cfb012c65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807780"
---
# <a name="transactioncontextex-class"></a><span data-ttu-id="ac9dd-104">Класс Трансактионконтекстекс</span><span class="sxs-lookup"><span data-stu-id="ac9dd-104">TransactionContextEx class</span></span>

<span data-ttu-id="ac9dd-105">Создает универсальный объект транзакции, который начинает транзакцию.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-105">Creates a generic transactional object that begins a transaction.</span></span> <span data-ttu-id="ac9dd-106">Вызывая методы этого класса, можно составить работу нескольких COM-объектов в одной транзакции и явно зафиксировать или прервать транзакцию.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-106">By calling the methods of this class, you can compose the work of multiple COM objects in a single transaction and explicitly commit or abort the transaction.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="ac9dd-107">Когда следует реализовывать</span><span class="sxs-lookup"><span data-stu-id="ac9dd-107">When to implement</span></span>

<span data-ttu-id="ac9dd-108">Этот класс реализуется с помощью COM+.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-108">This class is implemented by COM+.</span></span>



| <span data-ttu-id="ac9dd-109">Требование</span><span class="sxs-lookup"><span data-stu-id="ac9dd-109">Requirement</span></span> | <span data-ttu-id="ac9dd-110">Значение</span><span class="sxs-lookup"><span data-stu-id="ac9dd-110">Value</span></span> |
|------------|--------------------------------------------------------|
| <span data-ttu-id="ac9dd-111">CLSID</span><span class="sxs-lookup"><span data-stu-id="ac9dd-111">CLSID</span></span>      | <span data-ttu-id="ac9dd-112">\_ТРАНСАКТИОНКОНТЕКСТЕКС CLSID</span><span class="sxs-lookup"><span data-stu-id="ac9dd-112">CLSID\_TransactionContextEx</span></span>                            |
| <span data-ttu-id="ac9dd-113">ProgID:</span><span class="sxs-lookup"><span data-stu-id="ac9dd-113">ProgID</span></span>     | <span data-ttu-id="ac9dd-114">L "Ткскткс. Трансактионконтекстекс"</span><span class="sxs-lookup"><span data-stu-id="ac9dd-114">L"TxCTx.TransactionContextEx"</span></span>                          |
| <span data-ttu-id="ac9dd-115">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="ac9dd-115">Interfaces</span></span> | [<span data-ttu-id="ac9dd-116">**итрансактионконтекстекс**</span><span class="sxs-lookup"><span data-stu-id="ac9dd-116">**ITransactionContextEx**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex) |



 

## <a name="when-to-use"></a><span data-ttu-id="ac9dd-117">Назначение</span><span class="sxs-lookup"><span data-stu-id="ac9dd-117">When to use</span></span>

<span data-ttu-id="ac9dd-118">Клиент, не являющийся транзакционным, использует этот класс для начала транзакции.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-118">A non-transactional client uses this class to begin a transaction.</span></span> <span data-ttu-id="ac9dd-119">Используя методы этого класса, клиент может вызывать дополнительные COM-объекты, которые, если они настроены для участия в транзакции, выполняются в пределах границы транзакции объекта контекста транзакции.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-119">Using the methods of this class, the client can call additional COM objects that, if configured to participate in a transaction, run within the transaction boundary of the transaction context object.</span></span> <span data-ttu-id="ac9dd-120">В зависимости от бизнес-логики клиент может явно зафиксировать или прервать транзакцию.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-120">Based on its business logic, the client can explicitly commit or abort the transaction.</span></span>

<span data-ttu-id="ac9dd-121">Класс **трансактионконтекстекс** ограничивает повторное использование бизнес-логики, влияющей на транзакцию.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-121">The **TransactionContextEx** class limits reuse of the business logic driving the transaction.</span></span> <span data-ttu-id="ac9dd-122">По этой причине рекомендуется использовать объекты, созданные из класса **трансактионконтекстекс** , с осторожностью.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-122">For this reason, it is recommended that objects instantiated from the **TransactionContextEx** class be used sparingly.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac9dd-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac9dd-123">Remarks</span></span>

<span data-ttu-id="ac9dd-124">Чтобы создать этот объект, вызовите метод [**иобжектконтекст:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span><span class="sxs-lookup"><span data-stu-id="ac9dd-124">To create this object, call [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span></span>

<span data-ttu-id="ac9dd-125">Класс **трансактионконтекстекс** не предназначен для использования в Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ac9dd-125">The **TransactionContextEx** class was not designed to be used in Visual Basic.</span></span> <span data-ttu-id="ac9dd-126">Вместо этого используйте класс [**трансактионконтекст**](transactioncontext.md) .</span><span class="sxs-lookup"><span data-stu-id="ac9dd-126">Use the [**TransactionContext**](transactioncontext.md) class instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac9dd-127">Требования</span><span class="sxs-lookup"><span data-stu-id="ac9dd-127">Requirements</span></span>



| <span data-ttu-id="ac9dd-128">Требование</span><span class="sxs-lookup"><span data-stu-id="ac9dd-128">Requirement</span></span> | <span data-ttu-id="ac9dd-129">Значение</span><span class="sxs-lookup"><span data-stu-id="ac9dd-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ac9dd-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac9dd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ac9dd-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ac9dd-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ac9dd-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ac9dd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ac9dd-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ac9dd-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ac9dd-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ac9dd-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac9dd-135"><dt>Комсвкс. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac9dd-135"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac9dd-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac9dd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac9dd-137">Настройка транзакций</span><span class="sxs-lookup"><span data-stu-id="ac9dd-137">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="ac9dd-138">**итрансактионконтекстекс**</span><span class="sxs-lookup"><span data-stu-id="ac9dd-138">**ITransactionContextEx**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex)
</dt> <dt>

[<span data-ttu-id="ac9dd-139">**трансактионконтекст**</span><span class="sxs-lookup"><span data-stu-id="ac9dd-139">**TransactionContext**</span></span>](transactioncontext.md)
</dt> </dl>

 

 




