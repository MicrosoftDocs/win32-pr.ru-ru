---
title: Тег Vol
description: Тег Vol
ms.assetid: a6444eb2-79c2-4c86-8474-846d908479df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097d03b7bb536ada8dc783e1506ba4bedfd54c6b5698e1aa68dfe55fd1f939d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035982"
---
# <a name="vol-tag"></a>Тег Vol

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Задает уровень громкости, на котором наводится речь.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

**\\ Vol =**_номер_*_\\_*



| Часть     | Описание                                                         |
|----------|---------------------------------------------------------------------|
| *number* | Том с базовой назначением: 0 — это тишина, а 65535 — максимальный том. |



 

</dd> </dl>

### <a name="remarks"></a>Remarks

Параметр Volume влияет как на левый, так и на правый канал. Вы не можете задать громкость каждого канала отдельно. Этот тег поддерживается только для выходных данных, созданных системой TTS.

 

 




