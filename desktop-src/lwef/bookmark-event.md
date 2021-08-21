---
title: Событие закладки
description: Событие закладки
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c6a6dcd072b87c6a924c8d33e6ebb73c75c927bdf955f51612703d3fc18af79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976714"
---
# <a name="bookmark-event"></a>Событие закладки

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возникает при активации закладки в текстовой строке в речевом коде, заданной приложением.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 Закладка подпрограммы- *агента* \_  **(ByVal** *букмаркид * *)**



| Часть         | Описание                                     |
|--------------|-------------------------------------------------|
| *BookmarkID* | Длинное целое число, определяющее номер закладки. |



 

</dd> </dl>

### <a name="remarks"></a>Remarks

Чтобы указать событие закладки, используйте метод [**говорите**](speak-method.md) с тегом **МРК** в заданном тексте. Дополнительные сведения о тегах см. в разделе Теги вывода речи.

 

 




