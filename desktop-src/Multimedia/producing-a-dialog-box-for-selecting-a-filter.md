---
title: Создание диалогового окна для выбора фильтра
description: Создание диалогового окна для выбора фильтра
ms.assetid: 4cbb9276-6ce6-4cf4-a000-2b4f9ac42b31
keywords:
- Диспетчер аудиосжатия (ACM), создание диалоговых окон
- ACM (диспетчер аудиосжатия), создание диалоговых окон
- Примеры ACM, создание диалоговых окон
- Создание диалоговых окон
- Функция Акмфилтерчусе
- Диспетчер аудиосжатия (ACM), выбор фильтров
- ACM (диспетчер аудиосжатия), выбор фильтров
- Примеры ACM, выбор фильтров
- Выбор фильтров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87225c1aebf2a06c738a1b48b03b94ed81bf6c2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672047"
---
# <a name="producing-a-dialog-box-for-selecting-a-filter"></a><span data-ttu-id="04817-112">Создание диалогового окна для выбора фильтра</span><span class="sxs-lookup"><span data-stu-id="04817-112">Producing a Dialog Box for Selecting a Filter</span></span>

<span data-ttu-id="04817-113">Приложение может позволить пользователям выбрать произвольную операцию фильтрации и применить ее к данным аудио-сигнала.</span><span class="sxs-lookup"><span data-stu-id="04817-113">An application can allow users to select an arbitrary filter operation and apply it to waveform-audio data.</span></span> <span data-ttu-id="04817-114">В следующем примере приложение выделяет буфер для хранения фильтра, а затем использует функцию [**акмфилтерчусе**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) для выбора фильтра.</span><span class="sxs-lookup"><span data-stu-id="04817-114">In the following example, the application allocates a buffer to hold the filter and then uses the [**acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) function to select the filter.</span></span> <span data-ttu-id="04817-115">Функции в этом примере должны вызываться с соответствующим фильтром или тегом фильтра.</span><span class="sxs-lookup"><span data-stu-id="04817-115">The functions in this example must be called with the appropriate filter or filter tag.</span></span>


```C++
MMRESULT        mmr; 
ACMFILTERCHOOSE afc; 
PWAVEFILTER     pwfltr; 
DWORD           cbwfltr; 
 
// Determine the maximum size required for any valid filter 
// for which the ACM has a driver installed and enabled. 
mmr = acmMetrics(NULL, ACM_METRIC_MAX_SIZE_FILTER, &cbwfltr); 
if (MMSYSERR_NOERROR != mmr) { 
 
    // The ACM probably has no drivers installed and 
    // enabled for filter operations. 
    return (mmr); 
} 
 
// Dynamically allocate a structure large enough to hold the 
// maximum sized filter enabled in the system. 
pwfltr = (PWAVEFILTER)LocalAlloc(LPTR, (UINT)cbwfltr); 
if (NULL == pwfltr) { 
    return (MMSYSERR_NOMEM); 
} 
 
// Initialize the ACMFILTERCHOOSE members. 
memset(&afc, 0, sizeof(afc)); 
 
afc.cbStruct    = sizeof(afc); 
afc.fdwStyle    = 0L;               // no special style flags 
afc.hwndOwner   = hwnd;             // hwnd of parent window 
afc.pwfltr      = pwfltr;           // wfltr to receive selection 
afc.cbwfltr     = cbwfltr;          // size of wfltr buffer 
afc.pszTitle    = TEXT("Any Filter Selection"); 
 
// Call the ACM to bring up the filter-selection dialog box. 
mmr = acmFilterChoose(&afc); 
if (MMSYSERR_NOERROR == mmr) { 
    // The user selected a valid filter. The pwfltr buffer, 
    // allocated above, contains the complete filter description. 
} 
 
// Clean up and exit. 
LocalFree((HLOCAL)pwfltr); 
return (mmr); 
 
```



 

 




