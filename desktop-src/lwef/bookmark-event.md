---
title: Событие закладки
description: Событие закладки
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0695ccd04f93eae46eaae66955c84fefb9e0c963
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253111"
---
# <a name="bookmark-event"></a>Событие закладки

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возникает при активации закладки в текстовой строке в речевом коде, заданной приложением.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

 Закладка подпрограммы- *агента* \_  **(ByVal** *букмаркид * *)**



| Отделение         | Описание                                     |
|--------------|-------------------------------------------------|
| *BookmarkID* | Длинное целое число, определяющее номер закладки. |



 

</dd> </dl>

### <a name="remarks"></a>Комментарии

Чтобы указать событие закладки, используйте метод [**говорите**](speak-method.md) с тегом **МРК** в заданном тексте. Дополнительные сведения о тегах см. в разделе Теги вывода речи.

 

 




