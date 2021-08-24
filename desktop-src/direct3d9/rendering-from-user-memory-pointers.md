---
description: Дополнительный набор интерфейсов отрисовки поддерживает передачу данных вершин и индексов непосредственно из указателей памяти пользователя. Эти интерфейсы поддерживают только один поток данных вершин. Дополнительные сведения см. в следующих справочных разделах.
ms.assetid: 6f64cc17-cffc-4d18-acf2-73e400fa26f9
title: Отрисовка из указателей памяти пользователя (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9893d3728b3bac8bc38dd8118f995510de834d2c6e54cdadcafe2c26b8a78e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746484"
---
# <a name="rendering-from-user-memory-pointers-direct3d-9"></a>Отрисовка из указателей памяти пользователя (Direct3D 9)

Дополнительный набор интерфейсов отрисовки поддерживает передачу данных вершин и индексов непосредственно из указателей памяти пользователя. Эти интерфейсы поддерживают только один поток данных вершин. Дополнительные сведения см. в следующих справочных разделах.

-   [**IDirect3DDevice9::DrawPrimitiveUP**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup)
-   [**IDirect3DDevice9::DrawIndexedPrimitiveUP**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitiveup)

Эти методы отображаются с данными, заданными указателями памяти пользователя, а не буферами вершин и индексов.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Отрисовка примитивов](rendering-primitives.md)
</dt> </dl>

 

 
