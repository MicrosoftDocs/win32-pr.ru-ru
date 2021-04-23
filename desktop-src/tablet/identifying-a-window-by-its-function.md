---
description: Описание идентификации окна по его функции для планшетных ПК.
ms.assetid: 513e0c9d-4c9e-4e7c-8314-bd7603489e89
title: Определение окна по его функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497f660d6690bd4dc37c252f82f2408da3e3655d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711127"
---
# <a name="identifying-a-window-by-its-function"></a><span data-ttu-id="2cac6-103">Определение окна по его функции</span><span class="sxs-lookup"><span data-stu-id="2cac6-103">Identifying a Window by Its Function</span></span>

<span data-ttu-id="2cac6-104">Укажите каждый тип окна, назначив ему уникальный класс окна.</span><span class="sxs-lookup"><span data-stu-id="2cac6-104">Identify each type of window by assigning it a unique window class.</span></span> <span data-ttu-id="2cac6-105">Избегайте использования одного класса окон, используемого для широкого спектра функций.</span><span class="sxs-lookup"><span data-stu-id="2cac6-105">Avoid having a single window class that is used for a wide variety of functions.</span></span>

<span data-ttu-id="2cac6-106">Средства специальных возможностей должны иметь такую идентификацию, чтобы работать с различными окнами в одном приложении.</span><span class="sxs-lookup"><span data-stu-id="2cac6-106">Accessibility aids must have this identification in order to handle different windows within the same application.</span></span> <span data-ttu-id="2cac6-107">Для обработки этих окон могут существовать отдельные инструкции, такие как объявление конкретных областей при изменении содержимого.</span><span class="sxs-lookup"><span data-stu-id="2cac6-107">There may be separate instructions for handling these windows, such as announcing specific areas when the content changes.</span></span>

<span data-ttu-id="2cac6-108">Если нельзя использовать отдельные классы окон, можно предоставить различия в Microsoft <entity type="reg"/> Active Accessibility <entity type="reg"/> или, если это необходимо, в сообщении частного окна, которое вы задокументированы на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="2cac6-108">If you cannot use separate window classes, you can expose the differences through Microsoft<entity type="reg"/> Active Accessibility<entity type="reg"/>, or if necessary, by a private window message that you document on your website.</span></span>

<span data-ttu-id="2cac6-109">Дополнительные сведения о предоставлении классов окон с помощью Active Accessibility см. в разделе [Специальные возможности](/windows/desktop/accessibility) .</span><span class="sxs-lookup"><span data-stu-id="2cac6-109">For more information about exposing window classes by using Active Accessibility, see the [Accessibility](/windows/desktop/accessibility) section.</span></span>

 

 
