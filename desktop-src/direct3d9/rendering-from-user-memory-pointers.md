---
description: Дополнительный набор интерфейсов отрисовки поддерживает передачу данных вершин и индексов непосредственно из указателей памяти пользователя. Эти интерфейсы поддерживают только один поток данных вершин. Дополнительные сведения см. в следующих справочных разделах.
ms.assetid: 6f64cc17-cffc-4d18-acf2-73e400fa26f9
title: Отрисовка из указателей памяти пользователя (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b5499032e6fb92ea0f363bba2bd5fd961e53c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262418"
---
# <a name="rendering-from-user-memory-pointers-direct3d-9"></a>Отрисовка из указателей памяти пользователя (Direct3D 9)

Дополнительный набор интерфейсов отрисовки поддерживает передачу данных вершин и индексов непосредственно из указателей памяти пользователя. Эти интерфейсы поддерживают только один поток данных вершин. Дополнительные сведения см. в следующих справочных разделах.

-   [**IDirect3DDevice9::DrawPrimitiveUP**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup)
-   [**IDirect3DDevice9::DrawIndexedPrimitiveUP**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitiveup)

Эти методы отображаются с данными, заданными указателями памяти пользователя, а не буферами вершин и индексов.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Отрисовка примитивов](rendering-primitives.md)
</dt> </dl>

 

 
