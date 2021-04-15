---
description: Для каждого события могут сопоставлены связанные с событиями данные.
ms.assetid: fa2f9e71-44c3-4569-bde4-24112a756664
title: Данные о событиях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 459377d9cdf78fba46133b494723008df025caad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662610"
---
# <a name="event-data"></a><span data-ttu-id="2d83b-103">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="2d83b-103">Event Data</span></span>

<span data-ttu-id="2d83b-104">Для каждого события могут сопоставлены связанные с событиями данные.</span><span class="sxs-lookup"><span data-stu-id="2d83b-104">Each event can have event-specific data associated with it.</span></span> <span data-ttu-id="2d83b-105">Просмотр событий не интерпретирует эти данные; Дополнительные данные отображаются только в комбинированном шестнадцатеричном и текстовом формате.</span><span class="sxs-lookup"><span data-stu-id="2d83b-105">The Event Viewer does not interpret this data; it displays extra data only in a combined hexadecimal and text format.</span></span> <span data-ttu-id="2d83b-106">Максимальное ограничение размера события в четном журнале — 0x3FFFF байт.</span><span class="sxs-lookup"><span data-stu-id="2d83b-106">The maximum limit on the size of an event in the even log is 0x3FFFF bytes.</span></span> <span data-ttu-id="2d83b-107">Таким образом, данные событий следует использовать экономно, в том числе только в том случае, если вы уверены, что он будет полезен для отладки проблемы.</span><span class="sxs-lookup"><span data-stu-id="2d83b-107">Therefore, use event-specific data sparingly, including it only if you are sure it will be useful to someone debugging a problem.</span></span> <span data-ttu-id="2d83b-108">Например, многие события, связанные с сетью, включают в себя блоки управления сетью (NCB) как данные, относящиеся к конкретному событию.</span><span class="sxs-lookup"><span data-stu-id="2d83b-108">For example, many network-related events include network control blocks (NCB) as event-specific data.</span></span>

<span data-ttu-id="2d83b-109">При использовании данных, относящихся к конкретному событию, в последней части строки описания должно быть указано Примечание о сведениях, предоставляемых в виде данных, относящихся к конкретному событию.</span><span class="sxs-lookup"><span data-stu-id="2d83b-109">When you use event-specific data, the last part of its description string should provide a note about the information provided as event-specific data.</span></span> <span data-ttu-id="2d83b-110">Например, сетевое программное обеспечение может предоставить следующее примечание: "(NCB — это данные события)". В качестве соглашения используйте круглые скобки вокруг таких примечаний, как показано в этом примере.</span><span class="sxs-lookup"><span data-stu-id="2d83b-110">For example, the network software could provide a note such as: "(The NCB is the event data.)" As a convention, use parentheses around such remarks, as indicated in this example.</span></span>

<span data-ttu-id="2d83b-111">Можно также использовать данные событий для хранения информации, которую приложение может обрабатывать независимо от Просмотр событий.</span><span class="sxs-lookup"><span data-stu-id="2d83b-111">You can also use event-specific data to store information the application can process independently of the Event Viewer.</span></span> <span data-ttu-id="2d83b-112">Например, можно написать средство просмотра, предназначенное для событий, или написать программу, которая просматривает журнал и создает отчет, который включает сведения из данных, относящихся к конкретному событию.</span><span class="sxs-lookup"><span data-stu-id="2d83b-112">For example, you could write a viewer specifically for your events, or write a program that scans the log and creates a report that includes information from the event-specific data.</span></span>

 

 



