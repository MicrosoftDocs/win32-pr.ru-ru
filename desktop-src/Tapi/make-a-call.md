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
# <a name="make-a-call"></a>Выполнить вызов

В следующем примере кода показано, как создать объект call, обнаружить потоки, связанные с вызовом, выбрать и создать соответствующие терминалы, выбрать терминалы в потоках и завершить подключение.

Перед использованием этого примера кода необходимо выполнить операции в оснастке [инициализации TAPI](initialize-tapi.md) и [выбрать адрес](select-an-address.md).

Кроме того, необходимо выполнить операции, показанные в окне [Выбор терминала](select-a-terminal.md) после вызова [**Итаддресс:: креатекалл**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall).

> [!Note]  
> В этом примере отсутствует проверка ошибок и выпуски, соответствующие рабочему коду.

 

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

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Итаддресс:: Креатекалл**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)
</dt> <dt>

[**итбасиккаллконтрол**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**Итбасиккаллконтрол:: Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect)
</dt> </dl>

 

 



