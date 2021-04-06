---
description: Создание экземпляра кодека дмос
ms.assetid: e031d0d4-dd70-409e-8a2e-5a1433fe909e
title: Создание экземпляра кодека дмос
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7b98848b3e3fee5b3c28389294869eb39005c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991091"
---
# <a name="instantiating-codec-dmos"></a>Создание экземпляра кодека дмос

Можно создать кодек DMO, вызвав функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com. Необходимо передать идентификатор класса DMO, идентификатор интерфейса **имедиаобжект** и указатель на указатель **имедиаобжект** .

Идентификаторы класса кодека дмос определены как константы в файле заголовка вмкодекдсп. h.

Константа для идентификатора интерфейса **имедиаобжект** — IID \_ имедиаобжект.

В следующем примере кода показано, как создать экземпляр объекта DMO для кодека:


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Работа с кодеками дмос](workingwithcodecdmos.md)
</dt> </dl>

 

 
