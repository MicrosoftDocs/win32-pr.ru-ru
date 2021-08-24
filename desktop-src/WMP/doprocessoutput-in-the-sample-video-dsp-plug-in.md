---
title: Допроцессаутпут в примере подключаемого модуля DSP видео
description: Допроцессаутпут в примере подключаемого модуля DSP видео
ms.assetid: 67536e35-a049-49c8-bd89-fad1fab37e6c
keywords:
- подключаемые модули проигрыватель Windows Media, DSP видео
- подключаемые модули, DSP видео
- подключаемые модули обработки цифровых сигналов, Допроцессаутпут
- Подключаемые модули DSP, Допроцессаутпут
- подключаемые модули DSP видео, Допроцессаутпут
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b031ecddc4f7a1e4a83d4f8a7d8db3b975957789d7f887bf8b12438407624205
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680604"
---
# <a name="doprocessoutput-in-the-sample-video-dsp-plug-in"></a>Допроцессаутпут в примере подключаемого модуля DSP видео

Так как подключаемый модуль DSP видео обычно поддерживает несколько форматов видео, удобно разделить код реализации обработки на отдельную функцию для каждого формата. Это означает, что реализация **допроцессаутпут** для подключаемых модулей DSP видео относительно проста.

Реализация в примере подключаемого модуля сначала проверяет, включил ли пользователь подключаемый модуль. Если подключаемый модуль отключен, код копирует данные, содержащиеся во входном буфере, в выходной буфер, не изменяя его, как показано в следующем коде:


```C++
// Test whether the plug-in has been disabled by the user.
if (!m_bEnabled)
{
    // Just copy the data without changing it. You should
    // also do any necessary format conversion here.
    memcpy(pbOutputData, pbInputData, m_dwBufferSize);
    *cbBytesProcessed = m_dwBufferSize;

    return S_OK;
}

```



Если подключаемый модуль включен, код просто выполняет ряд **проверок элемента подтип входного типа носителя** , чтобы определить текущий формат видео. При обнаружении совпадения код вызывает соответствующую функцию обработки.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Реализация подключаемого модуля DSP видео**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




