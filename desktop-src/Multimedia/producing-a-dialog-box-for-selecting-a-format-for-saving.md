---
title: Создание диалогового окна для выбора формата для сохранения
description: Создание диалогового окна для выбора формата для сохранения
ms.assetid: f833b28c-13e1-497c-bfc4-2e3bc84d7fff
keywords:
- Диспетчер аудиосжатия (ACM), создание диалоговых окон
- ACM (диспетчер аудиосжатия), создание диалоговых окон
- Примеры ACM, создание диалоговых окон
- Создание диалоговых окон
- Функция Акмформатчусе
- Диспетчер аудиосжатия (ACM), выбор формата для сохранения
- ACM (диспетчер аудиосжатия), выбор формата для сохранения
- Примеры ACM, выбор формата для сохранения
- Выбор формата для сохранения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55df4cd89a04bf1d3dd34512c4014928b6d5d4fb
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/27/2020
ms.locfileid: "104412629"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-saving"></a><span data-ttu-id="10dc0-112">Создание диалогового окна для выбора формата для сохранения</span><span class="sxs-lookup"><span data-stu-id="10dc0-112">Producing a Dialog Box for Selecting a Format for Saving</span></span>

<span data-ttu-id="10dc0-113">Может потребоваться, чтобы приложение сохраняло существующие звуковые данные аудио-сигнала в другом формате.</span><span class="sxs-lookup"><span data-stu-id="10dc0-113">You might want an application to save existing waveform-audio data in another format.</span></span> <span data-ttu-id="10dc0-114">Например, редактор аудио-файлов может сохранить аудио-файл в виде сжатого файла.</span><span class="sxs-lookup"><span data-stu-id="10dc0-114">For example, a waveform-audio editor could save a waveform-audio file as a compressed file.</span></span> <span data-ttu-id="10dc0-115">Чтобы вывести только предложенные форматы назначения для указанного формата источника в диалоговом окне, созданном функцией [**акмформатчусе**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , укажите формат источника в элементе **ПВФКСЕНУМ** и \_ флаг ACM Форматенумф \_ в элементе **фдвенум** структуры [**акмформатчусе**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) .</span><span class="sxs-lookup"><span data-stu-id="10dc0-115">To list only the suggested destination formats for a specified source format in the dialog box created by the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, specify the source format in the **pwfxEnum** member and the ACM\_FORMATENUMF\_SUGGEST flag in the **fdwEnum** member of the [**ACMFORMATCHOOSE**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) structure.</span></span>

<span data-ttu-id="10dc0-116">Аналогичным образом, чтобы вывести список допустимых форматов назначения для указанного формата, \_ Используйте \_ флаг ACM форматенумф CONVERT вместо \_ флага ACM форматенумф \_ предлагаю.</span><span class="sxs-lookup"><span data-stu-id="10dc0-116">Similarly, to list valid destination formats for a specified format, use the ACM\_FORMATENUMF\_CONVERT flag instead of the ACM\_FORMATENUMF\_SUGGEST flag.</span></span>

 

 




