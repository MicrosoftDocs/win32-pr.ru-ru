---
title: D1101 неизвестный маркер
ms.assetid: ae40058a-ea17-4262-87dc-0ce852c16c2a
description: В нее передан интерфейс, не выделенный этой библиотекой DLL.
keywords:
- D1101 неизвестный Handle Direct2D
topic_type:
- apiref
api_name:
- D1101 Unknown Handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2a87491a02d3dea992f8dd767ad34cf83b2cbf40
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2021
ms.locfileid: "105658174"
---
# <a name="d1101-unknown-handle"></a>D1101: неизвестный маркер

\[  \] В нее не был передан интерфейс интерфейса, не выделенный этой библиотекой DLL.

## <a name="placeholders"></a>Заполнители

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*взаимодействия*
</dt> <dd>

Адрес интерфейса.

</dd> </dl> 




 

## <a name="possible-causes"></a>Возможные причины

Недопустимое использование ресурсов. Ресурс, созданный за пределами Direct2D, используется с фабрикой Direct2D, или ресурсы, созданные в одной фабрике, использовались с ресурсом, созданным другой фабрикой.

 

 




