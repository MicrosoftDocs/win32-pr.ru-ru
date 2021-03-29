---
description: Значения синхронизации могут быть автоматически определены или ограничены конфигурацией других свойств, например требованиями к транзакциям и JIT-активацией.
ms.assetid: 16771121-cb10-42b4-babc-59270188495a
title: Зависимости синхронизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c139d0d6e78288b25e42bd0a84b29432cebb44ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895737"
---
# <a name="synchronization-dependencies"></a><span data-ttu-id="3bea3-103">Зависимости синхронизации</span><span class="sxs-lookup"><span data-stu-id="3bea3-103">Synchronization Dependencies</span></span>

<span data-ttu-id="3bea3-104">Значения синхронизации могут быть автоматически определены или ограничены конфигурацией других свойств, например требованиями к транзакциям и JIT-активацией.</span><span class="sxs-lookup"><span data-stu-id="3bea3-104">Synchronization values can be automatically determined or constrained by the configuration of other properties, such as transactional requirements and just-in-time (JIT) activation.</span></span> <span data-ttu-id="3bea3-105">Например, COM+ обеспечивает принудительную синхронизацию как для транзакционных, так и для JIT-активированных компонентов.</span><span class="sxs-lookup"><span data-stu-id="3bea3-105">For example, COM+ enforces synchronization both for transactional and for JIT-activated components.</span></span>

<span data-ttu-id="3bea3-106">Эти зависимости существуют, поскольку компоненты, активируемые JIT-активацией или участвующие в транзакциях, должны иметь правильное поведение изоляции и параллелизма.</span><span class="sxs-lookup"><span data-stu-id="3bea3-106">These dependencies exist because components that are JIT-activated or participating in transactions must have proper isolation and concurrency behavior.</span></span> <span data-ttu-id="3bea3-107">Таким образом, COM+ требует, чтобы доступ к этим компонентам был сериализован путем принудительной синхронизации.</span><span class="sxs-lookup"><span data-stu-id="3bea3-107">Therefore, COM+ requires that access to these components be serialized by enforcing synchronization.</span></span> <span data-ttu-id="3bea3-108">(Дополнительные сведения об этих зависимостях см. [в разделе JIT-активация com+](com--just-in-time-activation.md).)</span><span class="sxs-lookup"><span data-stu-id="3bea3-108">(For details on these dependencies, see [COM+ Just-in-Time Activation](com--just-in-time-activation.md).)</span></span>

<span data-ttu-id="3bea3-109">В следующих таблицах показаны характеристики значений атрибута синхронизации COM+.</span><span class="sxs-lookup"><span data-stu-id="3bea3-109">The following tables show the characteristics of the COM+ synchronization attribute values.</span></span>

### <a name="transactional-requirement"></a><span data-ttu-id="3bea3-110">Транзакционное требование</span><span class="sxs-lookup"><span data-stu-id="3bea3-110">Transactional requirement</span></span>



| <span data-ttu-id="3bea3-111">Если для транзакций задано значение</span><span class="sxs-lookup"><span data-stu-id="3bea3-111">When transactions are set to</span></span> | <span data-ttu-id="3bea3-112">Для синхронизации можно задать значение</span><span class="sxs-lookup"><span data-stu-id="3bea3-112">Synchronization can be set to</span></span>                    |
|------------------------------|--------------------------------------------------|
| <span data-ttu-id="3bea3-113">Выключено</span><span class="sxs-lookup"><span data-stu-id="3bea3-113">Disabled</span></span><br/>          | <span data-ttu-id="3bea3-114">Что угодно, в зависимости от JIT-активации</span><span class="sxs-lookup"><span data-stu-id="3bea3-114">Anything, depending on JIT activation</span></span><br/> |
| <span data-ttu-id="3bea3-115">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3bea3-115">Not Supported</span></span><br/>     | <span data-ttu-id="3bea3-116">Что угодно, в зависимости от JIT-активации</span><span class="sxs-lookup"><span data-stu-id="3bea3-116">Anything, depending on JIT activation</span></span><br/> |
| <span data-ttu-id="3bea3-117">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="3bea3-117">Supported</span></span><br/>         | <span data-ttu-id="3bea3-118">Обязательно</span><span class="sxs-lookup"><span data-stu-id="3bea3-118">Required</span></span><br/>                              |
| <span data-ttu-id="3bea3-119">Обязательно</span><span class="sxs-lookup"><span data-stu-id="3bea3-119">Required</span></span><br/>          | <span data-ttu-id="3bea3-120">Обязательно</span><span class="sxs-lookup"><span data-stu-id="3bea3-120">Required</span></span><br/>                              |
| <span data-ttu-id="3bea3-121">RequiresNew</span><span class="sxs-lookup"><span data-stu-id="3bea3-121">Requires New</span></span><br/>      | <span data-ttu-id="3bea3-122">Обязательно или требуется новое</span><span class="sxs-lookup"><span data-stu-id="3bea3-122">Required or Requires New</span></span><br/>              |



 

### <a name="jit-activation"></a><span data-ttu-id="3bea3-123">JIT-активация</span><span class="sxs-lookup"><span data-stu-id="3bea3-123">JIT Activation</span></span>



| <span data-ttu-id="3bea3-124">Если для JIT-активации задано значение</span><span class="sxs-lookup"><span data-stu-id="3bea3-124">When JIT Activation is set to</span></span> | <span data-ttu-id="3bea3-125">Для синхронизации можно задать значение</span><span class="sxs-lookup"><span data-stu-id="3bea3-125">Synchronization can be set to</span></span>       |
|-------------------------------|-------------------------------------|
| <span data-ttu-id="3bea3-126">Активировано</span><span class="sxs-lookup"><span data-stu-id="3bea3-126">Enabled</span></span><br/>            | <span data-ttu-id="3bea3-127">Обязательно или требуется новое</span><span class="sxs-lookup"><span data-stu-id="3bea3-127">Required or Requires New</span></span><br/> |
| <span data-ttu-id="3bea3-128">Выключено</span><span class="sxs-lookup"><span data-stu-id="3bea3-128">Disabled</span></span><br/>           | <span data-ttu-id="3bea3-129">Кроме</span><span class="sxs-lookup"><span data-stu-id="3bea3-129">Anything</span></span><br/>                 |



 

<span data-ttu-id="3bea3-130">Дополнительные сведения о ведении транзакций, JIT-активации и атрибутов синхронизации см. в разделе [Настройка транзакций](configuring-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="3bea3-130">For more detail about how transaction, JIT Activation, and Synchronization attributes behave together, see [Configuring Transactions](configuring-transactions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3bea3-131">См. также</span><span class="sxs-lookup"><span data-stu-id="3bea3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bea3-132">Настройка атрибута синхронизации</span><span class="sxs-lookup"><span data-stu-id="3bea3-132">Setting the Synchronization Attribute</span></span>](setting-the-synchronization-attribute.md)
</dt> <dt>

[<span data-ttu-id="3bea3-133">Значения атрибутов синхронизации</span><span class="sxs-lookup"><span data-stu-id="3bea3-133">Synchronization Attribute Values</span></span>](synchronization-attribute-values.md)
</dt> </dl>

 

 




