---
description: Чтобы удалить из системы счетчики производительности приложений, выполните следующие действия.
ms.assetid: 40fc9831-1025-4052-a941-70767ee4e10f
title: Удаление счетчиков производительности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba257a1a44b5272543b7e61dcdc4b4e96225c160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663242"
---
# <a name="deleting-performance-counters"></a><span data-ttu-id="7a495-103">Удаление счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="7a495-103">Deleting Performance Counters</span></span>

<span data-ttu-id="7a495-104">Чтобы удалить счетчики производительности приложения из системы, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7a495-104">To remove your application's performance counters from the system, perform the following steps.</span></span>

1.  <span data-ttu-id="7a495-105">С помощью средства **lodctr** , входящего в состав компьютера, удалите из реестра данные, связанные со счетчиком.</span><span class="sxs-lookup"><span data-stu-id="7a495-105">Use the **unlodctr** tool included with the computer to remove the counter related data from the registry.</span></span> <span data-ttu-id="7a495-106">Обратите внимание, что для выполнения средства **lodctr** должен существовать ключ **производительности** приложения.</span><span class="sxs-lookup"><span data-stu-id="7a495-106">Note that the application's **Performance** key must exist for the **unlodctr** tool to succeed.</span></span> <span data-ttu-id="7a495-107">Дополнительные сведения см. [в разделе Удаление имен и описаний счетчиков из реестра](removing-counter-names-and-descriptions-from-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="7a495-107">For details, see [Removing Counter Names and Descriptions from the Registry](removing-counter-names-and-descriptions-from-the-registry.md).</span></span>
2.  <span data-ttu-id="7a495-108">Удалите ключи **производительности** и **компоновки** в разделе **служб** приложения.</span><span class="sxs-lookup"><span data-stu-id="7a495-108">Delete the **Performance** and **Linkage** keys under the application's **Services** key.</span></span> <span data-ttu-id="7a495-109">Чтобы удалить эти ключи, используйте либо служебную программу Regedt32.exe, либо вызов [**регделетекэй**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya).</span><span class="sxs-lookup"><span data-stu-id="7a495-109">To delete these keys, use either the Regedt32.exe utility or call [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya).</span></span>

 

 
