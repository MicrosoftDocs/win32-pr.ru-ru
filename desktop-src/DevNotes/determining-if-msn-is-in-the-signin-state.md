---
description: В следующем примере кода показано использование объекта Mutex для определения того, вошел ли MSN Explorer в.
ms.assetid: ec52a61c-9d2c-4327-977b-fb13d042bc37
title: Определение того, находится ли MSN в состоянии входа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da0abffc1735d2bf7af6ee6f9a68bf0d71ca1a2fda44176a0905c3e8faec6d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654196"
---
# <a name="determining-if-msn-is-in-the-sign-in-state"></a>Определение того, находится ли MSN в состоянии входа

В следующем примере кода показано использование объекта Mutex для определения того, вошел ли MSN Explorer в. По завершении использования маркера обязательно вызовите функцию [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .

> [!Note]  
> Этот объект мьютекса доступен для использования при проверке MSN Explorer 7. состояние входа *x* . В последующих версиях он может быть недоступен.

 


```C++
    HANDLE hMSNSignedInMutex;

    hMSNSignedInMutex = OpenMutex(SYNCHRONIZE, FALSE, 
        "{ECCC50B5-064B-4693-B104-925714A4C74B}");

    if (hMSNSignedInMutex != NULL)
    {
        // MSN Explorer is signed in
    }
```



 

 
