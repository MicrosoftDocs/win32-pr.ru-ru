---
description: В следующем примере кода показано, как создать объект call, обнаружить потоки, связанные с вызовом, выбрать и создать соответствующие терминалы, выбрать терминалы в потоках и завершить подключение.
ms.assetid: 49815b18-a8ea-46e0-b2a4-3d7a82e727b0
title: Выполнить вызов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc22ebde34e65c9acc8e6c7dd81944b06804935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683148"
---
# <a name="make-a-call"></a><span data-ttu-id="1f999-103">Выполнить вызов</span><span class="sxs-lookup"><span data-stu-id="1f999-103">Make a Call</span></span>

<span data-ttu-id="1f999-104">В следующем примере кода показано, как создать объект call, обнаружить потоки, связанные с вызовом, выбрать и создать соответствующие терминалы, выбрать терминалы в потоках и завершить подключение.</span><span class="sxs-lookup"><span data-stu-id="1f999-104">The following code example demonstrates how to create a call object, discover the streams associated with the call, select and create appropriate terminals, select the terminals onto the streams, and complete the connection.</span></span>

<span data-ttu-id="1f999-105">Перед использованием этого примера кода необходимо выполнить операции в оснастке [инициализации TAPI](initialize-tapi.md) и [выбрать адрес](select-an-address.md).</span><span class="sxs-lookup"><span data-stu-id="1f999-105">Before using this code example, you must perform the operations in [Initialize TAPI](initialize-tapi.md) and [Select an Address](select-an-address.md).</span></span>

<span data-ttu-id="1f999-106">Кроме того, необходимо выполнить операции, показанные в окне [Выбор терминала](select-a-terminal.md) после вызова [**Итаддресс:: креатекалл**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall).</span><span class="sxs-lookup"><span data-stu-id="1f999-106">Also, you must perform the operations illustrated in [Select a Terminal](select-a-terminal.md) following the call to [**ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall).</span></span>

> [!Note]  
> <span data-ttu-id="1f999-107">В этом примере отсутствует проверка ошибок и выпуски, соответствующие рабочему коду.</span><span class="sxs-lookup"><span data-stu-id="1f999-107">This example does not have the error checking and releases appropriate for production code.</span></span>

 

``` syntax
// Specify the destination address.
//
// szAddressToCall and 
// dwAddressType have been
// retrieved from a user interface.
ITBasicCallControl * pBasicCall
bstrAddressToCall = SysAllocString( szAddressToCall );
// If ( bstrAddressToCall == NULL ) process the error here. 

HRESULT hr = pAddress->CreateCall(
    bstrAddressToCall,
    dwAddressType,
    &pBasicCall
 );
// If ( hr != S_OK ) process the error here. 

SysFreeString(bstrAddressToCall);

// Create the required terminals for this call.
{
    // See the Select a Terminal code example.
}

// Make the connection.
pBasicCall->Connect( TRUE );
```

## <a name="related-topics"></a><span data-ttu-id="1f999-108">См. также</span><span class="sxs-lookup"><span data-stu-id="1f999-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f999-109">**Итаддресс:: Креатекалл**</span><span class="sxs-lookup"><span data-stu-id="1f999-109">**ITAddress::CreateCall**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)
</dt> <dt>

[<span data-ttu-id="1f999-110">**итбасиккаллконтрол**</span><span class="sxs-lookup"><span data-stu-id="1f999-110">**ITBasicCallControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[<span data-ttu-id="1f999-111">**Итбасиккаллконтрол:: Connect**</span><span class="sxs-lookup"><span data-stu-id="1f999-111">**ITBasicCallControl::Connect**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect)
</dt> </dl>

 

 



