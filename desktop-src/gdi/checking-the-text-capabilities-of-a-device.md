---
description: С помощью функций Енумфонтс и EnumFontFamilies можно перечислить шрифты, доступные в контексте устройства памяти, совместимого с принтерами.
ms.assetid: d68de203-2d5f-4a28-bb57-1dda9fcb078a
title: Проверка возможностей текста устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fd1a4ddc0c678c775c6c068216e60ead234d757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997418"
---
# <a name="checking-the-text-capabilities-of-a-device"></a><span data-ttu-id="e5172-103">Проверка возможностей текста устройства</span><span class="sxs-lookup"><span data-stu-id="e5172-103">Checking the Text Capabilities of a Device</span></span>

<span data-ttu-id="e5172-104">С помощью функций [енумфонтс](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) и [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) можно перечислить шрифты, доступные в контексте устройства памяти, совместимого с принтерами.</span><span class="sxs-lookup"><span data-stu-id="e5172-104">You can use the [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) and [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) functions to enumerate the fonts that are available in a printer-compatible memory device context.</span></span> <span data-ttu-id="e5172-105">Можно также использовать функцию [жетдевицекапс](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) для получения сведений о возможностях текста устройства.</span><span class="sxs-lookup"><span data-stu-id="e5172-105">You can also use the [GetDeviceCaps](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function to retrieve information about the text capabilities of a device.</span></span> <span data-ttu-id="e5172-106">Вызывая функцию [**жетдевицекапс**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) с индексом нумфонтс, можно определить минимальное число шрифтов, поддерживаемых принтером.</span><span class="sxs-lookup"><span data-stu-id="e5172-106">By calling the [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) function with the NUMFONTS index, you can determine the minimum number of fonts supported by a printer.</span></span> <span data-ttu-id="e5172-107">(Отдельный принтер может поддерживать больше шрифтов, чем указано в возвращаемом значении из **жетдевицекапс** с индексом нумфонтс.) С помощью индекса ТЕКСТКАПС можно вычислить многие текстовые возможности указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="e5172-107">(An individual printer may support more fonts than specified in the return value from **GetDeviceCaps** with the NUMFONTS index.) By using the TEXTCAPS index, you can identify many of the text capabilities of the specified device.</span></span>

 

 
