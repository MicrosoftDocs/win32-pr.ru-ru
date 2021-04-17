---
description: саферелеасе
ms.assetid: 2e9af7bc-f478-4a9c-b28f-b0a72fa9ec75
title: саферелеасе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0661b8515c1d8a79c81eef19f49cf8996fcbf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711406"
---
# <a name="saferelease"></a>саферелеасе


Во многих примерах кода в этой документации для освобождения указателей COM-интерфейса используется следующая функция.


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



> [!Note]  
> Эта функция не определена в заголовке пакета SDK. Чтобы использовать эту функцию, необходимо определить ее в собственном коде.

 

Эта функция освобождает указатель *PPT* и устанавливает его равным **null**.

Другим вариантом является использование класса интеллектуального указателя, такого как **CComPtr**, который определен в библиотеке активных шаблонов (ATL).

## <a name="related-topics"></a>См. также

<dl> <dt>

[О Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)
</dt> </dl>

 

 
