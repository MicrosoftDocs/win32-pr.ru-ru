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
ms.openlocfilehash: 37e84b9e5117732784267374ad9e6618e60d3b4020a6d23863b069b3b8233aa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161005"
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

 

 




