---
title: Создание диалогового окна для выбора формата записи
description: Создание диалогового окна для выбора формата записи
ms.assetid: e94ca8da-4ee6-4362-a144-27b86f2cadac
keywords:
- Диспетчер аудиосжатия (ACM), создание диалоговых окон
- ACM (диспетчер аудиосжатия), создание диалоговых окон
- Примеры ACM, создание диалоговых окон
- Создание диалоговых окон
- Функция Акмформатчусе
- Диспетчер аудиосжатия (ACM), выбор формата для перекодирования
- ACM (диспетчер аудиосжатия), выбор формата для перекодирования
- Примеры ACM, выбор формата для перекодирования
- Выбор формата для перекодирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7584d5f56904a6aa5241930041bf89c10373f6b1
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/27/2020
ms.locfileid: "104412628"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-recording"></a><span data-ttu-id="edb7d-112">Создание диалогового окна для выбора формата записи</span><span class="sxs-lookup"><span data-stu-id="edb7d-112">Producing a Dialog Box for Selecting a Format for Recording</span></span>

<span data-ttu-id="edb7d-113">Приложение может предоставить пользователю возможность выбрать формат, для которого устройство аудио аудио поддерживает встроенную поддержку.</span><span class="sxs-lookup"><span data-stu-id="edb7d-113">An application can allow the user to select a format for which an installed waveform-audio device provides native support.</span></span> <span data-ttu-id="edb7d-114">Например, вам может потребоваться, чтобы в редакторе аудио-аудио были записаны новые данные звуковой волны без использования ACM сжатия или декомпрессора для обеспечения слоя перевода.</span><span class="sxs-lookup"><span data-stu-id="edb7d-114">For example, you might want a waveform-audio editor to record new waveform-audio data without using an ACM compressor or decompressor to provide a translation layer.</span></span> <span data-ttu-id="edb7d-115">Для этого используйте функцию [**акмформатчусе**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , указав \_ \_ Флаги ACM форматенумф Hardware и ACM \_ форматенумф \_ input в **фдвенум** в структуре [**акмформатчусе**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) .</span><span class="sxs-lookup"><span data-stu-id="edb7d-115">To do this, use the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, specifying the ACM\_FORMATENUMF\_HARDWARE and ACM\_FORMATENUMF\_INPUT flags in the **fdwEnum** member of the [**ACMFORMATCHOOSE**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) structure.</span></span>

 

 




