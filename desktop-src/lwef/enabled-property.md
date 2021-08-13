---
title: Свойство Enabled (объект всплывающего объекта)
description: Сведения о включенном свойстве всплывающего объекта. не рекомендуется использовать Microsoft Agent на Windows 7.
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d4eaa09e173d847e9dead1bbd559b59e2d12a2d40b5f1d1f989d3cf70263ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118752006"
---
# <a name="enabled-property-balloon-object"></a>Свойство Enabled (объект всплывающего объекта)

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает значение, указывающее, включено ли всплывающее сообщение для указанного символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент ***. Символы ("**_чарактерид_*_"). Всплывающее сообщение. включено_*



| Значение     | Описание              |
|-----------|--------------------------|
| **True**  | Всплывающее сообщение включено.  |
| **False** | Всплывающее сообщение отключено. |



 

</dd> </dl>

## <a name="remarks"></a>Remarks

Свойство **Enabled** возвращает логическое значение, указывающее, включено ли всплывающее сообщение. Состояние всплывающей подсказки по умолчанию задается как часть определения символа при компиляции символа в редакторе символов Microsoft Agent. Если символ определен так, что не поддерживает всплывающую подсказку, это свойство всегда будет иметь **значение false** для символа.

 

 




