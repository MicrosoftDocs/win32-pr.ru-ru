---
description: В отличие от удаления динамического экземпляра, удаление класса является простой процедурой.
ms.assetid: bc0ee1e8-7515-4f35-ace3-6344c2ef0ab8
ms.tgt_platform: multiple
title: Удаление класса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3d9ce149b5eff0f5202cb25c5f7d16fdf44291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702721"
---
# <a name="deleting-a-class"></a><span data-ttu-id="814dc-103">Удаление класса</span><span class="sxs-lookup"><span data-stu-id="814dc-103">Deleting a Class</span></span>

<span data-ttu-id="814dc-104">В отличие от удаления динамического экземпляра, удаление класса является простой процедурой.</span><span class="sxs-lookup"><span data-stu-id="814dc-104">Unlike deleting a dynamic instance, deleting a class is a simple procedure.</span></span> <span data-ttu-id="814dc-105">Однако, как обсуждалось ранее, базовые или производные классы редко удаляются.</span><span class="sxs-lookup"><span data-stu-id="814dc-105">However, as discussed earlier, base or derived classes are rarely deleted.</span></span> <span data-ttu-id="814dc-106">Вместо этого экземпляр чаще всего удаляется.</span><span class="sxs-lookup"><span data-stu-id="814dc-106">Instead, an instance is more commonly deleted.</span></span> <span data-ttu-id="814dc-107">[API скриптов для WMI](scripting-api-for-wmi.md) использует те же методы для удаления объекта класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="814dc-107">The [Scripting API for WMI](scripting-api-for-wmi.md) uses the same methods to delete either a class object or an instance.</span></span> <span data-ttu-id="814dc-108">Дополнительные сведения см. в разделе [Удаление экземпляра](deleting-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="814dc-108">For more information, see [Deleting an Instance](deleting-an-instance.md).</span></span> <span data-ttu-id="814dc-109">Сведения об удалении классов и экземпляров из репозитория WMI см. в описании команды препроцессора [**pragma делетекласс**](pragma-deleteclass.md) .</span><span class="sxs-lookup"><span data-stu-id="814dc-109">For information about removing classes and instances from the WMI repository, see the [**pragma deleteclass**](pragma-deleteclass.md) preprocessor command.</span></span>

<span data-ttu-id="814dc-110">[Интерфейс API COM для WMI](com-api-for-wmi.md) имеет различные методы для удаления экземпляра и удаления объекта.</span><span class="sxs-lookup"><span data-stu-id="814dc-110">The [COM API for WMI](com-api-for-wmi.md) has different methods for deleting an instance and deleting an object.</span></span>

<span data-ttu-id="814dc-111">В следующей процедуре описывается удаление базового класса или производного класса.</span><span class="sxs-lookup"><span data-stu-id="814dc-111">The following procedure describes how to delete a base class or derived class.</span></span>

<span data-ttu-id="814dc-112">**Удаление базового класса или производного класса**</span><span class="sxs-lookup"><span data-stu-id="814dc-112">**To delete a base class or derived class**</span></span>

-   <span data-ttu-id="814dc-113">Вызовите метод [**IWbemServices::D елетекласс**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) или [**IWbemServices::D елетеклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) .</span><span class="sxs-lookup"><span data-stu-id="814dc-113">Call either the [**IWbemServices::DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) or [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) method.</span></span>

    <span data-ttu-id="814dc-114">Как видно из названия, [**делетеклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) удаляет экземпляр асинхронно, в то время как [**делетекласс**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) удаляет экземпляр синхронно.</span><span class="sxs-lookup"><span data-stu-id="814dc-114">As the name suggests, [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) deletes an instance asynchronously while [**DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) deletes an instance synchronously.</span></span> <span data-ttu-id="814dc-115">Чтобы использовать **делетеклассасинк**, необходимо также реализовать объект [**ивбемобжектсинк**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="814dc-115">To use **DeleteClassAsync**, you must also implement an [**IWbemObjectSink**](iwbemobjectsink.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="814dc-116">Поскольку обратный вызов приемника может не возвращаться на том же уровне проверки подлинности, что и клиент, рекомендуется использовать семисинчронаус вместо асинхронного взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="814dc-116">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="814dc-117">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="814dc-117">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 

 



