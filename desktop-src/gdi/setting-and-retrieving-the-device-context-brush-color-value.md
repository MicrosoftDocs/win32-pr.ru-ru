---
description: В следующем примере показано, как приложение может извлекать текущий цвет кисти контроллера домена с помощью функций Сетдкбрушколор и Жетдкбрушколор.
ms.assetid: a1ef6c25-0d00-4175-8679-001ba165bd6d
title: Установка и получение значения цвета кисти контекста устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c684bfd50fd92959e9b8f7eac5baf96c62fd0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997662"
---
# <a name="setting-and-retrieving-the-device-context-brush-color-value"></a><span data-ttu-id="78a6c-103">Установка и получение значения цвета кисти контекста устройства</span><span class="sxs-lookup"><span data-stu-id="78a6c-103">Setting and Retrieving the Device Context Brush Color Value</span></span>

<span data-ttu-id="78a6c-104">В следующем примере показано, как приложение может извлекать текущий цвет кисти контроллера домена с помощью функций [**сетдкбрушколор**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor) и [**жетдкбрушколор**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) .</span><span class="sxs-lookup"><span data-stu-id="78a6c-104">The following example shows how an application can retrieve the current DC brush color by using the [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor) and the [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) functions.</span></span>


```C++
SelectObject(hdc,GetStockObject(DC_BRUSH));
SetDCBrushColor(hdc, RGB(00,0xff;00);
PatBlt(0,0,200,200,PATCOPY)
SetDCBrushColor(hdc,RGB(00,00,0xff);
PatBlt(0,0,200,200,PATCOPY);
```



 

 



