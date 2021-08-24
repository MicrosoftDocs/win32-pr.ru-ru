---
description: Функция управления цветом изображений (ICM) (Майкрософт) гарантирует, что цвет изображения, графического объекта или текстового объекта будет отображаться как можно ближе к исходному намерению на любом устройстве, несмотря на различия в технологиях создания образов и цветовых возможностях устройств.
ms.assetid: 7b3cb9a4-ffd2-4867-85bd-0e663fdde6e3
title: ICM-Enabled функции точечного рисунка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38341851eb9ba2aed25cc93afbf7b869909430a30ecb626bf3a452883fdea97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831974"
---
# <a name="icm-enabled-bitmap-functions"></a>ICM-Enabled функции точечного рисунка

Функция управления цветом изображений (ICM) (Майкрософт) гарантирует, что цвет изображения, графического объекта или текстового объекта будет отображаться как можно ближе к исходному намерению на любом устройстве, несмотря на различия в технологиях создания образов и цветовых возможностях устройств. Независимо от того, сканируете изображение или какой-либо другой графический сканер, загружает его через Интернет, просматриваете или редактируете или печатаете на бумаге, на пленке или другом носителе, ICM 2,0 помогает постоянно и точно соответствовать цветам. дополнительные сведения о ICM см. в разделе [Windows цветовая система](/previous-versions//dd372446(v=vs.85)).

В интерфейсе графических устройств (GDI) есть различные функции, которые используют данные цвета или работают с ними. Следующие функции точечного рисунка включены для использования с ICM:

-   [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)
-   [**креатедибитмап**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)
-   [**креатедибсектион**](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)
-   [**маскблт**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)
-   [**сетдибколортабле**](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)
-   [**стретчблт**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)
-   [**сетдибитс**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)
-   [**сетдибитстодевице**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)
-   [**стретчдибитс**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)

 

 
