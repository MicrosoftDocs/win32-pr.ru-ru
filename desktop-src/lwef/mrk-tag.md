---
title: Тег МРК
description: Тег МРК
ms.assetid: 1bc04853-f919-4f6f-90c2-21ac836bb1e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 805a66b9ce5863bda7b7b95317bcab9cf1d80f32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776046"
---
# <a name="mrk-tag"></a>Тег МРК

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Определяет закладку в речевом тексте.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**\\МРК =***число***\\**



| Отделение     | Описание                                        |
|----------|----------------------------------------------------|
| *number* | Длинное целочисленное значение, идентифицирующее закладку. |



 

</dd> </dl>

### <a name="remarks"></a>Комментарии

Когда сервер обрабатывает закладку, он создает событие закладки. Необходимо указать число больше нуля (0) и не равно 2147483647 или 2147483646.

 

 




