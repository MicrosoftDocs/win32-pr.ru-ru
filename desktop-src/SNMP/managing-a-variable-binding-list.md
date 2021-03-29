---
title: Управление списком привязок переменных
description: Функция Снмпжетвб получает сведения о привязке переменных из списка привязок переменных. Функция получает имя переменной и связанное с переменной значение из записи привязки переменной, указанной в приложении WinSNMP.
ms.assetid: 357aebd6-171a-4221-b12a-712702f9d9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc8c1cbfa4eb0ec3acdc13e9c9cc480b88ddae8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067727"
---
# <a name="managing-a-variable-binding-list"></a><span data-ttu-id="1ae8b-104">Управление списком привязок переменных</span><span class="sxs-lookup"><span data-stu-id="1ae8b-104">Managing a Variable Binding List</span></span>

<span data-ttu-id="1ae8b-105">Функция [**снмпжетвб**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) получает сведения о привязке переменных из списка привязок переменных.</span><span class="sxs-lookup"><span data-stu-id="1ae8b-105">The [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) function retrieves variable binding information from a variable binding list.</span></span> <span data-ttu-id="1ae8b-106">Функция получает имя переменной и связанное с переменной значение из записи привязки переменной, указанной в приложении WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="1ae8b-106">The function retrieves the variable name and the variable's associated value from the variable binding entry specified by the WinSNMP application.</span></span>

<span data-ttu-id="1ae8b-107">Чтобы обновить записи привязки переменных в списке привязок переменных, вызовите функцию [**снмпсетвб**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) .</span><span class="sxs-lookup"><span data-stu-id="1ae8b-107">To update variable binding entries in a variable binding list, call the [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) function.</span></span> <span data-ttu-id="1ae8b-108">Функция **снмпсетвб** также добавляет новые записи привязки переменных в существующий список привязок переменных.</span><span class="sxs-lookup"><span data-stu-id="1ae8b-108">The **SnmpSetVb** function also appends new variable binding entries to an existing variable binding list.</span></span>

<span data-ttu-id="1ae8b-109">Для удаления записей из списка привязок переменных в приложении WinSNMP необходимо вызвать функцию [**снмпделетевб**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) .</span><span class="sxs-lookup"><span data-stu-id="1ae8b-109">The WinSNMP application must call the [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) function to remove entries from a variable binding list.</span></span>

<span data-ttu-id="1ae8b-110">Чтобы получить, изменить или удалить запись привязки переменной, в приложении WinSNMP необходимо указать расположение записи в списке привязок переменных.</span><span class="sxs-lookup"><span data-stu-id="1ae8b-110">To retrieve, modify or delete a variable binding entry, the WinSNMP application must specify the position of the entry in the variable binding list.</span></span>

<span data-ttu-id="1ae8b-111">Вызов функции [**снмпсетпдудата**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) связывает список привязок ПЕРЕМЕННЫХ с PDU.</span><span class="sxs-lookup"><span data-stu-id="1ae8b-111">A call to the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function associates a variable binding list with a PDU.</span></span> <span data-ttu-id="1ae8b-112">Вызов функции [**снмпжетпдудата**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) извлекает список привязок ПЕРЕМЕННЫХ из PDU.</span><span class="sxs-lookup"><span data-stu-id="1ae8b-112">A call to the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) function retrieves a variable binding list from a PDU.</span></span> <span data-ttu-id="1ae8b-113">Отдельная привязка переменных напрямую не связана с PDU, но она косвенно связана путем его включения в список привязок переменных.</span><span class="sxs-lookup"><span data-stu-id="1ae8b-113">An individual variable binding is not directly associated with a PDU, but it is indirectly associated through its inclusion in a variable binding list.</span></span>

 

 




