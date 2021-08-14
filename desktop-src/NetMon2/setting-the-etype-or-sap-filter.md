---
description: Установка части ETYPE или SAP фильтра записи является первым шагом в процессе создания фильтра записи.
ms.assetid: 0a22f74b-5bb1-43df-a70a-9f30195177ea
title: Настройка ETYPE или SAP Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abac637594debf03ca9f82c79382ababc4c696d79d5351b2d0be0a3e5b4ffa8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363169"
---
# <a name="setting-the-etype-or-sap-filter"></a>Настройка ETYPE или SAP Filter

Установка части ETYPE или SAP фильтра записи является первым шагом в процессе создания фильтра записи.

В следующем примере фильтр записи задается только для получения трафика IPX.


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



Значения SAP и ETYPE обычно доступны в документах RFC. Значения SAP и ETYPE могут находиться в массиве.

 

 



