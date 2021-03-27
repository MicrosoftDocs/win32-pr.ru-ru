---
description: Функция управления цветом изображений (ICM) (Майкрософт) гарантирует, что цвет изображения, графического объекта или текстового объекта будет отображаться как можно ближе к исходному намерению на любом устройстве, несмотря на различия в технологиях создания образов и цветовых возможностях устройств.
ms.assetid: 7b3cb9a4-ffd2-4867-85bd-0e663fdde6e3
title: ICM-Enabled функции точечного рисунка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b89dac569aafad1ef94b066bc97f588bac62c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898406"
---
# <a name="icm-enabled-bitmap-functions"></a>ICM-Enabled функции точечного рисунка

Функция управления цветом изображений (ICM) (Майкрософт) гарантирует, что цвет изображения, графического объекта или текстового объекта будет отображаться как можно ближе к исходному намерению на любом устройстве, несмотря на различия в технологиях создания образов и цветовых возможностях устройств. Независимо от того, сканируете изображение или какой-либо другой графический сканер, загружает его через Интернет, просматриваете или редактируете или печатаете на бумаге, на пленке или другом носителе, ICM 2,0 помогает постоянно и точно соответствовать цветам. Дополнительные сведения о ICM см. в разделе [Цветовая система Windows](/previous-versions//dd372446(v=vs.85)).

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

 

 
