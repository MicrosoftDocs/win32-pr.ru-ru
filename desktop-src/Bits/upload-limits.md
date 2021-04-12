---
title: Пределы передачи
description: Чтобы ограничить размер отправки, задайте свойство расширения IIS Битсмаксимумуплоадсизе.
ms.assetid: 01ad2f32-18be-43a5-a07f-e6f28f7a471b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647aeefe82cf9c3ab035bc3e233c4157f471110b
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104487296"
---
# <a name="upload-limits"></a><span data-ttu-id="28b34-103">Пределы передачи</span><span class="sxs-lookup"><span data-stu-id="28b34-103">Upload Limits</span></span>

<span data-ttu-id="28b34-104">Чтобы ограничить размер отправки, задайте свойство расширения IIS [**битсмаксимумуплоадсизе**](bits-iis-extension-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="28b34-104">To limit the size of uploads, set the [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) IIS extension property.</span></span> <span data-ttu-id="28b34-105">В IIS 7 может также потребоваться изменить атрибут **maxAllowedContentLength** .</span><span class="sxs-lookup"><span data-stu-id="28b34-105">In IIS 7, you may also have to modify the **maxAllowedContentLength** attribute.</span></span> <span data-ttu-id="28b34-106">По умолчанию предел загрузки IIS 7 составляет 30 000 000 байт.</span><span class="sxs-lookup"><span data-stu-id="28b34-106">By default, the IIS 7 upload limit is 30 million bytes.</span></span> <span data-ttu-id="28b34-107">Дополнительные сведения и сведения об изменении параметров IIS по умолчанию см. в разделе [KB942074](https://support.microsoft.com//kb/942074).</span><span class="sxs-lookup"><span data-stu-id="28b34-107">For details and information on changing the IIS default, see [KB942074](https://support.microsoft.com//kb/942074).</span></span>

 

 




