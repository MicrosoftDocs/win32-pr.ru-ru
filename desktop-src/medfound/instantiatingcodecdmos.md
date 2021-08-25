---
description: Создание экземпляра кодека дмос
ms.assetid: e031d0d4-dd70-409e-8a2e-5a1433fe909e
title: Создание экземпляра кодека дмос
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 180fcb6a3de7c581f48c7f78981e12b544963cbfb590e521d43413732bcc1e7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957554"
---
# <a name="instantiating-codec-dmos"></a>Создание экземпляра кодека дмос

вы можете создать кодек DMO, вызвав функцию [**cocreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) COM. необходимо передать идентификатор класса DMO, идентификатор интерфейса **имедиаобжект** и указатель на указатель **имедиаобжект** .

Идентификаторы класса кодека дмос определены как константы в файле заголовка вмкодекдсп. h.

Константа для идентификатора интерфейса **имедиаобжект** — IID \_ имедиаобжект.

В следующем примере кода показано, как создать экземпляр кодека DMO:


```
HRESULT CreateVideoEncoderDMO(IMediaObject** ppDMO)
{
    if(ppDMO == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMediaObject, 
                            (void**)ppDMO);
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Работа с кодеками дмос](workingwithcodecdmos.md)
</dt> </dl>

 

 
