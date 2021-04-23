---
description: Атрибуты транзакции можно задать вручную с помощью средства администрирования "службы компонентов" или добавить программную поддержку для транзакций при написании компонента.
ms.assetid: b0d701c7-47ef-4034-873f-dd4428efb4c7
title: Установка атрибута Transaction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0690a50f79c77a18b089cec1865dfbb9e7f428
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142367"
---
# <a name="setting-the-transaction-attribute"></a><span data-ttu-id="3a673-103">Установка атрибута Transaction</span><span class="sxs-lookup"><span data-stu-id="3a673-103">Setting the Transaction Attribute</span></span>

<span data-ttu-id="3a673-104">Атрибуты транзакции можно задать вручную с помощью средства администрирования "службы компонентов" или добавить программную поддержку для транзакций при написании компонента.</span><span class="sxs-lookup"><span data-stu-id="3a673-104">You can set transaction attributes manually by using the Component Services administrative tool, or you can add programmatic support for transactions when you write your component.</span></span>

<span data-ttu-id="3a673-105">Дополнительные сведения о значениях атрибутов транзакций см. в разделе [Настройка транзакций](configuring-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="3a673-105">For more on transaction attribute values, see [Configuring Transactions](configuring-transactions.md).</span></span>

<span data-ttu-id="3a673-106">**Установка значения атрибута с помощью средства администрирования "службы компонентов"**</span><span class="sxs-lookup"><span data-stu-id="3a673-106">**To set the attribute value by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="3a673-107">В дереве консоли щелкните правой кнопкой мыши компонент, который необходимо настроить, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="3a673-107">In the console tree, right-click the component you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="3a673-108">В диалоговом окне Свойства компонента перейдите на вкладку **транзакции** .</span><span class="sxs-lookup"><span data-stu-id="3a673-108">In the component properties dialog box, click the **Transactions** tab.</span></span>

3.  <span data-ttu-id="3a673-109">В разделе **Поддержка транзакций** выберите параметр для нужного значения.</span><span class="sxs-lookup"><span data-stu-id="3a673-109">Under **Transaction support**, select the option for the value you want.</span></span> <span data-ttu-id="3a673-110">Значение по умолчанию для всех компонентов **не поддерживается**.</span><span class="sxs-lookup"><span data-stu-id="3a673-110">The default value for all components is **Not Supported**.</span></span>

4.  <span data-ttu-id="3a673-111">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="3a673-111">Click **OK**.</span></span>

<span data-ttu-id="3a673-112">Эту процедуру необходимо повторить для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="3a673-112">You must repeat this procedure for each component.</span></span>

## <a name="to-set-the-attribute-value-programmatically"></a><span data-ttu-id="3a673-113">Задание значения атрибута программным способом</span><span class="sxs-lookup"><span data-stu-id="3a673-113">To set the attribute value programmatically</span></span>

<span data-ttu-id="3a673-114">Программисты, использующие Microsoft Visual Basic, могут установить атрибут TRANSACTION с **мтстрансактионмоде**, свойством модуля класса для проектов DLL ActiveX.</span><span class="sxs-lookup"><span data-stu-id="3a673-114">Programmers using Microsoft Visual Basic can set the transaction attribute with **MTSTransactionMode**, a class module property for ActiveX DLL projects.</span></span> <span data-ttu-id="3a673-115">Visual Basic сопоставляет выбранные элементы с эквивалентным значением атрибута транзакции COM+ и публикует значение в библиотеке типов компонента.</span><span class="sxs-lookup"><span data-stu-id="3a673-115">Visual Basic maps your selection to the equivalent COM+ transaction attribute value and publishes the value in your component's type library.</span></span>

<span data-ttu-id="3a673-116">В следующей таблице каждое значение константы **мтстрансактионмоде** сопоставляется с эквивалентным ЗНАЧЕНИЕМ транзакции COM+.</span><span class="sxs-lookup"><span data-stu-id="3a673-116">The following table maps each **MTSTransactionMode** constant value to its equivalent COM+ transaction value.</span></span>



| <span data-ttu-id="3a673-117">Константа Мтстрансактионмоде</span><span class="sxs-lookup"><span data-stu-id="3a673-117">MTSTransactionMode constant</span></span>         | <span data-ttu-id="3a673-118">Значение транзакции COM+</span><span class="sxs-lookup"><span data-stu-id="3a673-118">COM+ transaction value</span></span>             |
|-------------------------------------|------------------------------------|
| <span data-ttu-id="3a673-119">Нотанмтсобжект (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3a673-119">NotAnMTSObject (default)</span></span><br/> | <span data-ttu-id="3a673-120">Выключено</span><span class="sxs-lookup"><span data-stu-id="3a673-120">Disabled</span></span><br/>                |
| <span data-ttu-id="3a673-121">Нетранзакционные</span><span class="sxs-lookup"><span data-stu-id="3a673-121">NoTransactions</span></span><br/>           | <span data-ttu-id="3a673-122">Не поддерживается (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3a673-122">Not Supported (default)</span></span><br/> |
| <span data-ttu-id="3a673-123">рекуирестрансактион</span><span class="sxs-lookup"><span data-stu-id="3a673-123">RequiresTransaction</span></span> <br/>     | <span data-ttu-id="3a673-124">Обязательно</span><span class="sxs-lookup"><span data-stu-id="3a673-124">Required</span></span><br/>                |
| <span data-ttu-id="3a673-125">усестрансактион</span><span class="sxs-lookup"><span data-stu-id="3a673-125">UsesTransaction</span></span> <br/>         | <span data-ttu-id="3a673-126">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="3a673-126">Supported</span></span><br/>               |
| <span data-ttu-id="3a673-127">рекуиресневтрансактион</span><span class="sxs-lookup"><span data-stu-id="3a673-127">RequiresNewTransaction</span></span> <br/>  | <span data-ttu-id="3a673-128">RequiresNew</span><span class="sxs-lookup"><span data-stu-id="3a673-128">Requires New</span></span><br/>            |



 

<span data-ttu-id="3a673-129">Доступ к свойству **мтстрансактионмоде** также можно получить программно с помощью API библиотеки администрирования com+.</span><span class="sxs-lookup"><span data-stu-id="3a673-129">The **MTSTransactionMode** property can also be accessed programmatically by using the COM+ Administration Library API.</span></span>

 

 




