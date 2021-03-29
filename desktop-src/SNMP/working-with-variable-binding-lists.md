---
title: Работа с списками привязок переменных
description: Переменная Binding — это связывание имени экземпляра объекта SNMP со связанным значением. Список привязок переменных представляет собой последовательность записей привязки переменных. В WinSNMP единица данных протокола (PDU) включает список переменных привязки.
ms.assetid: e6353ae7-1d32-4de4-8518-49864fcbfc57
keywords:
- Работа с списками привязки переменных SNMP
- Списки переменных привязки SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26719c7dc987e61542f38a0b86db78c573793f98
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "103788887"
---
# <a name="working-with-variable-binding-lists"></a><span data-ttu-id="d199a-107">Работа с списками привязок переменных</span><span class="sxs-lookup"><span data-stu-id="d199a-107">Working with Variable Binding Lists</span></span>

<span data-ttu-id="d199a-108">*Переменная Binding* — это связывание имени экземпляра объекта SNMP со связанным значением.</span><span class="sxs-lookup"><span data-stu-id="d199a-108">A *variable binding* is the pairing of an SNMP object instance name with an associated value.</span></span> <span data-ttu-id="d199a-109">*Список привязок переменных* представляет собой последовательность записей привязки переменных.</span><span class="sxs-lookup"><span data-stu-id="d199a-109">A *variable binding list* is a series of variable binding entries.</span></span> <span data-ttu-id="d199a-110">В WinSNMP единица данных протокола (PDU) включает список переменных привязки.</span><span class="sxs-lookup"><span data-stu-id="d199a-110">In WinSNMP, a protocol data unit (PDU) includes a variable binding list.</span></span>

<span data-ttu-id="d199a-111">Сведения о структуре списка привязок переменных ограничиваются реализацией Microsoft WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="d199a-111">The details of the variable binding list structure are restricted to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="d199a-112">WinSNMP-приложение может обращаться к списку привязок переменных с помощью маркера типа **хснмп \_ вбл**.</span><span class="sxs-lookup"><span data-stu-id="d199a-112">A WinSNMP application can access a variable binding list with a handle of type **HSNMP\_VBL**.</span></span> <span data-ttu-id="d199a-113">Дополнительные сведения см. в разделе [объекты обработчика ресурсов](resource-handle-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d199a-113">For more information, see [Resource Handle Objects](resource-handle-objects.md).</span></span>

<span data-ttu-id="d199a-114">В приложении WinSNMP можно создавать списки привязок переменных и управлять ими, а также включать их в устройства PDU.</span><span class="sxs-lookup"><span data-stu-id="d199a-114">The WinSNMP application can construct and manipulate variable binding lists, and include them in PDUs.</span></span> <span data-ttu-id="d199a-115">Для выполнения этих операций приложение использует [функции привязки переменной](winsnmp-functions.md)WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="d199a-115">To perform these operations, the application uses the WinSNMP [variable binding functions](winsnmp-functions.md).</span></span> <span data-ttu-id="d199a-116">Дополнительные сведения о работе с таблицей WinSNMP и переменными привязками см. в разделах, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d199a-116">For more information about working with WinSNMP and variable binding lists, see the topics listed in the following table.</span></span>



| <span data-ttu-id="d199a-117">Раздел</span><span class="sxs-lookup"><span data-stu-id="d199a-117">Topic</span></span>                                                                    | <span data-ttu-id="d199a-118">Описание</span><span class="sxs-lookup"><span data-stu-id="d199a-118">Description</span></span>                                      |
|--------------------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="d199a-119">Создание списка привязок переменных</span><span class="sxs-lookup"><span data-stu-id="d199a-119">Creating a Variable Binding List</span></span>](creating-a-variable-binding-list.md) | <span data-ttu-id="d199a-120">Описывает, как создать список привязок переменных.</span><span class="sxs-lookup"><span data-stu-id="d199a-120">Describes how to create a variable binding list.</span></span> |
| [<span data-ttu-id="d199a-121">Управление списком привязок переменных</span><span class="sxs-lookup"><span data-stu-id="d199a-121">Managing a Variable Binding List</span></span>](managing-a-variable-binding-list.md) | <span data-ttu-id="d199a-122">Описывает, как управлять списком привязок переменных.</span><span class="sxs-lookup"><span data-stu-id="d199a-122">Describes how to manage a variable binding list.</span></span> |



 

<span data-ttu-id="d199a-123">Дополнительные сведения о привязках переменных и списках привязок переменных см. в разделе [RFC1905](https://www.ietf.org/rfc/rfc1905.txt), "операции протокола для версии 2 протокола простого сетевого управления (SNMPv2)" и [функции привязки переменной](winsnmp-functions.md)WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="d199a-123">For more information about variable bindings and variable binding lists, see [RFC1905](https://www.ietf.org/rfc/rfc1905.txt), "Protocol Operations for Version 2 of the Simple Network Management Protocol (SNMPv2)," and the WinSNMP [Variable Binding Functions](winsnmp-functions.md).</span></span>

 

 




