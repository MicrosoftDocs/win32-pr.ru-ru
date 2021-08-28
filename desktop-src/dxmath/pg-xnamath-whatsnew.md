---
description: Библиотека Директксмас основана на библиотеке XNA Math C++ SIMD Library версии 2. x. Здесь описывается отличие Директксмас от XNA Math и отличия версий Директксмас.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Новые возможности (Директксмас)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e94d4ba2433501fb5389b82dab4f5c3de4b8ed80904ed4629729537bbf264a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984714"
---
# <a name="whats-new-directxmath"></a>Новые возможности (Директксмас)

Библиотека Директксмас основана на [библиотеке XNA Math C++ SIMD версии 2,04](https://walbourn.github.io/xna-math-version-2-04/). Здесь описывается отличие Директксмас от XNA Math и отличия версий Директксмас.

-   [Журнал рлеасе](#release-history)
-   [Директксмас различия от XNA Math](#directxmath-differences-from-xna-math)
-   [Связанные темы](#related-topics)

## <a name="release-history"></a>История выпусков

<table>
 <tr>
  <td>Windows 10 Пакет SDK (20348), версия 2104</td><td>Директксмас 3,16</td>
 </td>
 <tr>
  <td>Windows 10 Май 2020 обновление пакета SDK</td><td>Директксмас 3,14</td>
 </tr>
 <tr>
  <td>обновление Windows 10 за октябрь 2018 г. Tool</td><td>Директксмас 3,13</td>
 </tr>
 <tr>
  <td>Windows 10 Пакет SDK для обновления за Апрель 2018<br />Windows 10 Fall Creators Update Tool</td><td>Директксмас 3,11</td>
 </tr>
 <tr>
  <td>Windows 10 Creators Update Tool</td><td>Директксмас 3,10</td>
 </tr>
 <tr>
  <td>Windows 10 Пакет SDK для годовщины</td><td>Директксмас 3,09</td>
 </tr>
 <tr>
  <td>Windows 10 Пакет SDK (Ноябрь 2015)</td><td>Директксмас 3,08</td>
 </tr>
 <tr>
  <td>Windows пакет SDK для Windows 8.1 (пружины 2015)</td><td>Директксмас 3,07</td>
 </tr>
 <tr>
  <td>Windows Пакет SDK для Windows 8.1</td><td>Директксмас 3,06</td>
 </tr>
 <tr>
  <td>Windows Пакет SDK для Windows 8</td><td>Директксмас 3,03</td>
 </tr>
</table>

Дополнительные сведения см. в разделе [директксмас releases](https://github.com/Microsoft/DirectXMath/releases) .

## <a name="directxmath-differences-from-xna-math"></a>Директксмас различия от XNA Math

Вот как библиотека Директксмас в основном отличается от библиотеки XNA Math:

-   Директксмас имеет только C++ (пространства имен, перегрузки, новые шаблоны и т. д.).
-   Требуется поддержка стандартной библиотеки C++ 11 (т. е. stdint. h и т. д.).
-   встроенная поддержка ARM-NEON для платформы Windows RT.
-   Новые функции цвета (преобразования цветового пространства, константы цвета .NET).
-   Ограничивающие типы томов (версия, которая ранее была в заголовке Кснаколлисион в примере конфликта SDK DirectX).
-   Версия Xbox 360 недоступна. XDK Xbox 360 переходит на Кснамас v2. x; Удаление конкретных типов данных и вариантов функций Xbox 360.
-   Переработано [**ксмвекторпермуте**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) для улучшения оптимизации SSE и встроенных функций ARM-Neon.
-   Тип [**ксмматрикс**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) является полностью непрозрачным. Для доступа к отдельным элементам **ксмматрикс** используйте другие типы, например [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Директксмас по программированию](ovw-xnamath-progguide.md)
</dt> <dt>

[Выпуски Директксмас](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
