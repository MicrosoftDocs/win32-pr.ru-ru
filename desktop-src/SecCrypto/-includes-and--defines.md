---
description: 'Все примеры в документации по пакету SDK для шифрования предполагают наличие следующих \# директив компилятора: include и \# define.'
ms.assetid: 98f85e7d-e557-4dde-b510-891b37daec87
title: '#включает и #defines'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dbab2a3c33b510df99c9d2e0fa292af53c96fcc471dfe8180d9d4be06b3a5b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774279"
---
# <a name="includes-and-defines"></a>\#включает и \# определяет

Все примеры в документации по пакету SDK для шифрования предполагают наличие следующих директив компилятора **\# : include** и **\# define** .


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
```



Кроме того, константа **\_ Win32 \_ WinNT** должна быть определена соответствующим образом. дополнительные сведения о **\_ WIN32 \_ WINNT** см. [в разделе использование Windows заголовков](../winprog/using-the-windows-headers.md).

 

 
