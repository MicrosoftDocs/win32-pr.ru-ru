---
description: Термин Блит является сокращением для &\# 0034; передача битового блока &\# 0034; что представляет собой процесс передачи блоков данных из одного места в памяти в другое.
ms.assetid: 5f2aed2e-66d2-40e6-be35-92c3f92d17bd
title: Копирование поверхностей (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50000e3b620c4d2fd217695551d898e5892430ba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692026"
---
# <a name="copying-surfaces-direct3d-9"></a>Копирование поверхностей (Direct3D 9)

Термин Блит является сокращением для "передачи битового блока", который представляет собой процесс передачи блоков данных из одного места в памяти в другое. Интерфейс драйвера устройства блиттинг (DDI) по-своему используется в Direct3D 9 в качестве основного механизма перемещения больших прямоугольников пикселей в зависимости от каждого кадра, механизма копирования, ориентированного на метод повторного выполнения [**IDirect3DDevice9::P**](/windows/desktop/api) . Транспорт иллюстраций в операции Блит выполняется методом [**IDirect3DDevice9:: упдатетекстуре**](/windows/desktop/api) . Кроме того, иллюстрацию можно скопировать в Direct3D 9 с помощью метода [**IDirect3DDevice9:: упдатесурфаце**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) , который копирует прямоугольное подмножество пикселей.

> [!Note]  
> Direct3D 9 предоставляет функции D3DX, позволяющие загружать иллюстрации из файлов, применять преобразование цветов и изменять размеры иллюстраций. Дополнительные сведения о доступных функциях см. [в разделе функции текстуры в D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md).

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Поверхности Direct3D](direct3d-surfaces.md)
</dt> <dt>

[**IDirect3DDevice9:: Стретчрект**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> <dt>

**IDirect3DDevice9:: Стретчрект**
</dt> </dl>

 

 
