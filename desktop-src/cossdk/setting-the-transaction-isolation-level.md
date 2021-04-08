---
description: Можно вручную задать уровень изоляции транзакций для компонентов с помощью средства администрирования "службы компонентов" или программно настроить уровень изоляции транзакции для компонента с помощью интерфейсов администрирования COM+.
ms.assetid: 3ef5b805-334d-4803-be67-00c9e35cdcc6
title: Установка уровня изоляции транзакций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b0447af2591c4f4b3e8e76c017157c02908367
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807781"
---
# <a name="setting-the-transaction-isolation-level"></a><span data-ttu-id="b905f-103">Установка уровня изоляции транзакций</span><span class="sxs-lookup"><span data-stu-id="b905f-103">Setting the Transaction Isolation Level</span></span>

<span data-ttu-id="b905f-104">Можно вручную задать уровень изоляции транзакций для компонентов с помощью средства администрирования "службы компонентов" или программно настроить уровень изоляции транзакции для компонента с помощью [интерфейсов администрирования com+](com--administration-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="b905f-104">You can manually set the transaction isolation level of components by using the Component Services administrative tool, or you can programmatically configure the transaction isolation level for a component by using the [COM+ administration interfaces](com--administration-interfaces.md).</span></span>

<span data-ttu-id="b905f-105">Дополнительные сведения об уровнях изоляции транзакций см. в разделе [Настройка уровней изоляции транзакций](configuring-transaction-isolation-levels.md).</span><span class="sxs-lookup"><span data-stu-id="b905f-105">For more on transaction isolation levels, see [Configuring Transaction Isolation Levels](configuring-transaction-isolation-levels.md).</span></span>

<span data-ttu-id="b905f-106">**Установка уровня изоляции транзакции с помощью средства администрирования "службы компонентов"**</span><span class="sxs-lookup"><span data-stu-id="b905f-106">**To set the transaction isolation level by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="b905f-107">В дереве консоли щелкните правой кнопкой мыши компонент, который необходимо настроить, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="b905f-107">In the console tree, right-click the component you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="b905f-108">В диалоговом окне Свойства компонента перейдите на вкладку **транзакции** .</span><span class="sxs-lookup"><span data-stu-id="b905f-108">In the component properties dialog box, click the **Transactions** tab.</span></span>

3.  <span data-ttu-id="b905f-109">В разделе **уровень изоляции транзакции** выберите нужное значение из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="b905f-109">Under **Transaction Isolation Level**, select the value you want from the drop-down box.</span></span> <span data-ttu-id="b905f-110">Значение по умолчанию для всех компонентов **сериализуется**.</span><span class="sxs-lookup"><span data-stu-id="b905f-110">The default value for all components is **Serialized**.</span></span>

    > [!Note]  
    > <span data-ttu-id="b905f-111">Если в разделе **Поддержка транзакций** выбрано значение **отключено** или **не поддерживается** , то нельзя задать уровень изоляции транзакции.</span><span class="sxs-lookup"><span data-stu-id="b905f-111">If either **Disabled** or **Not Supported** is selected under **Transaction support**, you cannot set the transaction isolation level.</span></span>

     

4.  <span data-ttu-id="b905f-112">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b905f-112">Click **OK**.</span></span>

<span data-ttu-id="b905f-113">Эту процедуру необходимо повторить для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="b905f-113">You must repeat this procedure for each component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b905f-114">См. также</span><span class="sxs-lookup"><span data-stu-id="b905f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b905f-115">Настройка уровней изоляции транзакций</span><span class="sxs-lookup"><span data-stu-id="b905f-115">Configuring Transaction Isolation Levels</span></span>](configuring-transaction-isolation-levels.md)
</dt> </dl>

 

 



