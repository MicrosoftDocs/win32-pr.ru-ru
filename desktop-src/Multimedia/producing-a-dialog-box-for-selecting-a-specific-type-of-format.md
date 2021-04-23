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
ms.openlocfilehash: bfc5d73d1b03f22923e6001d65898c05e2bd853e
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/27/2020
ms.locfileid: "104336540"
---
# <a name="producing-a-dialog-box-for-selecting-a-specific-type-of-format"></a><span data-ttu-id="e184e-112">Создание диалогового окна для выбора определенного типа формата</span><span class="sxs-lookup"><span data-stu-id="e184e-112">Producing a Dialog Box for Selecting a Specific Type of Format</span></span>

<span data-ttu-id="e184e-113">Может потребоваться, чтобы приложение позволяло пользователю выбирать формат из ограниченного списка форматов в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="e184e-113">You might want an application to allow the user to select a format from a restricted list of formats in a dialog box.</span></span> <span data-ttu-id="e184e-114">Ограничения могут ограничивать количество каналов, частоту выборки, тег формата звуковой волны или количество битов на выборку.</span><span class="sxs-lookup"><span data-stu-id="e184e-114">Restrictions might limit the number of channels, the sampling rate, the waveform-audio format tag, or the number of bits per sample.</span></span> <span data-ttu-id="e184e-115">Во всех этих случаях список можно создать с помощью функции [**акмформатчусе**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , задав элементы **фдвенум** и **пвфксенум** структуры [**акмформатчусе**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) .</span><span class="sxs-lookup"><span data-stu-id="e184e-115">In all of these cases, you can generate the list by using the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, setting the **fdwEnum** and **pwfxEnum** members of the [**ACMFORMATCHOOSE**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) structure.</span></span> <span data-ttu-id="e184e-116">Этот процесс показан в приведенном ниже примере.</span><span class="sxs-lookup"><span data-stu-id="e184e-116">The following example illustrates this process.</span></span>


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



 

 




