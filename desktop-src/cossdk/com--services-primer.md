---
description: COM+ предоставляет простую модель программирования для использования автоматических служб.
ms.assetid: 2d616b56-4b6a-4c3b-bbd8-d5ca03c4911f
title: Учебник по службам COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9fd9d256b0213d3b1c58cae7d9670f87e4f4423
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342342"
---
# <a name="com-services-primer"></a><span data-ttu-id="41b57-103">Учебник по службам COM+</span><span class="sxs-lookup"><span data-stu-id="41b57-103">COM+ Services Primer</span></span>

<span data-ttu-id="41b57-104">COM+ предоставляет простую модель программирования для использования автоматических служб.</span><span class="sxs-lookup"><span data-stu-id="41b57-104">COM+ provides a simple programming model for using its automatic services.</span></span> <span data-ttu-id="41b57-105">Эти службы можно просто задать в качестве декларативных атрибутов для компонентов и их методов.</span><span class="sxs-lookup"><span data-stu-id="41b57-105">You can simply set these services as declarative attributes on components and their methods.</span></span> <span data-ttu-id="41b57-106">При установке этих атрибутов COM+ автоматически доставляет запрошенные службы объекту при необходимости.</span><span class="sxs-lookup"><span data-stu-id="41b57-106">When you set these attributes, COM+ automatically delivers the requested services to the object as required.</span></span>

<span data-ttu-id="41b57-107">В этом учебнике показаны службы COM+ в действии путем прохода по образцу кода компонента в трех определенных шагах.</span><span class="sxs-lookup"><span data-stu-id="41b57-107">This primer shows COM+ services in action by walking through sample component code in three defined steps.</span></span> <span data-ttu-id="41b57-108">Сложность данных строится по мере выполнения шагов.</span><span class="sxs-lookup"><span data-stu-id="41b57-108">The complexity of the information builds as the steps progress.</span></span> <span data-ttu-id="41b57-109">Код ориентирован на упрощенную модель программирования, используя обработку транзакций для демонстрации основных принципов COM+.</span><span class="sxs-lookup"><span data-stu-id="41b57-109">The code focuses on the simplified programming model, using transaction processing to demonstrate basic COM+ principles.</span></span>

<span data-ttu-id="41b57-110">Каждый из следующих шагов иллюстрирует фундаментальный аспект служб COM+:</span><span class="sxs-lookup"><span data-stu-id="41b57-110">Each of the following steps illustrates a fundamental aspect of COM+ services:</span></span>

-   [<span data-ttu-id="41b57-111">Шаг 1. Создание транзакционного компонента</span><span class="sxs-lookup"><span data-stu-id="41b57-111">Step 1: Creating a Transactional Component</span></span>](step-1--creating-a-transactional-component.md)
-   [<span data-ttu-id="41b57-112">Шаг 2. расширение транзакции для нескольких компонентов</span><span class="sxs-lookup"><span data-stu-id="41b57-112">Step 2: Extending a Transaction Across Multiple Components</span></span>](step-2--extending-a-transaction-across-multiple-components.md)
-   [<span data-ttu-id="41b57-113">Шаг 3. повторное использование компонентов</span><span class="sxs-lookup"><span data-stu-id="41b57-113">Step 3: Reusing Components</span></span>](step-3--reusing-components.md)

## <a name="related-topics"></a><span data-ttu-id="41b57-114">См. также</span><span class="sxs-lookup"><span data-stu-id="41b57-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41b57-115">Общие сведения о программировании COM+</span><span class="sxs-lookup"><span data-stu-id="41b57-115">COM+ Programming Overview</span></span>](com--programming-overview.md)
</dt> <dt>

[<span data-ttu-id="41b57-116">Общие сведения о приложении COM+</span><span class="sxs-lookup"><span data-stu-id="41b57-116">COM+ Application Overview</span></span>](com--application-overview.md)
</dt> <dt>

[<span data-ttu-id="41b57-117">Настройка приложений COM+</span><span class="sxs-lookup"><span data-stu-id="41b57-117">Configuring COM+ Applications</span></span>](configuring-com--applications.md)
</dt> <dt>

[<span data-ttu-id="41b57-118">Контексты COM+ и модели потоков</span><span class="sxs-lookup"><span data-stu-id="41b57-118">COM+ Contexts and Threading Models</span></span>](com--contexts-and-threading-models.md)
</dt> <dt>

[<span data-ttu-id="41b57-119">Создание приложений COM+</span><span class="sxs-lookup"><span data-stu-id="41b57-119">Creating COM+ Applications</span></span>](creating-com--applications.md)
</dt> <dt>

[<span data-ttu-id="41b57-120">Проектирование приложений COM+</span><span class="sxs-lookup"><span data-stu-id="41b57-120">Designing COM+ Applications</span></span>](designing-com--applications.md)
</dt> </dl>

 

 



