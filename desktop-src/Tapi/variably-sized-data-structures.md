---
description: Если для передачи информации между TAPI и приложением используются вариабли структуры данных, приложение отвечает за выделение необходимого объема памяти.
ms.assetid: f1e2e864-fa10-4058-ba56-faa0ba7363a1
title: Вариабли структуры данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873fcbaa1e4e3bda772d92ad2de9b1f6258363cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266230"
---
# <a name="variably-sized-data-structures"></a><span data-ttu-id="315ad-103">Вариабли структуры данных</span><span class="sxs-lookup"><span data-stu-id="315ad-103">Variably Sized Data Structures</span></span>

<span data-ttu-id="315ad-104">Если для передачи информации между TAPI и приложением используются вариабли структуры данных, приложение отвечает за выделение необходимого объема памяти.</span><span class="sxs-lookup"><span data-stu-id="315ad-104">When variably sized data structures are used to transmit information between TAPI and the application, the application is responsible for allocating the necessary memory.</span></span> <span data-ttu-id="315ad-105">Объем выделенной памяти должен быть не менее велик для фиксированной части структуры данных и задается приложением в элементе **двтоталсизе** структуры данных.</span><span class="sxs-lookup"><span data-stu-id="315ad-105">The amount of memory allocated must be at least large enough for the fixed portion of the data structure, and is set by the application in the **dwTotalSize** member of the data structure.</span></span> <span data-ttu-id="315ad-106">Члены **двуседсизе** и **двнидедсизе** заполняются TAPI.</span><span class="sxs-lookup"><span data-stu-id="315ad-106">The **dwUsedSize** and **dwNeededSize** members are filled in by TAPI.</span></span> <span data-ttu-id="315ad-107">Если **двтоталсизе** меньше размера фиксированной части, возвращается ЛИНИРР/фонирр \_ структуретусмалл.</span><span class="sxs-lookup"><span data-stu-id="315ad-107">If **dwTotalSize** is less than the size of the fixed portion, then LINEERR/ PHONEERR\_STRUCTURETOOSMALL is returned.</span></span> <span data-ttu-id="315ad-108">Если функция возвращает значение Success, то все поля в фиксированной части были заполнены.</span><span class="sxs-lookup"><span data-stu-id="315ad-108">If a function returns success, then all the fields in the fixed portion have been filled in.</span></span> <span data-ttu-id="315ad-109">Члены **двуседсизе** и **двнидедсизе** можно сравнивать, чтобы определить, были ли заполнены все переменные части, и сколько пространства потребуется для их заполнения.</span><span class="sxs-lookup"><span data-stu-id="315ad-109">The **dwUsedSize** and **dwNeededSize** members can be compared to determine if all variable parts have been filled in, and how much space would be required to fill them all in.</span></span>

<span data-ttu-id="315ad-110">Если **двнидедсизе** равен **двуседсизе**, то все фиксированные и переменные части были заполнены.</span><span class="sxs-lookup"><span data-stu-id="315ad-110">If **dwNeededSize** is equal to **dwUsedSize**, then all fixed and variable parts have been filled in.</span></span> <span data-ttu-id="315ad-111">Если **двнидедсизе** больше **двуседсизе**, некоторые переменные части могут быть заполнены, но точно, какие поля вариабли размера заполнены, не определены.</span><span class="sxs-lookup"><span data-stu-id="315ad-111">If **dwNeededSize** is larger than **dwUsedSize**, some variable parts may have been filled in, but exactly which variably sized fields have been filled in is undefined.</span></span> <span data-ttu-id="315ad-112">Ни одна переменная часть не усекается, а переменные части, которые были бы усечены из-за недостаточного места, выделены, если обе соответствующие части "offset" и "size" имеют нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="315ad-112">No variable part is ever truncated, and variable parts that would have been truncated due to insufficient space are indicated by having both of their corresponding "Offset" and "Size" parts set to zero.</span></span> <span data-ttu-id="315ad-113">Если они не равны нулю (и ошибки не были возвращены), они указывают смещение и размер допустимых неусеченных данных частей переменной.</span><span class="sxs-lookup"><span data-stu-id="315ad-113">If these are not both zero (and no error was returned), they indicate the offset and size of valid, nontruncated variable-part data.</span></span>

<span data-ttu-id="315ad-114">Приложение всегда может гарантировать заполнение всех переменных частей путем выделения и указания **двнидедсизе** байтов для структуры и повторного вызова функции Get до тех пор, пока функция не вернет значение Success и **двнидедсизе** равно **двуседсизе**.</span><span class="sxs-lookup"><span data-stu-id="315ad-114">An application can always guarantee that all variable parts are filled in by allocating and indicating **dwNeededSize** bytes for the structure and calling the "Get" function again until the function returns success and **dwNeededSize** equals **dwUsedSize**.</span></span> <span data-ttu-id="315ad-115">Это должно произойти во второй раз, за исключением ситуаций состязания, которые приводят к изменению размера переменных частей между вызовами, что должно быть редким событием.</span><span class="sxs-lookup"><span data-stu-id="315ad-115">This should happen on the second try except for race conditions that cause changes in the size of variable parts between calls, which should be a rare occurrence.</span></span>

> [!Note]  
> <span data-ttu-id="315ad-116">Все текстовые строки, независимо от кодировки, в структурах размера вариабли должны **завершаться нулем в** соответствии с обычными соглашениями об обработке строк C.</span><span class="sxs-lookup"><span data-stu-id="315ad-116">All text strings, regardless of encoding, in variably sized structures should be **NULL**-terminated according to normal C string-handling conventions.</span></span>

 

 

 



