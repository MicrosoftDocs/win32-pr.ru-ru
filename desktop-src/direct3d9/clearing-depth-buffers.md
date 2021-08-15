---
description: Многие приложения C++ перед отрисовкой каждого нового кадра очищают буфер глубины.
ms.assetid: b8930211-82a1-4808-b042-1641e567cb6d
title: Очистка буферов глубины (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce150d729768321cb51abbea9f24ba8b490b7705f35945a4fd03e2a8ed58a039
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989314"
---
# <a name="clearing-depth-buffers-direct3d-9"></a>Очистка буферов глубины (Direct3D 9)

Многие приложения C++ перед отрисовкой каждого нового кадра очищают буфер глубины. Можно явным образом очистить буфер глубины с помощью Direct3D, вызвав [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) и указав D3DCLEAR \_ Збуффер для параметра flags. Метод **IDirect3DDevice9:: Clear** позволяет указать произвольное значение глубины в параметре Z.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Буферы глубины](depth-buffers.md)
</dt> </dl>

 

 
