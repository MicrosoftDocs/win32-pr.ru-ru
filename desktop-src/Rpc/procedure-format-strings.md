---
title: Строки формата процедур
description: Ниже приведено полное описание строки формата. Он собирает все уровни, связанные с разными этапами развития интерпретатора.
ms.assetid: fab603ed-1f68-4e0b-9c8d-b9730b8cd389
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb17434a1c05b66212283237d61ee4492aa23ed0bf1ecca75f1fec1b3ddd784b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019062"
---
# <a name="procedure-format-strings"></a>Строки формата процедур

Ниже приведено полное описание строки формата. Он собирает все уровни, связанные с разными этапами развития интерпретатора.

## <a name="procedure-descriptor-overview"></a>Обзор дескрипторов процедур

Дескриптор процедуры состоит из описательов заголовков и описательных параметров. Описание стиля [**– Oi**](/windows/desktop/Midl/-oi) считается устаревшим, в терминах общего использования в текущем программировании RPC. Параметр **– ОИФ** считается более актуальным.

## <a name="the-oi-style-description"></a>Описание стиля – OI

Это описание состоит из следующих компонентов:

``` syntax
-Oi_style_header_descriptor<>
{-Oi_style_parameter_descriptor<>}*
```

Заголовок будет содержать от 6 до 16 байт.

Полное описание создается при компиляции в режиме [**– Oi**](/windows/desktop/Midl/-oi) . В режиме [**операционной системы**](/windows/desktop/Midl/-os) создаются только дескрипторы параметров, которые используются для преобразования. Интерпретатор в поле выбора использует устаревшие дескрипторы параметров стиля.

## <a name="the-oif-style-description"></a>Описание стиля – ОИФ

Описание состоит из следующих элементов:

``` syntax
-Oif_style_header_descriptor<>
{-Oif_style_parameter_descriptor<6>}*
```

Дескриптор заголовка стиля [**– ОИФ**](/windows/desktop/Midl/-oi) состоит из

Описание стиля – ОИФ создается при компиляции в режиме компилятора [**– ОИФ**](/windows/desktop/Midl/-oi) или **– оикф** .

``` syntax
-Oi_style_header_descriptor<>
-Oif_extensions_to_the_old_header<6>
```

Некоторые более новые функции, такие как pipe, async и [**/robust**](/windows/desktop/Midl/-robust) , принудительно используют режим [**– оикф**](/windows/desktop/Midl/-oi) компилятора при его использовании.

## <a name="the-extended-oif-description"></a>Расширенное описание – ОИФ

Описание состоит из следующих элементов:

``` syntax
-Oif_style_header_descriptor<>
extensions_to_the_-Oif_header<8>
{-Oif style parameter descriptors<6>}*
```

 

 