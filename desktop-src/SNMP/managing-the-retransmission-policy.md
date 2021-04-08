---
title: Управление политикой повторной передачи
description: WinSNMP Application может запросить, чтобы реализация Microsoft WinSNMP выполняла политику повторной передачи приложения. Когда реализация управляет повторной передачей, она использует время ожидания и значения счетчика повторных попыток в своей базе данных.
ms.assetid: 1f1a9589-3566-4d90-ac4d-7acf69f34676
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f2e47d983f8da62ccb8ffbe9c20b35c71bfbb70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068304"
---
# <a name="managing-the-retransmission-policy"></a><span data-ttu-id="a2c44-104">Управление политикой повторной передачи</span><span class="sxs-lookup"><span data-stu-id="a2c44-104">Managing the Retransmission Policy</span></span>

<span data-ttu-id="a2c44-105">WinSNMP Application может запросить, чтобы реализация Microsoft WinSNMP выполняла политику повторной передачи приложения.</span><span class="sxs-lookup"><span data-stu-id="a2c44-105">The WinSNMP application can request that the Microsoft WinSNMP implementation execute the application's retransmission policy.</span></span> <span data-ttu-id="a2c44-106">Когда реализация управляет повторной передачей, она использует время ожидания и значения счетчика повторных попыток в своей базе данных.</span><span class="sxs-lookup"><span data-stu-id="a2c44-106">When the implementation manages retransmission, it uses the time-out period and the retry count values in its database.</span></span>

<span data-ttu-id="a2c44-107">Реализация определяет режим повторной отправки по умолчанию в возвращаемом значении функции [**снмпстартуп**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) во время инициализации.</span><span class="sxs-lookup"><span data-stu-id="a2c44-107">The implementation identifies the default retransmission mode in a return value from the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function during initialization.</span></span> <span data-ttu-id="a2c44-108">Режим может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a2c44-108">The mode can be one of the following values.</span></span>



| <span data-ttu-id="a2c44-109">Значение</span><span class="sxs-lookup"><span data-stu-id="a2c44-109">Value</span></span>        | <span data-ttu-id="a2c44-110">Значение</span><span class="sxs-lookup"><span data-stu-id="a2c44-110">Meaning</span></span>                                                                      |
|--------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a2c44-111">СНМПАПИ \_</span><span class="sxs-lookup"><span data-stu-id="a2c44-111">SNMPAPI\_ON</span></span>  | <span data-ttu-id="a2c44-112">Реализация исполняет политику повторной передачи приложения.</span><span class="sxs-lookup"><span data-stu-id="a2c44-112">The implementation is executing the application's retransmission policy.</span></span>     |
| <span data-ttu-id="a2c44-113">СНМПАПИ \_</span><span class="sxs-lookup"><span data-stu-id="a2c44-113">SNMPAPI\_OFF</span></span> | <span data-ttu-id="a2c44-114">Реализация не выполняла политику повторной передачи приложения.</span><span class="sxs-lookup"><span data-stu-id="a2c44-114">The implementation is not executing the application's retransmission policy.</span></span> |



 

<span data-ttu-id="a2c44-115">Приложение WinSNMP может извлекаться в любой момент, когда текущий режим повторной передачи действует для реализации путем вызова функции [**снмпжетретрансмитмоде**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) .</span><span class="sxs-lookup"><span data-stu-id="a2c44-115">A WinSNMP application can retrieve at any time the current retransmission mode in effect for the implementation by calling the [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) function.</span></span> <span data-ttu-id="a2c44-116">API-интерфейс WinSNMP предоставляет другие [функции базы данных](winsnmp-functions.md) , упрощающие управление политикой повторной передачи.</span><span class="sxs-lookup"><span data-stu-id="a2c44-116">The WinSNMP API provides other [database functions](winsnmp-functions.md) that simplify management of the retransmission policy.</span></span>

<span data-ttu-id="a2c44-117">В любой момент во время выполнения программы программа WinSNMP может настроить выполнение политики, выполнив одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="a2c44-117">At any time during program execution, the WinSNMP application can adjust execution of the policy by performing one of the following steps:</span></span>

-   <span data-ttu-id="a2c44-118">Запросите, что реализация запускает или останавливает выполнение политики повторной передачи, вызвав функцию [**снмпсетретрансмитмоде**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) .</span><span class="sxs-lookup"><span data-stu-id="a2c44-118">Request that the implementation start or stop executing the retransmission policy by calling the [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) function.</span></span> <span data-ttu-id="a2c44-119">Дополнительные сведения см. [в разделе Включение и отключение](turning-retransmission-on-and-off.md)повторной передачи.</span><span class="sxs-lookup"><span data-stu-id="a2c44-119">For more information, see [Turning Retransmission On and Off](turning-retransmission-on-and-off.md).</span></span>
-   <span data-ttu-id="a2c44-120">Измените период ожидания и значения счетчика повторных попыток в базе данных реализации.</span><span class="sxs-lookup"><span data-stu-id="a2c44-120">Modify the time-out period and retry count values in the implementation's database.</span></span> <span data-ttu-id="a2c44-121">Дополнительные сведения см. [в разделе изменение политики](changing-the-retransmission-policy.md)повторной передачи.</span><span class="sxs-lookup"><span data-stu-id="a2c44-121">For more information, see [Changing the Retransmission Policy](changing-the-retransmission-policy.md).</span></span>
-   <span data-ttu-id="a2c44-122">Вызовите функцию [**снмпканцелмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) , чтобы отменить цикл повторной передачи и освободить внутренние структуры данных, связанные с одним запросом SNMP-сообщения.</span><span class="sxs-lookup"><span data-stu-id="a2c44-122">Call the [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) function to cancel the retransmission cycle and release internal data structures associated with a single SNMP message request.</span></span> <span data-ttu-id="a2c44-123">Дополнительные сведения см. в разделе Отмена повторной [передачи](canceling-retransmission.md).</span><span class="sxs-lookup"><span data-stu-id="a2c44-123">For more information, see [Canceling Retransmission](canceling-retransmission.md).</span></span>

<span data-ttu-id="a2c44-124">Приложение может выполнять собственную политику повторной передачи.</span><span class="sxs-lookup"><span data-stu-id="a2c44-124">The application can execute its own retransmission policy.</span></span> <span data-ttu-id="a2c44-125">В этом случае выполнение может быть основано на значениях в базе данных.</span><span class="sxs-lookup"><span data-stu-id="a2c44-125">In this case, execution may or may not be based on the values in the database.</span></span>

 

 




