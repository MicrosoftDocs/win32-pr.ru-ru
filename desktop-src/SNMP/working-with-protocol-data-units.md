---
title: Работа с единицами данных протокола
description: Протокол SNMP отправляет запросы и ответы операций в виде SNMP-сообщений.
ms.assetid: 0928981c-4d60-4583-9eef-8127e05b1ba8
keywords:
- Работа с единицами данных протокола SNMP
- Протоколы единиц данных протокола SNMP, работа с
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e40f36fa28f7ff17974d79f4f8ac29b8b6130b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068293"
---
# <a name="working-with-protocol-data-units"></a><span data-ttu-id="45f8d-105">Работа с единицами данных протокола</span><span class="sxs-lookup"><span data-stu-id="45f8d-105">Working with Protocol Data Units</span></span>

<span data-ttu-id="45f8d-106">Протокол SNMP отправляет запросы и ответы операций в виде SNMP-сообщений.</span><span class="sxs-lookup"><span data-stu-id="45f8d-106">The Simple Network Management Protocol (SNMP) sends operation requests and responses as SNMP messages.</span></span> <span data-ttu-id="45f8d-107">SNMP-сообщение — это единица данных протокола SNMP (PDU), а также дополнительные элементы заголовка сообщения, определенные соответствующим RFC.</span><span class="sxs-lookup"><span data-stu-id="45f8d-107">An SNMP message is an SNMP protocol data unit (PDU) plus additional message header elements defined by the relevant RFC.</span></span> <span data-ttu-id="45f8d-108">PDU включает список привязок переменных.</span><span class="sxs-lookup"><span data-stu-id="45f8d-108">A PDU includes a variable binding list.</span></span>

<span data-ttu-id="45f8d-109">Структура PDU ограничена реализацией Microsoft WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="45f8d-109">The structure of a PDU is restricted to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="45f8d-110">Приложение WinSNMP может получить доступ к PDU с помощью маркера типа **хснмп \_ PDU**.</span><span class="sxs-lookup"><span data-stu-id="45f8d-110">A WinSNMP application can access a PDU with a handle of the type **HSNMP\_PDU**.</span></span> <span data-ttu-id="45f8d-111">Приложение WinSNMP должно создать PDU перед вызовом функции [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) или функции [**снмпенкодемсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) .</span><span class="sxs-lookup"><span data-stu-id="45f8d-111">The WinSNMP application must create a PDU before it calls the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function or the [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) function.</span></span>

<span data-ttu-id="45f8d-112">Приложение может извлекать и обновлять элементы данных PDU, а также освобождать ресурсы, выделенные для PDU.</span><span class="sxs-lookup"><span data-stu-id="45f8d-112">The application can extract and update the data elements of a PDU, and release resources allocated for PDUs.</span></span> <span data-ttu-id="45f8d-113">Для выполнения этих операций приложение использует [функции WinSNMP PDU](winsnmp-functions.md).</span><span class="sxs-lookup"><span data-stu-id="45f8d-113">To perform these operations, the application uses the WinSNMP [PDU functions](winsnmp-functions.md).</span></span> <span data-ttu-id="45f8d-114">В следующей таблице перечислены разделы, в которых рассматривается работа с PDU в среде программирования WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="45f8d-114">The following table lists topics that discuss working with PDUs in the WinSNMP programming environment.</span></span>



| <span data-ttu-id="45f8d-115">Раздел</span><span class="sxs-lookup"><span data-stu-id="45f8d-115">Topic</span></span>                                                                        | <span data-ttu-id="45f8d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="45f8d-116">Description</span></span>                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="45f8d-117">Создание PDU</span><span class="sxs-lookup"><span data-stu-id="45f8d-117">Creating a PDU</span></span>](creating-a-pdu.md)                                         | <span data-ttu-id="45f8d-118">Описывает, как создать PDU.</span><span class="sxs-lookup"><span data-stu-id="45f8d-118">Describes how to create a PDU.</span></span>                                     |
| [<span data-ttu-id="45f8d-119">Обновление PDU</span><span class="sxs-lookup"><span data-stu-id="45f8d-119">Updating a PDU</span></span>](updating-a-pdu.md)                                         | <span data-ttu-id="45f8d-120">Описывает, как извлекать и обновлять поля PDU.</span><span class="sxs-lookup"><span data-stu-id="45f8d-120">Describes how to retrieve and update PDU fields.</span></span>                   |
| [<span data-ttu-id="45f8d-121">Дублирование PDU</span><span class="sxs-lookup"><span data-stu-id="45f8d-121">Duplicating a PDU</span></span>](duplicating-a-pdu.md)                                   | <span data-ttu-id="45f8d-122">Описывает, как дублировать PDU.</span><span class="sxs-lookup"><span data-stu-id="45f8d-122">Describes how to duplicate a PDU.</span></span>                                  |
| [<span data-ttu-id="45f8d-123">Проверка PDU</span><span class="sxs-lookup"><span data-stu-id="45f8d-123">Validating a PDU</span></span>](validating-a-pdu.md)                                     | <span data-ttu-id="45f8d-124">Описывает проверку PDU.</span><span class="sxs-lookup"><span data-stu-id="45f8d-124">Describes the validation of a PDU.</span></span>                                 |
| [<span data-ttu-id="45f8d-125">Сопоставление устройств распределения питания и запросов</span><span class="sxs-lookup"><span data-stu-id="45f8d-125">Matching Response and Request PDUs</span></span>](matching-response-and-request-pdus.md) | <span data-ttu-id="45f8d-126">Описывает процесс сопоставления PDU ответа с PDU запроса.</span><span class="sxs-lookup"><span data-stu-id="45f8d-126">Describes the process of matching a response PDU to a request PDU.</span></span> |



 

<span data-ttu-id="45f8d-127">Дополнительные сведения см. в разделе [Работа с списками привязок переменных](working-with-variable-binding-lists.md) и [объектами обработчика ресурсов](resource-handle-objects.md).</span><span class="sxs-lookup"><span data-stu-id="45f8d-127">For more information, see [Working with Variable Binding Lists](working-with-variable-binding-lists.md) and [Resource Handle Objects](resource-handle-objects.md).</span></span>

 

 




