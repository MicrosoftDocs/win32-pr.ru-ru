---
title: Хасосерклиентс, свойство
description: Хасосерклиентс, свойство
ms.assetid: 5ecc6f42-786b-40a6-8800-9ad0d92edfb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3434cec191d2bec93d501847df064a8dbbf3e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068004"
---
# <a name="hasotherclients-property"></a>Хасосерклиентс, свойство

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Возвращает значение, указывающее, используется ли указанный символ другими приложениями.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Агент*. **Символы ("***чарактерид***"). Хасосерклиентс**



| Значение     | Описание                                |
|-----------|--------------------------------------------|
| **True**  | Этот символ содержит другие клиенты.           |
| **False** | Этот символ не содержит других клиентов. |



 

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это свойство можно использовать для определения того, является ли приложение единственным или последним клиентом символа, когда несколько приложений совместно используют один и тот же символ.

 

 




