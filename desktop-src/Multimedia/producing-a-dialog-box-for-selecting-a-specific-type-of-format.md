---
title: Создание диалогового окна для выбора определенного типа формата
description: Создание диалогового окна для выбора определенного типа формата
ms.assetid: e454f9d6-5cbf-4e1b-937e-771cf1dd38ba
keywords:
- Диспетчер аудиосжатия (ACM), создание диалоговых окон
- ACM (диспетчер аудиосжатия), создание диалоговых окон
- Примеры ACM, создание диалоговых окон
- Создание диалоговых окон
- Функция Акмформатчусе
- Диспетчер аудиосжатия (ACM), выбор типов форматов
- ACM (диспетчер аудиосжатия), выбор типов форматов
- Примеры ACM, выбор типов форматов
- Выбор типов форматов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f25f7b196fcb9462a3b61dd8e351ed75276c7df7bf46cec233dd8eac7deda5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037654"
---
# <a name="producing-a-dialog-box-for-selecting-a-specific-type-of-format"></a>Создание диалогового окна для выбора определенного типа формата

Может потребоваться, чтобы приложение позволяло пользователю выбирать формат из ограниченного списка форматов в диалоговом окне. Ограничения могут ограничивать количество каналов, частоту выборки, тег формата звуковой волны или количество битов на выборку. Во всех этих случаях список можно создать с помощью функции [**акмформатчусе**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , задав элементы **фдвенум** и **пвфксенум** структуры [**акмформатчусе**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) . Этот процесс показан в приведенном ниже примере.


```C++
MMRESULT            mmr; 
ACMFORMATCHOOSE     afc; 
WAVEFORMATEX        wfxSelection; 
WAVEFORMATEX        wfxEnum; 
 
// Initialize the ACMFORMATCHOOSE members. 
memset(&afc, 0, sizeof(afc)); 
 
afc.cbStruct    = sizeof(afc); 
afc.fdwStyle    = 0L;               // no special style flags 
afc.hwndOwner   = hwnd;             // hwnd of parent window 
afc.pwfx        = &wfxSelection;    // wfx to receive selection 
afc.cbwfx       = sizeof(wfxSelection); 
afc.pszTitle    = TEXT("16 Bit PCM Selection"); 
 
//  Request that all 16-bit PCM formats be displayed for the user 
//  to select from. 
memset(&wfxEnum, 0, sizeof(wfxEnum)); 
wfxEnum.wFormatTag = WAVE_FORMAT_PCM; 
wfxEnum.wBitsPerSample = 16; 
afc.fdwEnum = ACM_FORMATENUMF_WFORMATTAG | 
    ACM_FORMATENUMF_WBITSPERSAMPLE; 
afc.pwfxEnum = &wfxEnum; 
mmr = acmFormatChoose(&afc); 
if ((MMSYSERR_NOERROR != mmr) && (ACMERR_CANCELED != mmr)) 
{ 
    // There was a fatal error in bringing up the list 
    // dialog box (probably invalid input parameters). 
} 
 
```



 

 




