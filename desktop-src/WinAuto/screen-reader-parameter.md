---
title: Параметр средства чтения с экрана
description: Параметр средства чтения с экрана указывает, должно ли приложение предоставлять текстовую информацию в ситуациях, когда оно в противном случае будет представлять информацию графически.
ms.assetid: ac79c389-511c-4403-a8d5-75b2eba2b39f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c237f3d945b9782884ffc655cf87a203159a16
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070276"
---
# <a name="screen-reader-parameter"></a><span data-ttu-id="e180e-103">Параметр средства чтения с экрана</span><span class="sxs-lookup"><span data-stu-id="e180e-103">Screen reader parameter</span></span>

<span data-ttu-id="e180e-104">Параметр средства чтения с экрана указывает, должно ли приложение предоставлять текстовую информацию в ситуациях, когда оно в противном случае будет представлять информацию графически.</span><span class="sxs-lookup"><span data-stu-id="e180e-104">The screen reader parameter indicates whether an application should provide textual information in situations where it would otherwise present the information graphically.</span></span>

<span data-ttu-id="e180e-105">Этот параметр обычно задается специальными средствами, такими как средства чтения с экрана.</span><span class="sxs-lookup"><span data-stu-id="e180e-105">This parameter is typically set by accessibility aids such as screen readers.</span></span> <span data-ttu-id="e180e-106">Приложения используют флаги **SPI \_ Жетскринреадер** и **SPI \_ сетскринреадер** с функцией [**системпараметерсинфо**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) для получения и задания параметра средства чтения с экрана.</span><span class="sxs-lookup"><span data-stu-id="e180e-106">Applications use the **SPI\_GETSCREENREADER** and **SPI\_SETSCREENREADER** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to get and set the screen reader parameter.</span></span>

> [!Note]  
> <span data-ttu-id="e180e-107">Экранный диктор, средство чтения с экрана, включенное в Windows, не устанавливает флаги **SPI \_ Сетскринреадер** или **SPI \_ жетскринреадер** .</span><span class="sxs-lookup"><span data-stu-id="e180e-107">Narrator, the screen reader that is included with Windows, does not set the **SPI\_SETSCREENREADER** or **SPI\_GETSCREENREADER** flags.</span></span>

 

 

 