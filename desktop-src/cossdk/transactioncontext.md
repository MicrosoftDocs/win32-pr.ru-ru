---
description: Создает универсальный объект транзакции, который начинает транзакцию.
ms.assetid: efaf1468-4973-472f-af91-85957a52b7df
title: Класс Трансактионконтекст (Комсвкс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContext
api_type:
- COM
ms.openlocfilehash: 595b5a3192b87420855eb43f1e1e33df37a45c23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262739"
---
# <a name="transactioncontext-class"></a><span data-ttu-id="c4cb9-103">Класс Трансактионконтекст</span><span class="sxs-lookup"><span data-stu-id="c4cb9-103">TransactionContext class</span></span>

<span data-ttu-id="c4cb9-104">Создает универсальный объект транзакции, который начинает транзакцию.</span><span class="sxs-lookup"><span data-stu-id="c4cb9-104">Creates a generic transactional object that begins a transaction.</span></span> <span data-ttu-id="c4cb9-105">Вызывая методы этого класса, можно составить работу нескольких COM-объектов в одной транзакции и явно зафиксировать или прервать транзакцию.</span><span class="sxs-lookup"><span data-stu-id="c4cb9-105">By calling the methods of this class, you can compose the work of multiple COM objects in a single transaction and explicitly commit or abort the transaction.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="c4cb9-106">Когда следует реализовывать</span><span class="sxs-lookup"><span data-stu-id="c4cb9-106">When to implement</span></span>

<span data-ttu-id="c4cb9-107">Этот класс реализуется с помощью COM+.</span><span class="sxs-lookup"><span data-stu-id="c4cb9-107">This class is implemented by COM+.</span></span>



| <span data-ttu-id="c4cb9-108">Требование</span><span class="sxs-lookup"><span data-stu-id="c4cb9-108">Requirement</span></span> | <span data-ttu-id="c4cb9-109">Значение</span><span class="sxs-lookup"><span data-stu-id="c4cb9-109">Value</span></span> |
|------------|----------------------------------------------------|
| <span data-ttu-id="c4cb9-110">CLSID</span><span class="sxs-lookup"><span data-stu-id="c4cb9-110">CLSID</span></span>      | <span data-ttu-id="c4cb9-111">\_ТРАНСАКТИОНКОНТЕКСТ CLSID</span><span class="sxs-lookup"><span data-stu-id="c4cb9-111">CLSID\_TransactionContext</span></span>                          |
| <span data-ttu-id="c4cb9-112">ProgID:</span><span class="sxs-lookup"><span data-stu-id="c4cb9-112">ProgID</span></span>     | <span data-ttu-id="c4cb9-113">L "Ткскткс. Трансактионконтекст"</span><span class="sxs-lookup"><span data-stu-id="c4cb9-113">L"TxCTx.TransactionContext"</span></span>                        |
| <span data-ttu-id="c4cb9-114">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="c4cb9-114">Interfaces</span></span> | [<span data-ttu-id="c4cb9-115">**итрансактионконтекст**</span><span class="sxs-lookup"><span data-stu-id="c4cb9-115">**ITransactionContext**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext) |



 

## <a name="when-to-use"></a><span data-ttu-id="c4cb9-116">Назначение</span><span class="sxs-lookup"><span data-stu-id="c4cb9-116">When to use</span></span>

<span data-ttu-id="c4cb9-117">Клиент, не являющийся транзакционным, использует этот класс для начала транзакции.</span><span class="sxs-lookup"><span data-stu-id="c4cb9-117">A non-transactional client uses this class to begin a transaction.</span></span> <span data-ttu-id="c4cb9-118">Используя методы этого класса, клиент может вызывать дополнительные COM-объекты, которые, если они настроены для участия в транзакции, выполняются в пределах границы транзакции объекта контекста транзакции.</span><span class="sxs-lookup"><span data-stu-id="c4cb9-118">Using the methods of this class, the client can call additional COM objects that, if configured to participate in a transaction, run within the transaction boundary of the transaction context object.</span></span> <span data-ttu-id="c4cb9-119">В зависимости от бизнес-логики клиент может явно зафиксировать или прервать транзакцию.</span><span class="sxs-lookup"><span data-stu-id="c4cb9-119">Based on its business logic, the client can explicitly commit or abort the transaction.</span></span>

<span data-ttu-id="c4cb9-120">Класс **трансактионконтекст** ограничивает повторное использование бизнес-логики, влияющей на транзакцию.</span><span class="sxs-lookup"><span data-stu-id="c4cb9-120">The **TransactionContext** class limits reuse of the business logic driving the transaction.</span></span> <span data-ttu-id="c4cb9-121">По этой причине рекомендуется использовать объекты, созданные из класса **трансактионконтекст** , с осторожностью.</span><span class="sxs-lookup"><span data-stu-id="c4cb9-121">For this reason, it is recommended that objects instantiated from the **TransactionContext** class be used sparingly.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4cb9-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c4cb9-122">Remarks</span></span>

<span data-ttu-id="c4cb9-123">Чтобы создать этот объект, вызовите метод [**иобжектконтекст:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span><span class="sxs-lookup"><span data-stu-id="c4cb9-123">To create this object, call [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).</span></span>

<span data-ttu-id="c4cb9-124">Чтобы использовать этот класс из Visual Basic Майкрософт, добавьте ссылку на библиотеку типов служб COM+.</span><span class="sxs-lookup"><span data-stu-id="c4cb9-124">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="c4cb9-125">Объект Трансактионконтекст можно объявить с помощью "Комсвкслиб. Трансактионконтекст" в качестве имени класса.</span><span class="sxs-lookup"><span data-stu-id="c4cb9-125">A TransactionContext object can be declared using "COMSVCSLib.TransactionContext" as the class name.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4cb9-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c4cb9-126">Requirements</span></span>



| <span data-ttu-id="c4cb9-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c4cb9-127">Requirement</span></span> | <span data-ttu-id="c4cb9-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c4cb9-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c4cb9-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4cb9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c4cb9-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c4cb9-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c4cb9-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4cb9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c4cb9-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c4cb9-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c4cb9-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c4cb9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4cb9-134"><dt>Комсвкс. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4cb9-134"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4cb9-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4cb9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4cb9-136">Настройка транзакций</span><span class="sxs-lookup"><span data-stu-id="c4cb9-136">Configuring Transactions</span></span>](configuring-transactions.md)
</dt> <dt>

[<span data-ttu-id="c4cb9-137">**итрансактионконтекст**</span><span class="sxs-lookup"><span data-stu-id="c4cb9-137">**ITransactionContext**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext)
</dt> <dt>

[<span data-ttu-id="c4cb9-138">**трансактионконтекстекс**</span><span class="sxs-lookup"><span data-stu-id="c4cb9-138">**TransactionContextEx**</span></span>](transactioncontextex.md)
</dt> </dl>

 

 




