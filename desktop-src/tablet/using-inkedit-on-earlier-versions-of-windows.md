---
description: Из-за отсутствия распознавателей в выпусках Microsoft Windows XP, отличных от планшетных ПК, нельзя использовать InkEdit для визуализации рукописного ввода в Windows 2000, Windows Server 2003 и в выпусках Windows XP, отличных от планшетных ПК, и нельзя использовать этот элемент управления для ввода рукописного ввода в этих операционных системах.
ms.assetid: eb80ff91-5c09-43d1-afd4-6391097000c1
title: Использование InkEdit в более ранних версиях Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08343b3d379a3f45985b1f586254e7a370998f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710984"
---
# <a name="using-inkedit-on-earlier-versions-of-windows"></a><span data-ttu-id="f0817-103">Использование InkEdit в более ранних версиях Windows</span><span class="sxs-lookup"><span data-stu-id="f0817-103">Using InkEdit on Earlier Versions of Windows</span></span>

<span data-ttu-id="f0817-104">Из-за отсутствия распознавателей в выпусках Microsoft Windows XP, отличных от планшетных ПК, нельзя использовать [InkEdit](inkedit-control.md) для визуализации рукописного ввода в Windows 2000, windows Server 2003 и в выпусках Windows XP, отличных от планшетных ПК, и нельзя использовать этот элемент управления для ввода рукописного ввода в этих операционных системах.</span><span class="sxs-lookup"><span data-stu-id="f0817-104">Because of the lack of recognizers on non-Tablet PC editions of Microsoft Windows XP, you cannot use [InkEdit](inkedit-control.md) to render ink on Windows 2000, Windows Server 2003, and non-Tablet PC editions of Windows XP, and you cannot use the control to input ink on these operating systems.</span></span>

<span data-ttu-id="f0817-105">Свойство [**инкмоде**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) элемента управления имеет значение **disabled** (**Настройка Internet Explorer \_ отключено** для C++), и попытка изменить свойство не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="f0817-105">The control's [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) property is set to **Disabled** (**IEM\_Disabled** for C++), and attempting to change the property has no effect.</span></span> <span data-ttu-id="f0817-106">Можно назначать значения другим свойствам, копировать и вставлять рукописные данные в другие приложения, но нельзя использовать этот элемент управления для приема жестов или получения рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="f0817-106">You can assign values to other properties and copy and paste ink to other applications, but you cannot use the control to accept gestures or collect ink.</span></span>

 

 



