---
description: Изменение возвращаемых значений COM+
ms.assetid: a6997f02-8456-45b5-9f40-4b9094ee4626
title: Изменение возвращаемых значений COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa8270e41f1a1a96df0c17ccc1b98530fba4347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141827"
---
# <a name="how-com-modifies-return-values"></a><span data-ttu-id="4c787-103">Изменение возвращаемых значений COM+</span><span class="sxs-lookup"><span data-stu-id="4c787-103">How COM+ Modifies Return Values</span></span>

<span data-ttu-id="4c787-104">COM+ никогда не изменяет возвращаемое значение **HRESULT** , которое указывает на сбой, например "e \_ непредвиденно" или "e \_ Failed".</span><span class="sxs-lookup"><span data-stu-id="4c787-104">COM+ never changes the return value of an **HRESULT** that indicates failure, such as E\_UNEXPECTED or E\_FAIL.</span></span> <span data-ttu-id="4c787-105">Однако если объект, использующий функциональность COM+, возвращает значение **HRESULT** , указывающее на успешное выполнение (например \_ , S OK, s \_ false или No Error), COM+ иногда преобразует значение **HRESULT** в код ошибки COM+, прежде чем возвратить вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="4c787-105">However, when an object using COM+ functionality returns an **HRESULT** value indicating success (such as S\_OK, S\_FALSE, or NOERROR), COM+ sometimes converts the **HRESULT** into a COM+ error code before it returns to the caller.</span></span>

<span data-ttu-id="4c787-106">Например, если приложение возвращает значение S \_ ОК после вызова [**иобжектконтекст:: сеткомплете**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), если объект является корнем транзакции, которая не может быть зафиксирована, то значение **HRESULT** преобразуется в контекст \_ E, \_ Прерванный.</span><span class="sxs-lookup"><span data-stu-id="4c787-106">For example, when an application returns S\_OK after calling [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), if the object is the root of a transaction that fails to commit, the **HRESULT** is converted to CONTEXT\_E\_ABORTED.</span></span>

<span data-ttu-id="4c787-107">Когда COM+ преобразует значение **HRESULT** , он очищает все выходные параметры метода.</span><span class="sxs-lookup"><span data-stu-id="4c787-107">When COM+ converts an **HRESULT** value, it clears all of the method's output parameters.</span></span> <span data-ttu-id="4c787-108">Возвращаемые ссылки освобождаются, а значения возвращаемых указателей объектов устанавливаются в **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="4c787-108">Returned references are released, and the values of the returned object pointers are set to **NULL**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c787-109">См. также</span><span class="sxs-lookup"><span data-stu-id="4c787-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c787-110">Изоляция сбоев и политика FailFast</span><span class="sxs-lookup"><span data-stu-id="4c787-110">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[<span data-ttu-id="4c787-111">Поиск источника ошибки</span><span class="sxs-lookup"><span data-stu-id="4c787-111">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)
</dt> <dt>

[<span data-ttu-id="4c787-112">Анализ кодов ошибок</span><span class="sxs-lookup"><span data-stu-id="4c787-112">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="4c787-113">Стратегии обработки ошибок в COM+</span><span class="sxs-lookup"><span data-stu-id="4c787-113">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[<span data-ttu-id="4c787-114">Устранение неполадок</span><span class="sxs-lookup"><span data-stu-id="4c787-114">Troubleshooting</span></span>](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



