---
description: Можно вручную задать время ожидания транзакций с помощью средства администрирования "службы компонентов" или настроить время ожидания с помощью интерфейсов администрирования COM+.
ms.assetid: f7a35bdf-ea6d-40ea-b3c0-c2a3ae2276c4
title: Настройка Time-Out транзакций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b002448ca21e97e2e4996679d87a4b6a7680161f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496590"
---
# <a name="setting-the-transaction-time-out"></a><span data-ttu-id="f10d5-103">Настройка Time-Out транзакций</span><span class="sxs-lookup"><span data-stu-id="f10d5-103">Setting the Transaction Time-Out</span></span>

<span data-ttu-id="f10d5-104">Можно вручную задать время ожидания транзакций с помощью средства администрирования "службы компонентов" или настроить время ожидания с помощью [интерфейсов администрирования com+](com--administration-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="f10d5-104">You can manually set the time-out for transactions by using the Component Services administrative tool, or you can programmatically configure the time-out by using the [COM+ administration interfaces](com--administration-interfaces.md).</span></span> <span data-ttu-id="f10d5-105">Время ожидания можно настроить на локальном уровне компьютера, а также для отдельных компонентов.</span><span class="sxs-lookup"><span data-stu-id="f10d5-105">The time-out can be configured at the local computer level and also for individual components.</span></span>

<span data-ttu-id="f10d5-106">**Задание времени ожидания транзакции для локального компьютера с помощью средства администрирования "службы компонентов"**</span><span class="sxs-lookup"><span data-stu-id="f10d5-106">**To set the transaction time-out for the local computer by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="f10d5-107">В дереве консоли щелкните правой кнопкой мыши локальный компьютер, который необходимо настроить, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="f10d5-107">In the console tree, right-click the local computer you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="f10d5-108">В диалоговом окне Свойства компьютера перейдите на вкладку **Параметры** .</span><span class="sxs-lookup"><span data-stu-id="f10d5-108">In the computer properties dialog box, click the **Options** tab.</span></span>

3.  <span data-ttu-id="f10d5-109">В разделе время **ожидания транзакции** введите время ожидания транзакции в секундах.</span><span class="sxs-lookup"><span data-stu-id="f10d5-109">Under **Transaction Timeout**, enter the transaction time-out in seconds.</span></span> <span data-ttu-id="f10d5-110">По умолчанию время ожидания составляет 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="f10d5-110">The default time-out is 60 seconds.</span></span>

4.  <span data-ttu-id="f10d5-111">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f10d5-111">Click **OK**.</span></span>

<span data-ttu-id="f10d5-112">**Установка времени ожидания транзакции для компонента с помощью средства администрирования "службы компонентов"**</span><span class="sxs-lookup"><span data-stu-id="f10d5-112">**To set the transaction time-out for a component by using the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="f10d5-113">В дереве консоли щелкните правой кнопкой мыши компонент, который необходимо настроить, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="f10d5-113">In the console tree, right-click the component you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="f10d5-114">В диалоговом окне Свойства компонента перейдите на вкладку **транзакции** .</span><span class="sxs-lookup"><span data-stu-id="f10d5-114">In the component properties dialog box, click the **Transactions** tab.</span></span>

3.  <span data-ttu-id="f10d5-115">Установите флажок **переопределить глобальное значение времени ожидания транзакции**.</span><span class="sxs-lookup"><span data-stu-id="f10d5-115">Check the box labeled **Override global transaction timeout value**.</span></span>

    > [!Note]  
    > <span data-ttu-id="f10d5-116">Нельзя установить флажок, чтобы переопределить значение времени ожидания глобальной транзакции, если для **поддержки транзакций** задано **отключено**, **не поддерживается или не** **поддерживается**.</span><span class="sxs-lookup"><span data-stu-id="f10d5-116">You cannot check the box to override the global transaction time-out value if the **Transaction support** is set to **Disabled**, **Not Supported**, or **Supported**.</span></span>

     

4.  <span data-ttu-id="f10d5-117">В разделе время **ожидания транзакции** введите время ожидания транзакции в секундах.</span><span class="sxs-lookup"><span data-stu-id="f10d5-117">Under **Transaction Timeout**, enter the transaction time-out in seconds.</span></span> <span data-ttu-id="f10d5-118">По умолчанию время ожидания составляет 0 секунд, что означает, что компонент никогда не будет ждать истечения времени ожидания транзакции.</span><span class="sxs-lookup"><span data-stu-id="f10d5-118">The default time-out is 0 seconds, which means that the component will never cause the transaction to time out.</span></span>

5.  <span data-ttu-id="f10d5-119">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="f10d5-119">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f10d5-120">См. также</span><span class="sxs-lookup"><span data-stu-id="f10d5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f10d5-121">Управление автоматическими транзакциями в COM+</span><span class="sxs-lookup"><span data-stu-id="f10d5-121">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



