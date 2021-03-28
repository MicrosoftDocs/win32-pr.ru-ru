---
title: Новые возможности пакета SDK для Windows 7 августа 2009 и Direct3D 11
description: Эта версия Windows 7 или Direct3D 11 поставляется в составе пакета SDK DirectX и содержит новые функции, средства и документацию.
ms.assetid: c2dc3726-70a0-49ff-bbad-8ef774bc4868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5e600e5dff679129bb9d007b9f1659bfd018d1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "103794820"
---
# <a name="whats-new-in-the-august-2009-windows-7direct3d-11-sdk"></a>Новые возможности пакета SDK для Windows 7 августа 2009 и Direct3D 11

Эта версия Windows 7 или Direct3D 11 поставляется в составе пакета SDK DirectX и содержит новые функции, средства и документацию.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Элемент</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Direct2D"></span><span id="direct2d"></span><span id="DIRECT2D"></span>Direct2D<br/></td>
<td>Direct2D — это высокопроизводительный высокоскоростной графический API, обеспечивающий высокую производительность и высококачественную отрисовку для двухмерной геометрии, точечных рисунков и текста. API Direct2D поддерживает взаимодействие с Direct3D и GDI. Этот пакет SDK позволяет разработчикам оценивать API и создавать простые приложения с использованием некоторых расширенных функций, доступных на правильно настроенных компьютерах. <br/> <a href="/windows/win32/direct2d/direct2d-portal">Документация</a> и <a href="/previous-versions//dd372354(v=vs.85)">примеры</a> для Direct2D в настоящее время доступны на сайте MSDN.<br/></td>
</tr>
<tr class="even">
<td><span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite<br/></td>
<td>DirectWrite обеспечивает поддержку высококачественной отрисовки текста, независимых от разрешения шрифтов, полную поддержку текста и макета в Юникоде, а также многое другое.<br/>
<ul>
<li>Независимая от устройства система макета текста, улучшающая удобочитаемость текста в документах и в пользовательском интерфейсе.<br/></li>
<li>Высококачественная, Подпиксельная визуализация текста ClearType, которая может использовать GDI Direct3D, Direct2D или технологию отрисовки для конкретного приложения.<br/></li>
<li>Поддержка многоязычного текста. <br/></li>
<li>Поддержка расширенных типографских функций шрифтов OpenType.<br/></li>
<li>Поддержка макета и отрисовки текста во всех языках, поддерживаемых Windows.<br/></li>
</ul>
Этот пакет SDK позволяет разработчикам оценивать API и создавать базовые приложения только в демонстрационных целях.<br/> <a href="/windows/win32/directwrite/direct-write-portal">Документация</a> и <a href="/windows/win32/directwrite/samples">примеры</a> для DirectWrite в настоящее время доступны на сайте MSDN.<br/></td>
</tr>
<tr class="odd">
<td><span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1,1<br/></td>
<td><a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi-overviews">Dxgi 1,1</a> строится на DXGI 1,0 и будет доступно как в Windows Vista, так и в Windows 7. DXGI 1,1 добавляет несколько новых функций:<br/>
<ul>
<li>Поддержка синхронизированных общих поверхностей. Это обеспечивает эффективное совместное использование поверхности чтения и записи для нескольких D3D (может быть между D3D10 и D3D11).<br/></li>
<li>Поддержка формата BGRA. Это позволяет GDI отображаться на той же поверхности DXGI, которая предназначена для устройства Direct2D, Direct3D 10,1 или Direct3D 11. <br/></li>
<li>Максимальная задержка кадра. С помощью <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency"><strong>IDXGIDevice1:: сетмаксимумфрамелатенци</strong></a> и <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency"><strong>IDXGIDevice1:: жетмаксимумфрамелатенци</strong></a>заголовки могут управлять числом кадров, которые могут храниться в очереди, перед отправкой для подготовки к просмотру. Задержка часто используется для управления тем, как ЦП выбирает между ответами на вводимые пользователем данные и фреймами, находящиеся в очереди отрисовки.<br/></li>
<li>Перечисление адаптеров. С помощью <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1"><strong>IDXGIFactory1:: EnumAdapters1</strong></a>заголовки могут перечислять локальные адаптеры без подключенных мониторов или выходных данных, а также адаптеры с присоединенными выходами.<br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>Обновленные примеры<br/></td>
<td>В этом выпуске есть несколько новых и обновленных примеров.<br/>
<ul>
<li>Новый <a href="https://msdn.microsoft.com/library/Ee416556(v=VS.85).aspx">AdaptiveTessellationCS40</a> — это иллюстрация более сложных методов обработки шейдеров вычислений, которые можно ЗАПУСКАТЬ на D3D10 или D3D11 GPU.</li>
<li><a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">Пример HDRToneMappingCS11</a> был расширен для реализации эффектов размытия и раскрытияа (в дополнение к сопоставлению тонов) с помощью COMPUTE Shader, а также для сравнения реализаций шейдеров пикселей.</li>
<li><a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">Пример MultithreadedRendering11</a> был значительно обновлен, благодаря более сложным материалам для графических ресурсов и более интенсивной обработке потоков.</li>
<li><a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">Образец SubD11</a> был обновлен с использованием новой модели лица, и теперь в примере используется функция вычисления соседей в средстве экспорта содержимого примеров.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Функции, появившиеся в предыдущих выпусках](d3d11-features-introduced-previous-releases.md)
</dt> </dl>

