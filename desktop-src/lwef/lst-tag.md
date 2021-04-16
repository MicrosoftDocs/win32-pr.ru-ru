---
title: Тег LST
description: Тег LST
ms.assetid: 82246675-9aa1-4603-a8f7-a5fd7b3f6be2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf13da7bf0267941939ec22c12706ed8c75c27e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532132"
---
# <a name="lst-tag"></a>Тег LST

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Повторяет последнюю произнесенную инструкцию для символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

\\**LST**\\

</dd> </dl>

### <a name="remarks"></a>Комментарии

Этот тег позволяет символу повторять последнюю произнесенную инструкцию. Этот тег должен располагаться в методе [**говорите**](speak-method.md) . никакой другой текст или параметры не могут быть добавлены. При повторении речевого текста все остальные теги, включенные в исходный текст, повторяются, за исключением закладок. Всеми. WAV и. Файлы ЛВВ, содержащиеся в тексте, также повторяются.

 

 




