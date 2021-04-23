---
description: В следующем примере кода показано, как выбрать терминалы на потоках, связанных с вызовом.
ms.assetid: ff43e81c-ff39-466d-870a-54b75c2938a4
title: Выберите терминал
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac3d195e021f5937c733f3d7a0efce0cfee5eba9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674465"
---
# <a name="select-a-terminal"></a><span data-ttu-id="44c02-103">Выберите терминал</span><span class="sxs-lookup"><span data-stu-id="44c02-103">Select a Terminal</span></span>

<span data-ttu-id="44c02-104">В следующем примере кода показано, как выбрать терминалы на потоках, связанных с вызовом.</span><span class="sxs-lookup"><span data-stu-id="44c02-104">The following code example demonstrates how to select terminals onto streams associated with a call.</span></span>

<span data-ttu-id="44c02-105">Перед использованием этого примера кода необходимо выполнить операции в оснастке [инициализации TAPI](initialize-tapi.md) и [выбрать адрес](select-an-address.md).</span><span class="sxs-lookup"><span data-stu-id="44c02-105">Before using this code example, you must perform the operations in [Initialize TAPI](initialize-tapi.md) and [Select an Address](select-an-address.md).</span></span>

<span data-ttu-id="44c02-106">Кроме того, в этом примере требуется, чтобы приложение уже имело указатель на интерфейс [**итбасиккаллконтрол**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) входящего или исходящего вызова.</span><span class="sxs-lookup"><span data-stu-id="44c02-106">Also, this example requires that the application already have a pointer to the [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) interface of either an incoming or outgoing call.</span></span> <span data-ttu-id="44c02-107">Чтобы получить этот указатель, см. статью [выполнение вызова](make-a-call.md) или [получение вызова](receive-a-call.md) для примеров кода.</span><span class="sxs-lookup"><span data-stu-id="44c02-107">See [Make a Call](make-a-call.md) or [Receive a Call](receive-a-call.md) for code examples on how to obtain this pointer.</span></span>

> [!Note]  
> <span data-ttu-id="44c02-108">В этом примере отсутствует проверка ошибок и выпуски, соответствующие рабочему коду.</span><span class="sxs-lookup"><span data-stu-id="44c02-108">This example does not have the error checking and releases appropriate for production code.</span></span>

 

``` syntax
// pAddress is an ITAddress interface pointer.
// pBasicCall is an ITBasicCallControl interface pointer.

// Get the ITStreamControl interface.
ITStreamControl * pStreamControl;
HRESULT hr = pBasicCall->QueryInterface(
        IID_ITStreamControl,
        (void **) &pStreamControl
        );
// If ( hr != S_OK ) process the error here. 

// Enumerate the streams and select 
// terminals onto them.
IEnumStream * pEnumStreams;
ITStream    * pStream;
hr = pStreamControl->EnumerateStreams(&pEnumStreams);
// If ( hr != S_OK ) process the error here. 

while ( S_OK == pEnumStreams->Next(1, &pStream, NULL) )
{
    // Get the media type and direction of this stream.
    long                lMediaType;
    TERMINAL_DIRECTION  dir;
    hr = pStream->get_MediaType( &lMediaType );
    // If ( hr != S_OK ) process the error here. 
    hr = pStream->get_Direction( &dir );
    // If ( hr != S_OK ) process the error here. 

    // Create the default terminal for this media type and direction.
    //   If lMediaType == TAPIMEDIATYPE_VIDEO and
    //   dir == TD_RENDER, a dynamic video render terminal
    //   is required. Please see Incoming.cpp in 
    //   the samples section of the SDK. 
    // For all other terminals, get the default static terminal.
    ITTerminal * pTerminal;
    ITTerminalSupport * pTerminalSupport;
    hr = pAddress->QueryInterface( 
            IID_ITTerminalSupport, 
            (void **)&pTerminalSupport
         );
    // If ( hr != S_OK ) process the error here. 
    hr = pTerminalSupport->GetDefaultStaticTerminal(
            lMediaType,
            dir,
            pTerminal
         );
    // If ( hr != S_OK ) process the error here. 
    // Select the terminal on the stream.
    hr = pStream->SelectTerminal(pTerminal);
    // If ( hr != S_OK ) process the error here. 
}
```

## <a name="related-topics"></a><span data-ttu-id="44c02-109">См. также</span><span class="sxs-lookup"><span data-stu-id="44c02-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44c02-110">**итаддресс**</span><span class="sxs-lookup"><span data-stu-id="44c02-110">**ITAddress**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)
</dt> <dt>

[<span data-ttu-id="44c02-111">**итбасиккаллконтрол**</span><span class="sxs-lookup"><span data-stu-id="44c02-111">**ITBasicCallControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[<span data-ttu-id="44c02-112">**итстреамконтрол**</span><span class="sxs-lookup"><span data-stu-id="44c02-112">**ITStreamControl**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)
</dt> <dt>

[<span data-ttu-id="44c02-113">**итстреам**</span><span class="sxs-lookup"><span data-stu-id="44c02-113">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[<span data-ttu-id="44c02-114">**иенумстреам**</span><span class="sxs-lookup"><span data-stu-id="44c02-114">**IEnumStream**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[<span data-ttu-id="44c02-115">**иттерминал**</span><span class="sxs-lookup"><span data-stu-id="44c02-115">**ITTerminal**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)
</dt> <dt>

[<span data-ttu-id="44c02-116">**иттерминалсуппорт**</span><span class="sxs-lookup"><span data-stu-id="44c02-116">**ITTerminalSupport**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)
</dt> </dl>

 

 
