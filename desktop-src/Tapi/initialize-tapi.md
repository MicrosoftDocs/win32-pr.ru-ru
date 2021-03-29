---
description: В следующем примере кода показано создание объекта TAPI.
ms.assetid: f8566e53-51c9-4424-a8bb-369455f35706
title: Инициализация TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78062e71df2d68895a645ca8a6c4c480a1415cd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912776"
---
# <a name="initialize-tapi"></a>Инициализация TAPI

В следующем примере кода показано создание объекта TAPI.

```cpp
const auto result = ITTAPI::Initialize();

if (result != S_OK) {
    switch (result) {
        case S_FALSE: {
            std::cerr << "TAPI has already been initialized.\n";
        } break;

        [[fallthrough]]
        case E_OUTOFMEMORY: {
            std::cerr << "Insufficient memory exists to perform the operation.\n";
        }

        default: {
            // TODO: Handle unrecoverable error here
        }
    }
}
```

## <a name="see-also"></a>См. также:

- [ИТТАПИ:: Initialize](/windows/win32/api/tapi3if/nf-tapi3if-ittapi-initialize)
- [Общие значения HRESULT](../seccrypto/common-hresult-values.md)
