---
title: Регистр постоянного float (Справочник по HLSL VS)
description: Входной регистр шейдера вершин для четырех компонентов с плавающей запятой. Установите регистр константы с помощью DEF-VS или Сетвертексшадерконстантф.
ms.assetid: 45a14258-52d5-4c22-885f-5af20ae36251
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c81cc05a40ebb7ede53fb14c957584f289a14a15045a2b69f557072c6885c9ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949934"
---
# <a name="constant-float-register-hlsl-vs-reference"></a>Регистр постоянного float (Справочник по HLSL VS)

Входной регистр шейдера вершин для четырех компонентов с плавающей запятой. Установите регистр константы с помощью [DEF-VS](def---vs.md) или [**сетвертексшадерконстантф**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf).

Файл регистра константы доступен только для чтения с точки шейдера вершин. Любая одна инструкция может обращаться только к одному регистру констант. Однако каждый источник в этой инструкции может независимо свиззле и инвертировать этот вектор по мере считывания.

Поведение констант шейдера изменилось между Direct3D 8 и Direct3D 9.

-   Для Direct3D 9 константы, заданные с помощью дефкс, присваивают значения константному пространству шейдера. Время существования константы, объявленной с помощью дефкс, ограничено выполнением только этого шейдера. И наоборот, константы, заданные с помощью API-интерфейсов, Сетксксксшадерконстанткс инициализировать константы в глобальном пространстве. Константы в глобальном пространстве не копируются в локальное пространство (видимую шейдеру) до тех пор, пока не будет вызван Сетксксксшадерконстантс.
-   Для Direct3D 8 константы, заданные с помощью дефкс или API, присваивают значения константному пространству шейдера. При каждом выполнении шейдера все константы используются текущим шейдером независимо от метода, используемого для их установки.

Регистр константы обозначается как абсолютный или относительный:


```
c[n]           ; absolute
c[a0.x + n]    ; relative - supported only in version 1_1
```



Регистр констант может быть считан, поэтому либо с помощью абсолютного индекса, либо с относительным индексом от регистра адресов. Операции чтения из недопустимых регистров возвращают (0,0, 0,0, 0,0, 0,0).

## <a name="examples"></a>Примеры

Ниже приведен пример объявления двух констант с плавающей запятой в шейдере.


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



Эти константы загружаются каждый раз при вызове [**сетвертексшадер**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) .

Ниже приведен пример использования API.


```
    // Set up the vertex shader constants.
    {
        D3DXMATRIXA16 mat;
        D3DXMatrixMultiply( &mat, &m_matView, &m_matProj );
        D3DXMatrixTranspose( &mat, &mat );

        D3DXVECTOR4 vA( sinf(m_fTime)*15.0f, 0.0f, 0.5f, 1.0f );
        D3DXVECTOR4 vD( D3DX_PI, 1.0f/(2.0f*D3DX_PI), 2.0f*D3DX_PI, 0.05f );

        // Taylor series coefficients for sin and cos.
        D3DXVECTOR4 vSin( 1.0f, -1.0f/6.0f, 1.0f/120.0f, -1.0f/5040.0f );
        D3DXVECTOR4 vCos( 1.0f, -1.0f/2.0f, 1.0f/ 24.0f, -1.0f/ 720.0f );

        m_pd3dDevice->SetVertexShaderConstantF(  0, (float*)&mat,  4 );
        m_pd3dDevice->SetVertexShaderConstantF(  4, (float*)&vA,   1 );
        m_pd3dDevice->SetVertexShaderConstantF(  7, (float*)&vD,   1 );
        m_pd3dDevice->SetVertexShaderConstantF( 10, (float*)&vSin, 1 );
        m_pd3dDevice->SetVertexShaderConstantF( 11, (float*)&vCos, 1 );
    }
```



Если вы устанавливаете постоянные значения с помощью API, то объявление шейдера не требуется.



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Регистр констант      | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Регистры шейдеров вершин](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 