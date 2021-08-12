---
description: 'Объект буфера вершин создается путем вызова метода IDirect3DDevice9:: Креатевертексбуффер, который принимает пять параметров.'
ms.assetid: 95116ef5-af88-47e7-abf7-1ade9735e2a7
title: Создание буфера вершин (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c12cb50d7879ef73d4c760ac61a0698651cb9ed7d334c90475bd2e8ee4148db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527678"
---
# <a name="creating-a-vertex-buffer-direct3d-9"></a>Создание буфера вершин (Direct3D 9)

Объект буфера вершин создается путем вызова метода [**IDirect3DDevice9:: креатевертексбуффер**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) , который принимает пять параметров. Первый параметр указывает длину буфера вершин в байтах. Используйте оператор sizeof для определения размера формата вершины в байтах. Рассмотрим следующий пользовательский формат вершин.


```
struct CUSTOMVERTEX {
        FLOAT x, y, z;
        FLOAT rhw;
        DWORD color;
        FLOAT tu, tv;   // Texture coordinates
};

// Custom flexible vertex format (FVF) describing the custom vertex structure
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)
```



Чтобы создать буфер вершин для хранения четырех структур КУСТОМВЕРТЕКС, укажите \[ \* \] в параметре *length* 4 sizeof (кустомвертекс).

Второй параметр — это набор элементов управления использованием. Помимо прочего, его значение определяет, может ли буфер вершин содержать сведения об обрезке в форме флагов клипов — для вершин, которые существуют за пределами области просмотра. Чтобы создать буфер вершин, который не может содержать флаги обрезки, включите \_ флаг D3DUSAGE донотклип для параметра *использования* . Флаг D3DUSAGE \_ донотклип применяется только в том случае, если также указано, что буфер вершин будет содержать преобразованные вершины — флаг D3DFVF \_ ксизрхв включен в параметр *фвф* . Метод [**IDirect3DDevice9:: креатевертексбуффер**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) ИГНОРИРУЕТ \_ флаг D3DUSAGE донотклип, если вы указываете, что буфер будет содержать непреобразованные вершины ( \_ флаг D3DFVF XYZ). Флаги обрезки занимают дополнительную память, что делает буфер вершин, поддерживающий отрезки, немного больше, чем буфер вершин, в котором не может составляться флаги обрезки. Так как эти ресурсы выделяются при создании буфера вершин, необходимо заранее запросить буфер вершин, поддерживающий обрезку.

Третий параметр, *фвф*, представляет собой сочетание [D3DFVF](d3dfvf.md) , описывающее формат вершины буфера вершин. Если для этого параметра задано значение 0, то буфер вершин представляет собой буфер вершин, отличный от ФВФ. Дополнительные сведения см. в разделе [Фвф вершинные буферы (Direct3D 9)](fvf-vertex-buffers.md). Четвертый параметр описывает класс памяти, в который помещается буфер вершин.

Последний параметр, [**IDirect3DDevice9:: креатевертексбуффер**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) , принимает адрес переменной, которая будет заполнена указателем на новый интерфейс [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) объекта буфера вершин, если вызов завершается.

Нельзя создавать флаги клипов для буфера вершин, созданного без поддержки.

В следующем примере кода C++ показано, что создание буфера вершин может выглядеть как в коде.


```
   
// d3dDevice contains the address of an IDirect3DDevice9 interface
// g_pVB is a variable of type LPDIRECT3DVERTEXBUFFER9 

// The custom vertex type
struct CUSTOMVERTEX {
    FLOAT x, y, z;
    FLOAT rhw;
    DWORD color;
    FLOAT tu, tv;   // The texture coordinates
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)

// Create a clipping-capable vertex buffer. Allocate enough memory 
// in the default memory pool to hold three CUSTOMVERTEX 
// structures

    if( FAILED( d3dDevice->CreateVertexBuffer( 3*sizeof(CUSTOMVERTEX),
            0 /*Usage*/, D3DFVF_CUSTOMVERTEX, D3DPOOL_DEFAULT, &g_pVB, NULL ) ) )
        return E_FAIL;
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Буферы вершин](vertex-buffers.md)
</dt> </dl>

 

 
