---
description: Из-за того, что существуют статически связываемые DLL, следует избегать использования Microsoft Foundation Classes (Мфкс) для написания эксперта.
ms.assetid: 634852fd-d0e0-42a7-90af-e93cc0e4ac84
title: Использование Microsoft Foundation Classes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bec1b01260d3fd7d1e7058c9fff8aa3cc32390b3f2f6cc715c91563a871fbf20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362933"
---
# <a name="using-microsoft-foundation-classes"></a>Использование Microsoft Foundation Classes

Из-за того, что существуют статически связываемые DLL, следует избегать использования Microsoft Foundation Classes (Мфкс) для написания эксперта. Однако при использовании MFC Обеспечьте доступ к любому из ресурсов библиотеки DLL MFC, включив следующий код сразу после записи:

``` syntax
#ifdef _AFXDLL
      AFX_MANAGE_STATE(AfxGetStaticModuleState());
#endif
```

 

 



