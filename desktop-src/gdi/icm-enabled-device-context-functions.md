---
description: Функция управления цветом изображений (ICM) (Майкрософт) гарантирует, что цвет изображения, графика или текстового объекта будет отображаться как можно ближе к исходному намерению на любом устройстве, несмотря на различия в технологиях создания образов и цветовых возможностях устройств.
ms.assetid: eced18cf-be5a-4c61-b0e5-36d607daa6ff
title: ICM-Enabled функции контекста устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a0b49e62d0b4d05e0690d2aee0d3c5f0f530cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984952"
---
# <a name="icm-enabled-device-context-functions"></a><span data-ttu-id="28742-103">ICM-Enabled функции контекста устройства</span><span class="sxs-lookup"><span data-stu-id="28742-103">ICM-Enabled Device Context Functions</span></span>

<span data-ttu-id="28742-104">Функция управления цветом изображений (ICM) (Майкрософт) гарантирует, что цвет изображения, графика или текстового объекта будет отображаться как можно ближе к исходному намерению на любом устройстве, несмотря на различия в технологиях создания образов и цветовых возможностях устройств.</span><span class="sxs-lookup"><span data-stu-id="28742-104">Microsoft Image Color Management (ICM) ensures that a color image, graphic, or text object is rendered as closely as possible to its original intent on any device, despite differences in imaging technologies and color capabilities between devices.</span></span> <span data-ttu-id="28742-105">(Дополнительные сведения см. в разделе [Цветовая система Windows](/previous-versions//dd372446(v=vs.85)).)</span><span class="sxs-lookup"><span data-stu-id="28742-105">(For more information, see [Windows Color System](/previous-versions//dd372446(v=vs.85)).)</span></span>

<span data-ttu-id="28742-106">В интерфейсе графических устройств (GDI) есть различные функции, которые используют данные цвета или работают с ними.</span><span class="sxs-lookup"><span data-stu-id="28742-106">There are various functions in the graphics device interface (GDI) that use or operate on color data.</span></span> <span data-ttu-id="28742-107">Следующие функции контекста устройства включены для использования с ICM:</span><span class="sxs-lookup"><span data-stu-id="28742-107">The following device context functions are enabled for use with ICM:</span></span>

-   [<span data-ttu-id="28742-108">**креатекомпатибледк**</span><span class="sxs-lookup"><span data-stu-id="28742-108">**CreateCompatibleDC**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)
-   [<span data-ttu-id="28742-109">**креатедк**</span><span class="sxs-lookup"><span data-stu-id="28742-109">**CreateDC**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdca)
-   [<span data-ttu-id="28742-110">**жетдкбрушколор**</span><span class="sxs-lookup"><span data-stu-id="28742-110">**GetDCBrushColor**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)
-   [<span data-ttu-id="28742-111">**жетдкпенколор**</span><span class="sxs-lookup"><span data-stu-id="28742-111">**GetDCPenColor**</span></span>](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)
-   [<span data-ttu-id="28742-112">**ресетдк**</span><span class="sxs-lookup"><span data-stu-id="28742-112">**ResetDC**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)
-   [<span data-ttu-id="28742-113">**Функцию**</span><span class="sxs-lookup"><span data-stu-id="28742-113">**SelectObject**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)
-   [<span data-ttu-id="28742-114">**сетдкбрушколор**</span><span class="sxs-lookup"><span data-stu-id="28742-114">**SetDCBrushColor**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)
-   [<span data-ttu-id="28742-115">**сетдкпенколор**</span><span class="sxs-lookup"><span data-stu-id="28742-115">**SetDCPenColor**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)

 

 
