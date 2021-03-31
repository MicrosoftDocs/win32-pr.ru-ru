---
title: Проектирование интерфейсов, совместимых с 64-bit
description: Проблемы обратной совместимости возникают при добавлении новых типов данных или методов в интерфейс, изменении старых типов данных или неправильном использовании типов данных.
ms.assetid: 676affd8-a155-4ac2-9647-0c7352c87a31
keywords:
- Обратная совместимость 64-разрядное программирование для Windows
- 64-разрядные совместимые интерфейсы 64-разрядное программирование для Windows
- 64-разрядное руководством по программированию для Windows 64-разрядное программирование для Windows, совместимость
- совместимость с 64-разрядным программированием для Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebcde0e621d35cf216c2191f2e4b7da624dc274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329811"
---
# <a name="designing-64-bit-compatible-interfaces"></a><span data-ttu-id="b6fdb-107">Проектирование интерфейсов, совместимых с 64-bit</span><span class="sxs-lookup"><span data-stu-id="b6fdb-107">Designing 64-bit-Compatible Interfaces</span></span>

<span data-ttu-id="b6fdb-108">Перенос с 32-разрядной версии Windows на 64-bit Windows не должен самостоятельно создавать проблемы для распределенных приложений, независимо от того, используют ли они удаленный вызов процедур (RPC) напрямую или через DCOM.</span><span class="sxs-lookup"><span data-stu-id="b6fdb-108">Porting from 32-bit Windows to 64-bit Windows should not, by itself, create any problems for distributed applications, whether they use Remote Procedure Calls (RPC) directly or through DCOM.</span></span> <span data-ttu-id="b6fdb-109">Модель программирования RPC задает четко определенные размеры данных и целочисленные типы одинакового размера на каждом конце соединения.</span><span class="sxs-lookup"><span data-stu-id="b6fdb-109">The RPC programming model specifies well-defined data sizes and integer types that are the same size on each end of the connection.</span></span> <span data-ttu-id="b6fdb-110">Кроме того, в модели абстрактных данных LLP64, разработанной для 64-разрядных Windows, только указатели расширяются до 64 бит — все остальные целочисленные типы данных остаются в виде 32 бит.</span><span class="sxs-lookup"><span data-stu-id="b6fdb-110">Also, in the LLP64 abstract data model developed for 64-bit Windows, only the pointers expand to 64 bits—all other integer data types remain 32 bits.</span></span> <span data-ttu-id="b6fdb-111">Поскольку указатели являются локальными для каждой стороны соединения клиент/сервер и обычно передаются как маркеры **со значением NULL** или без **null** , механизм упаковки может прозрачно обработать разные размеры указателя на любом конце соединения.</span><span class="sxs-lookup"><span data-stu-id="b6fdb-111">Because pointers are local to each side of the client/server connection and are usually transmitted as **NULL** or non-**NULL** markers, the marshaling engine can handle different pointer sizes on either end of a connection transparently.</span></span>

<span data-ttu-id="b6fdb-112">Однако проблемы обратной совместимости возникают при добавлении новых типов данных или методов в интерфейс, изменении старых типов данных или неправильном использовании типов данных.</span><span class="sxs-lookup"><span data-stu-id="b6fdb-112">However, backward compatibility issues arise when you add new data types or methods to an interface, change old data types, or use data types inappropriately.</span></span> <span data-ttu-id="b6fdb-113">В следующих разделах описывается, как избежать таких ситуаций (по возможности) и как разработать надежные обходные пути, когда их невозможно избежать.</span><span class="sxs-lookup"><span data-stu-id="b6fdb-113">The following topics discuss how to avoid these situations (when possible) and how to design robust workarounds when it is not possible to avoid them.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b6fdb-114">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="b6fdb-114">In this Section</span></span>

-   [<span data-ttu-id="b6fdb-115">Изменение существующего интерфейса</span><span class="sxs-lookup"><span data-stu-id="b6fdb-115">Changing an Existing Interface</span></span>](changing-an-existing-interface.md)
-   [<span data-ttu-id="b6fdb-116">Предотвращение скрытия информации</span><span class="sxs-lookup"><span data-stu-id="b6fdb-116">Avoiding Information Hiding</span></span>](avoiding-information-hiding.md)
-   [<span data-ttu-id="b6fdb-117">Предотвращение полиморфизма</span><span class="sxs-lookup"><span data-stu-id="b6fdb-117">Avoiding Polymorphism</span></span>](avoiding-polymorphism.md)
-   [<span data-ttu-id="b6fdb-118">Использование новых типов данных в IDL-файле</span><span class="sxs-lookup"><span data-stu-id="b6fdb-118">Using New Data Types in Your IDL File</span></span>](using-new-data-types-in-your-idl-file.md)
-   [<span data-ttu-id="b6fdb-119">Подготовка приложения для 64-разрядной версии Windows</span><span class="sxs-lookup"><span data-stu-id="b6fdb-119">Preparing Your Application for 64-bit Windows</span></span>](preparing-your-application-for-64-bit-windows.md)

## <a name="related-sections"></a><span data-ttu-id="b6fdb-120">Связанные разделы</span><span class="sxs-lookup"><span data-stu-id="b6fdb-120">Related Sections</span></span>

<span data-ttu-id="b6fdb-121">Если вы еще не знакомы с новыми типами данных, рабочей средой и изменениями API для 64-разрядной версии Windows, см. статью [Подготовка к использованию 64-разрядной версии Windows](getting-ready-for-64-bit-windows.md).</span><span class="sxs-lookup"><span data-stu-id="b6fdb-121">If you are not already familiar with the new data types, working environment, and API changes for 64-bit Windows, see [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).</span></span>

 

 




