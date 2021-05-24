---
description: Функции набора Direct3D 10 не содержат ссылку на объект устройства-потомка.
ms.assetid: 4f4e1af8-5830-4b2d-ba2e-dc2ec4e74a19
title: Подсчет ссылок (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3587466aa3ecaea5f3a77332c77654b0725bb1
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335458"
---
# <a name="reference-counting-direct3d-10"></a><span data-ttu-id="b1946-103">Подсчет ссылок (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="b1946-103">Reference Counting (Direct3D 10)</span></span>

<span data-ttu-id="b1946-104">Функции набора Direct3D 10 не содержат ссылку на объект устройства-потомка.</span><span class="sxs-lookup"><span data-stu-id="b1946-104">Direct3D 10 set functions do not hold a reference to a device-child object.</span></span> <span data-ttu-id="b1946-105">Это означает, что каждое приложение должно содержать ссылку на дочерний объект устройства, пока объект должен быть привязан к конвейеру.</span><span class="sxs-lookup"><span data-stu-id="b1946-105">This means that each application must hold a reference to a device-child object for as long as the object needs to be bound to the pipeline.</span></span> <span data-ttu-id="b1946-106">Когда число ссылок объекта становится равным нулю, объект будет отменен из конвейера и уничтожен.</span><span class="sxs-lookup"><span data-stu-id="b1946-106">When the reference count of an object drops to zero, the object will be unbound from the pipeline and destroyed.</span></span> <span data-ttu-id="b1946-107">Этот стиль ссылки, удерживаемый также, называется слабой ссылкой, так как каждое расположение привязки конвейера содержит слабую ссылку на интерфейс или объект, который привязан к нему.</span><span class="sxs-lookup"><span data-stu-id="b1946-107">This style of reference holding is also known as weak-reference holding because each pipeline binding location holds a weak reference to the interface/object that is bound to it.</span></span>

<span data-ttu-id="b1946-108">Пример:</span><span class="sxs-lookup"><span data-stu-id="b1946-108">For example:</span></span>


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





<span data-ttu-id="b1946-109">Различия между Direct3D 9 и Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="b1946-109">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="b1946-110">В Direct3D 9 функции SET содержат ссылку на объекты устройства; в Direct3D 10 функции set не содержат ссылку на объекты-потомки устройства.</span><span class="sxs-lookup"><span data-stu-id="b1946-110">In Direct3D 9, set functions hold a reference to the device objects; in Direct3D 10 set functions do not hold a reference to the device-child objects.</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="b1946-111">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b1946-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1946-112">Функции API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="b1946-112">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




