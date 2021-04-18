---
description: Прежде чем приступить к разработке приложения служб Microsoft Windows HTTP (WinHTTP), необходимо сначала решить, следует ли использовать API C/C++ или COM-интерфейс.
ms.assetid: 451ad247-962f-4af1-bb21-0aed4ef5f93c
title: Выбор интерфейса WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc529e6052b0de2de19a7c15ff1cfad226cee2cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712127"
---
# <a name="choosing-a-winhttp-interface"></a><span data-ttu-id="2a534-103">Выбор интерфейса WinHTTP</span><span class="sxs-lookup"><span data-stu-id="2a534-103">Choosing a WinHTTP Interface</span></span>

<span data-ttu-id="2a534-104">Прежде чем приступить к разработке приложения служб Microsoft Windows HTTP (WinHTTP), необходимо сначала решить, следует ли использовать API C/C++ или COM-интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2a534-104">Before you begin to develop a Microsoft Windows HTTP Services (WinHTTP) application, you must first decide whether to use the C/C++ API or the COM interface.</span></span> <span data-ttu-id="2a534-105">В следующей таблице перечислены преимущества и недостатки, связанные с каждым из этих подходов.</span><span class="sxs-lookup"><span data-stu-id="2a534-105">The following table summarizes the advantages and disadvantages associated with each of these approaches.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="2a534-106">API C/C++</span><span class="sxs-lookup"><span data-stu-id="2a534-106">C/C++ API</span></span></th>
<th><span data-ttu-id="2a534-107">Интерфейс COM</span><span class="sxs-lookup"><span data-stu-id="2a534-107">COM interface</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a534-108">Преимущества</span><span class="sxs-lookup"><span data-stu-id="2a534-108">Advantages</span></span></td>
<td><ul>
<li><span data-ttu-id="2a534-109">Ответы могут обрабатываться в виде фрагментов, что является более эффективным.</span><span class="sxs-lookup"><span data-stu-id="2a534-109">Responses can be processed in chunks, which is more efficient.</span></span></li>
<li><span data-ttu-id="2a534-110">Операции POST также можно обрабатывать в виде фрагментов, ускоряя время обработки.</span><span class="sxs-lookup"><span data-stu-id="2a534-110">POST operations can also be processed in chunks, speeding processing time.</span></span></li>
<li><span data-ttu-id="2a534-111">Поддержка автопрокси.</span><span class="sxs-lookup"><span data-stu-id="2a534-111">AutoProxy support.</span></span></li>
<li><span data-ttu-id="2a534-112">Доступ к полному набору функций WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="2a534-112">Access to the full feature set of WinHTTP.</span></span></li>
<li><span data-ttu-id="2a534-113">Двоичные данные можно легко обрабатывать.</span><span class="sxs-lookup"><span data-stu-id="2a534-113">Binary data can easily be handled.</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2a534-114">Создание приложения несложно и требует меньше строк кода, чем API C/C++.</span><span class="sxs-lookup"><span data-stu-id="2a534-114">Creating an application is easy and requires fewer lines of code than the C/C++ API.</span></span></li>
<li><span data-ttu-id="2a534-115">Интерфейс может использоваться в языках сценариев.</span><span class="sxs-lookup"><span data-stu-id="2a534-115">The interface can be used by scripting languages.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a534-116">Недостатки</span><span class="sxs-lookup"><span data-stu-id="2a534-116">Disadvantages</span></span></td>
<td><ul>
<li><span data-ttu-id="2a534-117">Обработка более сложная.</span><span class="sxs-lookup"><span data-stu-id="2a534-117">Processing is more complex.</span></span></li>
<li><span data-ttu-id="2a534-118">API C/C++ требует больше шагов, чем COM-интерфейс для выполнения тех же действий.</span><span class="sxs-lookup"><span data-stu-id="2a534-118">The C/C++ API requires more steps than the COM interface to perform the same actions.</span></span></li>
<li><span data-ttu-id="2a534-119">Настройка запроса занимает больше кода.</span><span class="sxs-lookup"><span data-stu-id="2a534-119">Setting up a request takes more code.</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2a534-120">COM-интерфейс не предоставляет доступ к полному набору функций WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="2a534-120">The COM interface does not provide access to the full feature set of WinHTTP.</span></span></li>
<li><span data-ttu-id="2a534-121">Трудно управлять двоичными типами данных на некоторых языках сценариев, таких как VBScript и JScript.</span><span class="sxs-lookup"><span data-stu-id="2a534-121">It is difficult to handle binary data types in some scripting languages, such as VBScript and JScript.</span></span></li>
<li><span data-ttu-id="2a534-122">Интерфейс COM не поддерживает автопрокси.</span><span class="sxs-lookup"><span data-stu-id="2a534-122">The COM interface does not support AutoProxy.</span></span></li>
<li><span data-ttu-id="2a534-123">Приложения должны использовать модель COM APARTMENT_THREADED.</span><span class="sxs-lookup"><span data-stu-id="2a534-123">Applications must use the COM APARTMENT_THREADED model.</span></span></li>
<li><span data-ttu-id="2a534-124">Перед обработкой ответа необходимо сначала получить и буферизовать весь ответ.</span><span class="sxs-lookup"><span data-stu-id="2a534-124">Before a response can begin being processed, the entire response must first be received and buffered.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



