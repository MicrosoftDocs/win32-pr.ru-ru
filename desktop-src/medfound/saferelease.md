---
description: саферелеасе
ms.assetid: 2e9af7bc-f478-4a9c-b28f-b0a72fa9ec75
title: саферелеасе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46359821dd1f7741f6038ddb2f33cec591aacdf1bf9fc7fd3e6004e9d7601e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034872"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[О Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)
</dt> </dl>

 

 
