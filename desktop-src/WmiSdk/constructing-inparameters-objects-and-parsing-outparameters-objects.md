---
description: Как правило, прямой доступ подходит для вызова метода поставщика WMI.
ms.assetid: be9332b5-8094-44a2-8632-af9957ecf36b
ms.tgt_platform: multiple
title: Построение объектов параметров и анализ объектов параметров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a291d4fd44e69e87572684856bba587685e1f07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998981"
---
# <a name="constructing-inparameters-objects-and-parsing-outparameters-objects"></a><span data-ttu-id="86d62-103">Построение объектов параметров и анализ объектов параметров</span><span class="sxs-lookup"><span data-stu-id="86d62-103">Constructing InParameters Objects and Parsing OutParameters Objects</span></span>

<span data-ttu-id="86d62-104">Как правило, прямой доступ подходит для вызова [*метода поставщика*](gloss-p.md)WMI.</span><span class="sxs-lookup"><span data-stu-id="86d62-104">Normally, direct access is adequate to call a WMI [*provider method*](gloss-p.md).</span></span> <span data-ttu-id="86d62-105">Прямой доступ означает исполнение метода с помощью синтаксиса *Object. Method* .</span><span class="sxs-lookup"><span data-stu-id="86d62-105">Direct access means executing a method by using *object.method* syntax.</span></span> <span data-ttu-id="86d62-106">Однако в некоторых случаях нельзя использовать прямой доступ.</span><span class="sxs-lookup"><span data-stu-id="86d62-106">However, in some cases, direct access cannot be used.</span></span> <span data-ttu-id="86d62-107">Кроме того, для асинхронного вызова метода поставщика из скрипта требуется тип вызова [**ексекмесодасинк**](swbemobject-execmethodasync-.md) .</span><span class="sxs-lookup"><span data-stu-id="86d62-107">Also, calling a provider method asynchronously from a script requires an [**ExecMethodAsync**](swbemobject-execmethodasync-.md) type of call.</span></span>

> [!Note]  
> <span data-ttu-id="86d62-108">Поскольку обратный вызов приемника может не возвращаться на том же уровне проверки подлинности, что и клиент, рекомендуется использовать семисинчронаус вместо асинхронного взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="86d62-108">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="86d62-109">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="86d62-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="86d62-110">Порядок входных и выходных параметров метода определяется в схеме MOF-файл (MOF) для метода.</span><span class="sxs-lookup"><span data-stu-id="86d62-110">The order of method input and output parameters is defined in the Managed Object Format (MOF) schema for the method.</span></span> <span data-ttu-id="86d62-111">Инструментарий WMI не предотвращает изменение порядка параметров при повторной компиляции класса с помощью [mofcomp](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="86d62-111">WMI does not prevent the parameter order from being changed when the class is recompiled by [mofcomp](mofcomp.md).</span></span> <span data-ttu-id="86d62-112">Используя объект [**параметров**](swbemmethod-inparameters.md) , можно избежать проблем, вызванных измененной схемой, поскольку входные параметры идентифицируются по имени.</span><span class="sxs-lookup"><span data-stu-id="86d62-112">By using an [**InParameters**](swbemmethod-inparameters.md) object, you can avoid problems that result from changed schema because the input parameters are identified by name.</span></span> <span data-ttu-id="86d62-113">Правильный параметр можно увидеть, изучив квалификатор **идентификатора** каждого входного параметра.</span><span class="sxs-lookup"><span data-stu-id="86d62-113">The correct parameter can be seen by examining the **ID** qualifier of each input parameter.</span></span> <span data-ttu-id="86d62-114">Первый параметр имеет значение **ID** , равное 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="86d62-114">The first parameter has an **ID** value of 0 (zero).</span></span>

<span data-ttu-id="86d62-115">Методы [**SWbemObject.Exeкмесод \_**](swbemobject-execmethod-.md), [**SWbemObject.Exeкмесодасинк \_**](swbemobject-execmethodasync-.md), [**SWbemServices.Exeкмесод**](swbemservices-execmethod.md)и [**SWbemServices.Exeкмесодасинк**](swbemservices-execmethodasync.md) предоставляют альтернативный способ выполнения метода поставщика в случаях, когда невозможно выполнить метод напрямую.</span><span class="sxs-lookup"><span data-stu-id="86d62-115">[**The SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md), [**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), and [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) methods provide an alternate way to execute a provider method in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="86d62-116">Дополнительные сведения см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="86d62-116">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="86d62-117">Дополнительные сведения о параметрах см. в разделе [Построение объектов](constructing-inparameters-objects.md) параметров и [анализ объектов параметров](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="86d62-117">For more information about parameters, see [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span>

 

 



