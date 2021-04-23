---
description: В следующем примере кода показано использование объекта Mutex для определения того, вошел ли MSN Explorer в.
ms.assetid: ec52a61c-9d2c-4327-977b-fb13d042bc37
title: Определение того, находится ли MSN в состоянии входа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d7af3511035c997493f0439a8635c1a928a75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539122"
---
# <a name="determining-if-msn-is-in-the-sign-in-state"></a><span data-ttu-id="09e9c-103">Определение того, находится ли MSN в состоянии входа</span><span class="sxs-lookup"><span data-stu-id="09e9c-103">Determining if MSN Is in the Sign-in State</span></span>

<span data-ttu-id="09e9c-104">В следующем примере кода показано использование объекта Mutex для определения того, вошел ли MSN Explorer в.</span><span class="sxs-lookup"><span data-stu-id="09e9c-104">The following code example shows the usage of a mutex object to determine if MSN Explorer is signed in.</span></span> <span data-ttu-id="09e9c-105">По завершении использования маркера обязательно вызовите функцию [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="09e9c-105">When you have finished using the handle, be sure to call the [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) function.</span></span>

> [!Note]  
> <span data-ttu-id="09e9c-106">Этот объект мьютекса доступен для использования при проверке MSN Explorer 7. состояние входа *x* .</span><span class="sxs-lookup"><span data-stu-id="09e9c-106">This mutex object is available for use in checking MSN Explorer 7.*x* sign-in status.</span></span> <span data-ttu-id="09e9c-107">В последующих версиях он может быть недоступен.</span><span class="sxs-lookup"><span data-stu-id="09e9c-107">It may be unavailable in subsequent versions.</span></span>

 


```C++
    HANDLE hMSNSignedInMutex;

    hMSNSignedInMutex = OpenMutex(SYNCHRONIZE, FALSE, 
        "{ECCC50B5-064B-4693-B104-925714A4C74B}");

    if (hMSNSignedInMutex != NULL)
    {
        // MSN Explorer is signed in
    }
```



 

 
