---
title: Интерфейсы D3DX (графика Direct3D 11)
description: В этом разделе содержатся справочные сведения о COM-интерфейсах, предоставляемых библиотекой служебной программы D3DX.
ms.assetid: 0d3be1e6-b558-4586-9440-251a5611d7cd
keywords:
- Интерфейсы D3DX, Direct3D 11
- интерфейсы, Direct3D 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd67f82d3198ef25254b3a682c80dc98e0313321
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475747"
---
# <a name="d3dx-interfaces-direct3d-11-graphics"></a>Интерфейсы D3DX (графика Direct3D 11)

В этом разделе содержатся справочные сведения о COM-интерфейсах, предоставляемых библиотекой служебной программы D3DX.

> [!Note]  
> библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows.

 


## <a name="in-this-section"></a>В этом разделе




| Раздел | Описание | 
|-------|-------------|
| <a href="id3dx11dataloader.md"><strong>ID3DX11DataLoader</strong></a><br /> | <blockquote>[!Note]<br />библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows.</blockquote><br /> Объект загрузки данных, используемый <a href="id3dx11threadpump.md"><strong>интерфейсом ID3DX11ThreadPump</strong></a> для асинхронной загрузки данных.<br /> | 
| <a href="id3dx11dataprocessor.md"><strong>ID3DX11DataProcessor</strong></a><br /> | <blockquote>[!Note]<br />библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows.</blockquote><br /> Объект обработки данных, используемый <a href="id3dx11threadpump.md"><strong>интерфейсом ID3DX11ThreadPump</strong></a> для асинхронной загрузки данных.<br /> | 
| <a href="id3dx11threadpump.md"><strong>ID3DX11ThreadPump</strong></a><br /> | <blockquote>[!Note]<br />библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений магазина Windows.</blockquote><br /> Конвейер потока выполняет задачи асинхронно. Он создается путем вызова <a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a>. Существует несколько интерфейсов API, принимающих дополнительный потоковый конвейер в качестве параметра, например <a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a> и <a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a>. Если передать в эти API интерфейс конвейера потока, функции будут выполняться асинхронно в отдельном потоке. В частности, на многопроцессорных компьютерах конвейер потоков может загружать ресурсы и обрабатывать данные без заметного снижения производительности.<br /> | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по D3DX 11](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

 





