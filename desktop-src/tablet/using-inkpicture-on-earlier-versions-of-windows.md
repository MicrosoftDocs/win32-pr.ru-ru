---
description: Элемент управления InkPicture можно использовать для визуализации рукописного ввода на Microsoft Windows 2000, Windows Server 2003 и в выпусках Windows XP, отличных от планшетных ПК. Однако нельзя использовать элемент управления для ввода рукописного ввода в этих операционных системах.
ms.assetid: e5d00b0f-0a4f-4ea2-ae63-dfb6bc8c2caf
title: Использование функции InkPicture в более ранних версиях Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbd2bf8545524787c9e37f70c43d954ab440910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710983"
---
# <a name="using-inkpicture-on-earlier-versions-of-windows"></a><span data-ttu-id="59e67-104">Использование функции InkPicture в более ранних версиях Windows</span><span class="sxs-lookup"><span data-stu-id="59e67-104">Using InkPicture on Earlier Versions of Windows</span></span>

<span data-ttu-id="59e67-105">[Элемент управления InkPicture](inkpicture-control.md) можно использовать для визуализации рукописного ввода на Microsoft Windows 2000, windows Server 2003 и в выпусках Windows XP, отличных от планшетных ПК.</span><span class="sxs-lookup"><span data-stu-id="59e67-105">You can use the [InkPicture Control](inkpicture-control.md) to render ink on Microsoft Windows 2000, Windows Server 2003, and non-Tablet PC editions of Windows XP.</span></span> <span data-ttu-id="59e67-106">Однако нельзя использовать элемент управления для ввода рукописного ввода в этих операционных системах.</span><span class="sxs-lookup"><span data-stu-id="59e67-106">However, you cannot use the control to input ink on these operating systems.</span></span>

<span data-ttu-id="59e67-107">Свойство [**инкенаблед**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled) элемента управления имеет значение **false**, и попытка изменить свойство не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="59e67-107">The control's [**InkEnabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled) property is set to **FALSE**, and attempting to change the property has no effect.</span></span> <span data-ttu-id="59e67-108">Можно назначать значения другим свойствам и программно манипулировать рукописным вводом, но нельзя использовать элемент управления для получения рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="59e67-108">You can assign values to other properties and programmatically manipulate ink, but you cannot use the control to collect ink.</span></span>

 

 



