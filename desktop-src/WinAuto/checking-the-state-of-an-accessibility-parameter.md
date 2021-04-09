---
title: Проверка состояния параметра специальных возможностей
description: В следующем фрагменте кода используется функция Жетсистемметрикс для проверки параметра субтитров. Если Жетсистемметрикс возвращает значение TRUE, приложение должно представлять всю важную информацию в визуальной форме.
ms.assetid: fb6a0adf-ca38-4e21-9edd-1abb2efd59e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75409f5af96f83bf13f4834f83503579862caa97
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070095"
---
# <a name="checking-the-state-of-an-accessibility-parameter"></a>Проверка состояния параметра специальных возможностей

В следующем фрагменте кода используется функция [**жетсистемметрикс**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) для проверки параметра субтитров. Если **жетсистемметрикс** возвращает **значение true**, приложение должно представлять всю важную информацию в визуальной форме.


```C++
BOOL fShowSounds; 
fShowSounds = GetSystemMetrics(SM_SHOWSOUNDS); 
```



 

 