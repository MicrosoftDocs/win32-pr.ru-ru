---
description: 'Все примеры в документации по пакету SDK для шифрования предполагают наличие следующих \# директив компилятора: include и \# define.'
ms.assetid: 98f85e7d-e557-4dde-b510-891b37daec87
title: '#включает и #defines'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9834fd8103b9fd28a01e416bd1df8b03fb7ad680
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105684759"
---
# <a name="includes-and-defines"></a>\#включает и \# определяет

Все примеры в документации по пакету SDK для шифрования предполагают наличие следующих директив компилятора **\# : include** и **\# define** .


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
```



Кроме того, константа **\_ Win32 \_ WinNT** должна быть определена соответствующим образом. Дополнительные сведения о **\_ Win32 \_ WinNT** см. [в разделе Использование заголовков Windows](../winprog/using-the-windows-headers.md).

 

 
