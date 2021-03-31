---
title: Тег Vol
description: Тег Vol
ms.assetid: a6444eb2-79c2-4c86-8474-846d908479df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7979278b2eb89c352b9e53f6141cb585fb0ed134
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067528"
---
# <a name="vol-tag"></a>Тег Vol

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Задает уровень громкости, на котором наводится речь.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**\\Vol =***номер***\\**



| Отделение     | Описание                                                         |
|----------|---------------------------------------------------------------------|
| *number* | Том с базовой назначением: 0 — это тишина, а 65535 — максимальный том. |



 

</dd> </dl>

### <a name="remarks"></a>Комментарии

Параметр Volume влияет как на левый, так и на правый канал. Вы не можете задать громкость каждого канала отдельно. Этот тег поддерживается только для выходных данных, созданных системой TTS.

 

 




