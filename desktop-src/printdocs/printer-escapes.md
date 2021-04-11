---
description: Функции переключения принтера, предоставляемые 16-разрядной системой Windows, имеют доступ к специальным функциям устройства.
ms.assetid: 4bdd1d47-8cf4-4088-aec8-88193e71a828
title: Escape-последовательности принтера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59463c4201e97c5ac1ec689a772581fab28314b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265110"
---
# <a name="printer-escapes"></a><span data-ttu-id="b58d7-103">Escape-последовательности принтера</span><span class="sxs-lookup"><span data-stu-id="b58d7-103">Printer Escapes</span></span>

<span data-ttu-id="b58d7-104">Функции переключения принтера, предоставляемые 16-разрядной системой Windows, имеют доступ к специальным функциям устройства.</span><span class="sxs-lookup"><span data-stu-id="b58d7-104">The printer escapes provided by 16-bit Windows allowed access special device features.</span></span> <span data-ttu-id="b58d7-105">Большинство этих escape-версий устарели, но для упрощения переноса 16-разрядных приложений на основе Windows предоставляется несколько средств.</span><span class="sxs-lookup"><span data-stu-id="b58d7-105">Most of these escapes are obsolete, but a few are provided to simplify the porting of 16-bit Windows-based applications.</span></span> <span data-ttu-id="b58d7-106">GDI поддерживает полный набор функций Path, которые могут использоваться приложениями вместо escape для рисования контуров на любом устройстве.</span><span class="sxs-lookup"><span data-stu-id="b58d7-106">GDI supports a complete set of path functions that applications can use instead of the escapes to draw paths on any device.</span></span> <span data-ttu-id="b58d7-107">Список функций, которые заменяют некоторые escape-последовательности, см. в разделе [**escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) -функция.</span><span class="sxs-lookup"><span data-stu-id="b58d7-107">For a list of functions that replace some of the escapes, see the [**Escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) function.</span></span>

<span data-ttu-id="b58d7-108">Из **куересксуппортных** escape-символов принтера 64 можно использовать только и **Пересылка** .</span><span class="sxs-lookup"><span data-stu-id="b58d7-108">Of the 64 original printer escapes, only **QUERYESCSUPPORT** and **PASSTHROUGH** can be used.</span></span>

<span data-ttu-id="b58d7-109">Также имеется Расширенная Escape-функция с именем [**екстескапе**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="b58d7-109">There is also an extended escape function called [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span> <span data-ttu-id="b58d7-110">Эта функция позволяет приложениям получать доступ к возможностям определенного устройства, которые не доступны напрямую через GDI.</span><span class="sxs-lookup"><span data-stu-id="b58d7-110">This function allows applications to access capabilities of a particular device not directly available through GDI.</span></span>

 

 



