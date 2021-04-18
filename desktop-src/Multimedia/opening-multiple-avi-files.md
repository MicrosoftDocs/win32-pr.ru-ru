---
title: Открытие нескольких файлов AVI
description: Открытие нескольких файлов AVI
ms.assetid: 982bcea1-77b0-4a38-893d-1f506ffb18f5
keywords:
- Функция Инитави
- Функция Термави
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac540d670b15eaf1befb1d2f253223e3571ecee
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105681616"
---
# <a name="opening-multiple-avi-files"></a>Открытие нескольких файлов AVI

Если приложение открывает несколько файлов, оно должно включать в себя подпрограммы, такие как следующие простые функции. Приложение будет использовать функцию "Инитави" во время инициализации и функцию "Термави" во время ее завершения. Эти функции просто заключают функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .


```C++
// Initialize the MCIAVI driver. This returns TRUE if OK, 
// FALSE on error. 
 
BOOL initAVI(VOID) 
{ 
    // Perform additional initialization before loading first file. 
    return mciSendString("open digitalvideo", NULL, 0, NULL) == 0; 
} 
 
// Close the MCIAVI driver. 
void termAVI(VOID) 
{ 
    mciSendString("close digitalvideo", NULL, 0, NULL); 
} 
```



 

 