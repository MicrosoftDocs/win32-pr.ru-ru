---
title: Обработка ошибок с помощью функций MIDI
description: Обработка ошибок с помощью функций MIDI
ms.assetid: 7ea5db5e-34d7-4506-8157-c24adf5bcdda
keywords:
- Цифровой интерфейс музыкальных инструментов (MIDI), ошибки
- MIDI (цифровой интерфейс музыкального инструмента), ошибки
- Службы MIDI, ошибки
- Ошибки MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9689fe30b9c4f598cfc9bea892ff3d4fe15d3a9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105650354"
---
# <a name="handling-errors-with-midi-functions"></a><span data-ttu-id="091c5-107">Обработка ошибок с помощью функций MIDI</span><span class="sxs-lookup"><span data-stu-id="091c5-107">Handling Errors with MIDI Functions</span></span>

<span data-ttu-id="091c5-108">Функции аудио MIDI возвращают ненулевой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="091c5-108">MIDI audio functions return a nonzero error code.</span></span> <span data-ttu-id="091c5-109">Для ошибок, связанных с MIDI, функции [**мидиинжетеррортекст**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) и [**мидиаутжетеррортекст**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) извлекают текстовые описания кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="091c5-109">For MIDI-associated errors, the [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) and [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) functions retrieve textual descriptions for the error codes.</span></span> <span data-ttu-id="091c5-110">Приложение должно по-прежнему просматривать значение ошибки, чтобы определить, как это можно сделать, но оно может использовать описания ошибок в диалоговых окнах для информирования пользователей об условиях ошибки.</span><span class="sxs-lookup"><span data-stu-id="091c5-110">The application must still look at the error value itself to determine how to proceed, but it can use the error descriptions in dialog boxes to inform users of the error conditions.</span></span>

<span data-ttu-id="091c5-111">Единственными функциями MIDI, которые не возвращают коды ошибок, являются функции [**мидиинжетнумдевс**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) и [**мидиаутжетнумдевс**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) .</span><span class="sxs-lookup"><span data-stu-id="091c5-111">The only MIDI functions that do not return error codes are the [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) and [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) functions.</span></span> <span data-ttu-id="091c5-112">Эти функции возвращают нулевое значение, если в системе нет устройств или если какая-либо ошибка обнаружена функцией.</span><span class="sxs-lookup"><span data-stu-id="091c5-112">These functions return a value of zero if no devices are present in a system or if any errors are encountered by the function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="091c5-113">См. также</span><span class="sxs-lookup"><span data-stu-id="091c5-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="091c5-114">Службы MIDI</span><span class="sxs-lookup"><span data-stu-id="091c5-114">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 