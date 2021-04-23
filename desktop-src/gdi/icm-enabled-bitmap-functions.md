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
# <a name="icm-enabled-bitmap-functions"></a><span data-ttu-id="2a3f0-103">ICM-Enabled функции точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="2a3f0-103">ICM-Enabled Bitmap Functions</span></span>

<span data-ttu-id="2a3f0-104">Функция управления цветом изображений (ICM) (Майкрософт) гарантирует, что цвет изображения, графического объекта или текстового объекта будет отображаться как можно ближе к исходному намерению на любом устройстве, несмотря на различия в технологиях создания образов и цветовых возможностях устройств.</span><span class="sxs-lookup"><span data-stu-id="2a3f0-104">Microsoft Image Color Management (ICM) ensures that a color image, graphic object, or text object is rendered as closely as possible to its original intent on any device, despite differences in imaging technologies and color capabilities between devices.</span></span> <span data-ttu-id="2a3f0-105">Независимо от того, сканируете изображение или какой-либо другой графический сканер, загружает его через Интернет, просматриваете или редактируете или печатаете на бумаге, на пленке или другом носителе, ICM 2,0 помогает постоянно и точно соответствовать цветам.</span><span class="sxs-lookup"><span data-stu-id="2a3f0-105">Whether you are scanning an image or other graphic on a color scanner, downloading it over the Internet, viewing or editing it onscreen, or printing it on paper, film, or other media, ICM 2.0 helps you keep colors consistent and accurate.</span></span> <span data-ttu-id="2a3f0-106">Дополнительные сведения о ICM см. в разделе [Цветовая система Windows](/previous-versions//dd372446(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2a3f0-106">For more information about ICM, see [Windows Color System](/previous-versions//dd372446(v=vs.85)).</span></span>

<span data-ttu-id="2a3f0-107">В интерфейсе графических устройств (GDI) есть различные функции, которые используют данные цвета или работают с ними.</span><span class="sxs-lookup"><span data-stu-id="2a3f0-107">There are various functions in the graphics device interface (GDI) that use or operate on color data.</span></span> <span data-ttu-id="2a3f0-108">Следующие функции точечного рисунка включены для использования с ICM:</span><span class="sxs-lookup"><span data-stu-id="2a3f0-108">The following bitmap functions are enabled for use with ICM:</span></span>

-   [<span data-ttu-id="2a3f0-109">**BitBlt**</span><span class="sxs-lookup"><span data-stu-id="2a3f0-109">**BitBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)
-   [<span data-ttu-id="2a3f0-110">**креатедибитмап**</span><span class="sxs-lookup"><span data-stu-id="2a3f0-110">**CreateDIBitmap**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)
-   [<span data-ttu-id="2a3f0-111">**креатедибсектион**</span><span class="sxs-lookup"><span data-stu-id="2a3f0-111">**CreateDIBSection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)
-   [<span data-ttu-id="2a3f0-112">**маскблт**</span><span class="sxs-lookup"><span data-stu-id="2a3f0-112">**MaskBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)
-   [<span data-ttu-id="2a3f0-113">**сетдибколортабле**</span><span class="sxs-lookup"><span data-stu-id="2a3f0-113">**SetDIBColorTable**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)
-   [<span data-ttu-id="2a3f0-114">**стретчблт**</span><span class="sxs-lookup"><span data-stu-id="2a3f0-114">**StretchBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)
-   [<span data-ttu-id="2a3f0-115">**сетдибитс**</span><span class="sxs-lookup"><span data-stu-id="2a3f0-115">**SetDIBits**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)
-   [<span data-ttu-id="2a3f0-116">**сетдибитстодевице**</span><span class="sxs-lookup"><span data-stu-id="2a3f0-116">**SetDIBitsToDevice**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)
-   [<span data-ttu-id="2a3f0-117">**стретчдибитс**</span><span class="sxs-lookup"><span data-stu-id="2a3f0-117">**StretchDIBits**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)

 

 
