---
title: Изменение текущей должности
description: Изменение текущей должности
ms.assetid: f8c4b9b5-c5fb-4292-8418-41650dcd65c0
keywords:
- Сообщение команды MCI_SEEK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235dc2639d7d9fc01f94aff700ae9e0ebf1dcbe2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412972"
---
# <a name="changing-the-current-position"></a><span data-ttu-id="cb950-104">Изменение текущей должности</span><span class="sxs-lookup"><span data-stu-id="cb950-104">Changing the Current Position</span></span>

<span data-ttu-id="cb950-105">Чтобы изменить текущую положение в элементе устройства, используйте команду [**MCI \_ Seek**](mci-seek.md) , а также установите флаг MCI, \_ а также структуру [**\_ \_ пармс для MCI**](mci-seek-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="cb950-105">To change the current position in a device element, use the [**MCI\_SEEK**](mci-seek.md) command message along with the MCI\_TO flag and the [**MCI\_SEEK\_PARMS**](mci-seek-parms.md) structure.</span></span> <span data-ttu-id="cb950-106">Если вы используете элемент **двто** , чтобы указать положение поиска с помощью MCI \_ Seek, необходимо запросить формат времени и задать его при необходимости.</span><span class="sxs-lookup"><span data-stu-id="cb950-106">If you use the **dwTo** member to specify a seek position with MCI\_SEEK, you should query the time format and set it, if necessary.</span></span>

<span data-ttu-id="cb950-107">Помимо указания позиции с элементом **двто** , можно указать \_ \_ \_ НАЧАЛЬное начало или функцию MCI найти \_ \_ \_ Флаги для параметра *dwParam1* функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) , чтобы определить начальную и конечную позиции элемента Device.</span><span class="sxs-lookup"><span data-stu-id="cb950-107">In addition to specifying a position with the **dwTo** member, you can specify the MCI\_SEEK\_TO\_START or MCI\_SEEK\_TO\_END flags for the *dwParam1* parameter of the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function to find the starting and ending positions of the device element.</span></span> <span data-ttu-id="cb950-108">Если используется один из этих флагов, не указывайте параметр MCI \_ для флага.</span><span class="sxs-lookup"><span data-stu-id="cb950-108">If you use one of these flags, don't specify the MCI\_TO flag.</span></span>

 

 