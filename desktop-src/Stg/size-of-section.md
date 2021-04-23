---
title: Размер раздела
description: Тип данных размер раздела указывает размер раздела в байтах.
ms.assetid: 6438fbce-42b9-4b16-a6b0-80c80246e546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b19df1c2f9a65f6952855a4ab325565c759af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258984"
---
# <a name="size-of-section"></a><span data-ttu-id="850bb-103">Размер раздела</span><span class="sxs-lookup"><span data-stu-id="850bb-103">Size of Section</span></span>

<span data-ttu-id="850bb-104">Тип данных размер раздела указывает размер раздела в байтах.</span><span class="sxs-lookup"><span data-stu-id="850bb-104">The section size data type indicates the size, in bytes, of the section.</span></span> <span data-ttu-id="850bb-105">Поскольку размер раздела составляет первые 4 байта, разделы можно копировать в виде массива байтов.</span><span class="sxs-lookup"><span data-stu-id="850bb-105">Because the section size is the first 4 bytes, sections can be copied as an array of bytes.</span></span> <span data-ttu-id="850bb-106">Размер раздела всегда должен быть кратен четырем.</span><span class="sxs-lookup"><span data-stu-id="850bb-106">The section size should always be a multiple of four.</span></span>

<span data-ttu-id="850bb-107">Например, пустой раздел, т. е. один из которых имеет нулевые свойства, будет иметь число байтов, равное восьми ( **DWORD** -числа байтов и **DWORD** счетчика свойств).</span><span class="sxs-lookup"><span data-stu-id="850bb-107">For example, an empty section, that is, one with zero properties in it, would have a byte count of eight (the **DWORD** byte count and the **DWORD** count of properties).</span></span> <span data-ttu-id="850bb-108">Сам раздел будет содержать 8 байт: **08 00 00 00 00 00 00 00**.</span><span class="sxs-lookup"><span data-stu-id="850bb-108">The section itself would contain the 8 bytes: **08 00 00 00 00 00 00 00**.</span></span>

 

 




