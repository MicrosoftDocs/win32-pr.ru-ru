---
title: Идентификаторы формата
description: Значения набора свойств хранятся в разделе, помеченном уникальным FMTID.
ms.assetid: 3ffb6c5e-72ce-4769-847a-72db6f145d61
keywords:
- Идентификаторы формата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0202cd1287c3b4fef6e9e2b56e272541a03425b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329544"
---
# <a name="format-identifiers"></a><span data-ttu-id="26095-104">Идентификаторы формата</span><span class="sxs-lookup"><span data-stu-id="26095-104">Format Identifiers</span></span>

<span data-ttu-id="26095-105">Значения набора свойств хранятся в разделе, помеченном уникальным FMTID.</span><span class="sxs-lookup"><span data-stu-id="26095-105">Property set values are stored in a section tagged with a unique FMTID.</span></span> <span data-ttu-id="26095-106">Например, FMTID для набора свойств "Сводная информация COM" — **F29F85E0-4FF9-1068-AB91-08002B27B3D9**.</span><span class="sxs-lookup"><span data-stu-id="26095-106">For example, the FMTID for the COM Summary Information property set is **F29F85E0-4FF9-1068-AB91-08002B27B3D9**.</span></span>

<span data-ttu-id="26095-107">Чтобы определить FMTID для набора свойств сводных данных, используйте макрос **define \_ GUID** в включаемом файле для кода, который управляет набором свойств.</span><span class="sxs-lookup"><span data-stu-id="26095-107">To define a FMTID for the Summary Information property set, use the **DEFINE\_GUID** macro in an include file for the code that manipulates the property set.</span></span>


```C++
DEFINE_GUID(FMTID_SummaryInformation, 0xF29F85E0, 0x4FF9, 0x1068, 
0xAB, 0x91, 0x08, 0x00, 0x2B, 0x27, 0xB3, 0xD9);
```



<span data-ttu-id="26095-108">Любой код, который требует FMTID для набора свойств сводки, может получить доступ к нему через переменную *FMTID \_ SummaryInformation* .</span><span class="sxs-lookup"><span data-stu-id="26095-108">Any code that requires the FMTID for the Summary Information property set, can access it through the *FMTID\_SummaryInformation* variable.</span></span>

<span data-ttu-id="26095-109">При хранении наборов свойств в экземплярах [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) преобразуйте FMTID в строковое имя для объекта хранилища.</span><span class="sxs-lookup"><span data-stu-id="26095-109">When storing property sets in [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) instances, convert the FMTID to a string name for the storage object.</span></span>

 

 




