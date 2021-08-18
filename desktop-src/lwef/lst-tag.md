---
title: Тег LST
description: Тег LST
ms.assetid: 82246675-9aa1-4603-a8f7-a5fd7b3f6be2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad70173ef3919ae2291204745f727961165a83f4f0fad0ad310003b997a5565e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114594"
---
# <a name="lst-tag"></a>Тег LST

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**
</dt> <dd>

Повторяет последнюю произнесенную инструкцию для символа.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

\\**LST**\\

</dd> </dl>

### <a name="remarks"></a>Remarks

Этот тег позволяет символу повторять последнюю произнесенную инструкцию. Этот тег должен располагаться в методе [**говорите**](speak-method.md) . никакой другой текст или параметры не могут быть добавлены. При повторении речевого текста все остальные теги, включенные в исходный текст, повторяются, за исключением закладок. Всеми. WAV и. Файлы ЛВВ, содержащиеся в тексте, также повторяются.

 

 




