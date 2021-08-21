---
title: Хасосерклиентс, свойство
description: Хасосерклиентс, свойство
ms.assetid: 5ecc6f42-786b-40a6-8800-9ad0d92edfb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf7bb91240ade815c00fb2e36adf1466dcb30ba4240be038342906be49e6ff2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479009"
---
# <a name="hasotherclients-property"></a>Хасосерклиентс, свойство

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает значение, указывающее, используется ли указанный символ другими приложениями.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент*. **Символы ("**_чарактерид_*_"). Хасосерклиентс_*



| Значение     | Описание                                |
|-----------|--------------------------------------------|
| **True**  | Этот символ содержит другие клиенты.           |
| **False** | Этот символ не содержит других клиентов. |



 

</dd> </dl>

## <a name="remarks"></a>Remarks

Это свойство можно использовать для определения того, является ли приложение единственным или последним клиентом символа, когда несколько приложений совместно используют один и тот же символ.

 

 




