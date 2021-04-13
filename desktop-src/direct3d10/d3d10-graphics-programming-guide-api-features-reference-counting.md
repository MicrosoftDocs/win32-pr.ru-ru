---
description: Функции набора Direct3D 10 не содержат ссылку на объект устройства-потомка.
ms.assetid: 4f4e1af8-5830-4b2d-ba2e-dc2ec4e74a19
title: Подсчет ссылок (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6482918601f163bdea92291eb3927899ca797d29
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538573"
---
# <a name="reference-counting-direct3d-10"></a>Подсчет ссылок (Direct3D 10)

Функции набора Direct3D 10 не содержат ссылку на объект устройства-потомка. Это означает, что каждое приложение должно содержать ссылку на дочерний объект устройства, пока объект должен быть привязан к конвейеру. Когда число ссылок объекта становится равным нулю, объект будет отменен из конвейера и уничтожен. Этот стиль ссылки, удерживаемый также, называется слабой ссылкой, так как каждое расположение привязки конвейера содержит слабую ссылку на интерфейс или объект, который привязан к нему.

Пример:


```
pDevice->CreateRasterizerState( ..., &pRasterizerState );
pDevice->RSSetState( pRasterizerState );
 
pDevice->RSGetState( &pCurRasterizerState );
// pCurRasterizerState will be equal to pRasterizerState.
pCurRasterizerState->Release();
 
pRasterizerState->Release();
// Following the final release, the object is unbound.
pDevice->RSGetState( &pCurRasterizerState );
// pCurRasterizerState will be equal to NULL.
```





|                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Различия между Direct3D 9 и Direct3D 10:<br/> В Direct3D 9 функции SET содержат ссылку на объекты устройства; в Direct3D 10 функции set не содержат ссылку на объекты-потомки устройства.<br/> |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Функции API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




