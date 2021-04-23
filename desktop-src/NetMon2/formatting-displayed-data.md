---
description: Сетевой монитор или библиотека DLL средства синтаксического анализа могут отформатировать данные, отображаемые в области сведений пользовательского интерфейса сетевой монитор.
ms.assetid: 60ab9253-ec0f-4c97-a475-ce2a74d469c4
title: Форматирование отображаемых данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017946dab9db443cf7083109dd75ccee1f6d278a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540218"
---
# <a name="formatting-displayed-data"></a><span data-ttu-id="eb0bc-103">Форматирование отображаемых данных</span><span class="sxs-lookup"><span data-stu-id="eb0bc-103">Formatting Displayed Data</span></span>

<span data-ttu-id="eb0bc-104">Сетевой монитор или библиотека DLL средства синтаксического анализа могут отформатировать данные, отображаемые в области сведений пользовательского интерфейса сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="eb0bc-104">Network Monitor or your parser DLL can format the data that is displayed in the details pane of the Network Monitor UI.</span></span>

<span data-ttu-id="eb0bc-105">Сетевой монитор предоставляет универсальный модуль форматирования, предоставляющий базовые службы, необходимые для вывода большинства типов данных, существующих в протоколе.</span><span class="sxs-lookup"><span data-stu-id="eb0bc-105">Network Monitor provides a generic formatter that provides the basic services needed to display most data types that exist within a protocol.</span></span> <span data-ttu-id="eb0bc-106">Однако универсальный модуль форматирования не поддерживает все типы данных.</span><span class="sxs-lookup"><span data-stu-id="eb0bc-106">However, the generic formatter does not support all data types.</span></span> <span data-ttu-id="eb0bc-107">Например, универсальный модуль форматирования не поддерживает следующее:</span><span class="sxs-lookup"><span data-stu-id="eb0bc-107">For example, the generic formatter does not support the following:</span></span>

-   <span data-ttu-id="eb0bc-108">Несколько типов адресов.</span><span class="sxs-lookup"><span data-stu-id="eb0bc-108">Several address types.</span></span>
-   <span data-ttu-id="eb0bc-109">Имена, понятные источнику и назначению.</span><span class="sxs-lookup"><span data-stu-id="eb0bc-109">Source and destination-friendly names.</span></span>
-   <span data-ttu-id="eb0bc-110">Идентификаторы объектов.</span><span class="sxs-lookup"><span data-stu-id="eb0bc-110">Object identifiers.</span></span>
-   <span data-ttu-id="eb0bc-111">Большие целочисленные типы данных.</span><span class="sxs-lookup"><span data-stu-id="eb0bc-111">Large integer data types.</span></span>
-   <span data-ttu-id="eb0bc-112">Небольшие целочисленные типы данных переменной длины.</span><span class="sxs-lookup"><span data-stu-id="eb0bc-112">Variable length small integer data types.</span></span>

<span data-ttu-id="eb0bc-113">Следующий пример определяет две форматированные строки для свойства идентификатора привилегии.</span><span class="sxs-lookup"><span data-stu-id="eb0bc-113">The following example identifies two formatted strings for the Privilege ID property.</span></span>

-   <span data-ttu-id="eb0bc-114">В первой строке кода показаны выходные данные универсального модуля форматирования.</span><span class="sxs-lookup"><span data-stu-id="eb0bc-114">The first line of code shows the output of the generic formatter.</span></span> <span data-ttu-id="eb0bc-115">Выходные данные основываются на типе данных.</span><span class="sxs-lookup"><span data-stu-id="eb0bc-115">The output is based on the data type.</span></span>
-   <span data-ttu-id="eb0bc-116">Вторая строка кода показывает выходные данные пользовательского модуля форматирования со строкой для данных свойства.</span><span class="sxs-lookup"><span data-stu-id="eb0bc-116">The second line of code shows the output of a custom formatter with a string to the property data.</span></span>

``` syntax
Privilege ID (PID) = 0x0029
Privilege ID   (PID) = 0x0029   The Process has privileges
```

> [!Note]  
> <span data-ttu-id="eb0bc-117">По возможности используйте универсальный модуль форматирования для вывода данных, так как он позволяет управлять размером библиотеки DLL средства синтаксического анализа и предоставляет более эффективные возможности кросс-платформенных функций для библиотеки DLL синтаксического анализатора.</span><span class="sxs-lookup"><span data-stu-id="eb0bc-117">When possible, use the generic formatter to display your data because it allows you to control the size of your parser DLL, and provides better cross-platform capabilities for your parser DLL.</span></span>

 

 

 



