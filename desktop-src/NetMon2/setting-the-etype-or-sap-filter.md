---
description: Установка части ETYPE или SAP фильтра записи является первым шагом в процессе создания фильтра записи.
ms.assetid: 0a22f74b-5bb1-43df-a70a-9f30195177ea
title: Настройка ETYPE или SAP Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee117e992968265be5a973f3f4017832ee6ca0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991199"
---
# <a name="setting-the-etype-or-sap-filter"></a><span data-ttu-id="e4fd1-103">Настройка ETYPE или SAP Filter</span><span class="sxs-lookup"><span data-stu-id="e4fd1-103">Setting the Etype or SAP Filter</span></span>

<span data-ttu-id="e4fd1-104">Установка части ETYPE или SAP фильтра записи является первым шагом в процессе создания фильтра записи.</span><span class="sxs-lookup"><span data-stu-id="e4fd1-104">Setting the Etype or SAP portion of the capture filter is the first step in the capture filter creation process.</span></span>

<span data-ttu-id="e4fd1-105">В следующем примере фильтр записи задается только для получения трафика IPX.</span><span class="sxs-lookup"><span data-stu-id="e4fd1-105">In the following example, the capture filter is set to only retrieve IPX traffic:</span></span>


```C++
BYTE Sap[]   = { 0x10, 0xE0 };
WORD Etype[] = { 0x8137 }; 

rc = SetNPPEtypeSapFilter(m_hBlob, 
     2,      //  nSaps,
     1,      //  nEtypes,
     &Sap,   //  LPBYTE lpSapTable,
     &Etype, //  LPWORD lpEtypeTable,
     0,      //  DWORD  FilterFlags,
     NULL
);
```



<span data-ttu-id="e4fd1-106">Значения SAP и ETYPE обычно доступны в документах RFC.</span><span class="sxs-lookup"><span data-stu-id="e4fd1-106">SAP and Etype values are usually available in RFCs.</span></span> <span data-ttu-id="e4fd1-107">Значения SAP и ETYPE могут находиться в массиве.</span><span class="sxs-lookup"><span data-stu-id="e4fd1-107">Both SAP and Etype values can be in an array.</span></span>

 

 



