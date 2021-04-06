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
# <a name="instantiating-codec-dmos"></a><span data-ttu-id="a87a8-103">Создание экземпляра кодека дмос</span><span class="sxs-lookup"><span data-stu-id="a87a8-103">Instantiating Codec DMOs</span></span>

<span data-ttu-id="a87a8-104">Можно создать кодек DMO, вызвав функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com.</span><span class="sxs-lookup"><span data-stu-id="a87a8-104">You can create a codec DMO by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) COM function.</span></span> <span data-ttu-id="a87a8-105">Необходимо передать идентификатор класса DMO, идентификатор интерфейса **имедиаобжект** и указатель на указатель **имедиаобжект** .</span><span class="sxs-lookup"><span data-stu-id="a87a8-105">You must pass the class identifier of the DMO, the interface identifier of **IMediaObject**, and a pointer to an **IMediaObject** pointer.</span></span>

<span data-ttu-id="a87a8-106">Идентификаторы класса кодека дмос определены как константы в файле заголовка вмкодекдсп. h.</span><span class="sxs-lookup"><span data-stu-id="a87a8-106">The class identifiers of the codec DMOs are defined as constants in the wmcodecdsp.h header file.</span></span>

<span data-ttu-id="a87a8-107">Константа для идентификатора интерфейса **имедиаобжект** — IID \_ имедиаобжект.</span><span class="sxs-lookup"><span data-stu-id="a87a8-107">The constant for the **IMediaObject** interface identifier is IID\_IMediaObject.</span></span>

<span data-ttu-id="a87a8-108">В следующем примере кода показано, как создать экземпляр объекта DMO для кодека:</span><span class="sxs-lookup"><span data-stu-id="a87a8-108">The following code example demonstrates how to create an instance of a codec DMO:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a87a8-109">См. также</span><span class="sxs-lookup"><span data-stu-id="a87a8-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a87a8-110">Работа с кодеками дмос</span><span class="sxs-lookup"><span data-stu-id="a87a8-110">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 
