---
title: Загрузка и регистрация библиотеки типов
description: Библиотека динамической компоновки службы автоматизации, Oleaut32.dll, предоставляет несколько функций, которые можно вызывать для загрузки и регистрации библиотеки типов. Вызов Лоадтипелибекс, как показано в следующем примере, обе загружают библиотеку и создает записи реестра.
ms.assetid: b7404919-fa0a-4de8-8c85-41b7bc7c5a52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e98ea3a28f3884cbd6a377e45f1b537d169f510fdc4ce9a433dff6e976d9c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854234"
---
# <a name="loading-and-registering-a-type-library"></a>Загрузка и регистрация библиотеки типов

Библиотека динамической компоновки службы автоматизации, Oleaut32.dll, предоставляет несколько функций, которые можно вызывать для загрузки и регистрации библиотеки типов. Вызов [лоадтипелибекс](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), как показано в следующем примере, обе загружают библиотеку и создает записи реестра.

## <a name="example"></a>Пример

``` syntax
ITypeLib *pTypeLib;
HRESULT hr;
hr = LoadTypeLibEx("example.tlb", REGKIND_REGISTER, &pTypeLib);
if(SUCCEEDED(hr))
{
    pTypeLib->Release();
} else {
    exit(0); // Handle errors here.
}
```

 

 