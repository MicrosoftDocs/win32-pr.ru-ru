---
title: Интерфейсы D3DX (графика Direct3D 11)
description: В этом разделе содержатся справочные сведения о COM-интерфейсах, предоставляемых библиотекой служебной программы D3DX.
ms.assetid: 0d3be1e6-b558-4586-9440-251a5611d7cd
keywords:
- Интерфейсы D3DX, Direct3D 11
- интерфейсы, Direct3D 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da2890c3c55d1bac9eba09c046927e432b1a27f8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104070943"
---
# <a name="d3dx-interfaces-direct3d-11-graphics"></a>Интерфейсы D3DX (графика Direct3D 11)

В этом разделе содержатся справочные сведения о COM-интерфейсах, предоставляемых библиотекой служебной программы D3DX.

> [!Note]  
> Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.

 


## <a name="in-this-section"></a>В этом разделе



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Раздел</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="id3dx11dataloader.md"><strong>ID3DX11DataLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.
</blockquote>
<br/> Объект загрузки данных, используемый <a href="id3dx11threadpump.md"><strong>интерфейсом ID3DX11ThreadPump</strong></a> для асинхронной загрузки данных.<br/></td>
</tr>
<tr class="even">
<td><a href="id3dx11dataprocessor.md"><strong>ID3DX11DataProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.
</blockquote>
<br/> Объект обработки данных, используемый <a href="id3dx11threadpump.md"><strong>интерфейсом ID3DX11ThreadPump</strong></a> для асинхронной загрузки данных.<br/></td>
</tr>
<tr class="odd">
<td><a href="id3dx11threadpump.md"><strong>ID3DX11ThreadPump</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.
</blockquote>
<br/> Конвейер потока выполняет задачи асинхронно. Он создается путем вызова <a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a>. Существует несколько интерфейсов API, принимающих дополнительный потоковый конвейер в качестве параметра, например <a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a> и <a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a>. Если передать в эти API интерфейс конвейера потока, функции будут выполняться асинхронно в отдельном потоке. В частности, на многопроцессорных компьютерах конвейер потоков может загружать ресурсы и обрабатывать данные без заметного снижения производительности.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по D3DX 11](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

 





