---
title: Формат буфера потока
description: Формат буфера потока
ms.assetid: 4b24c12e-b43f-492e-a000-af4f59d5e16f
keywords:
- Цифровой интерфейс музыкальных инструментов (MIDI), буферы потоков
- MIDI (цифровой интерфейс музыкального инструмента), буферы потоков
- буферы потоков, формат
- Структура МИДИХДР
- Структура МИДИЕВЕНТ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a7f0dbeabd0d7aebeae0387af415a831e4658
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412791"
---
# <a name="stream-buffer-format"></a><span data-ttu-id="c6907-108">Формат буфера потока</span><span class="sxs-lookup"><span data-stu-id="c6907-108">Stream Buffer Format</span></span>

<span data-ttu-id="c6907-109">Элемент **лпдата** структуры [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) указывает на буфер потока, а элемент **двбуфферленгс** указывает фактический размер этого буфера.</span><span class="sxs-lookup"><span data-stu-id="c6907-109">The **lpData** member of the [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure points to a stream buffer, and the **dwBufferLength** member specifies the actual size of this buffer.</span></span> <span data-ttu-id="c6907-110">Член **двбитесрекордед** параметра **мидихдр** указывает число байтов в буфере, которые фактически используются событиями MIDI; Это значение должно быть меньше или равно значению, заданному параметром **двбуфферленгс**.</span><span class="sxs-lookup"><span data-stu-id="c6907-110">The **dwBytesRecorded** member of **MIDIHDR** specifies the number of bytes in the buffer that are actually used by the MIDI events; this value must be less than or equal to the value specified by **dwBufferLength**.</span></span>

<span data-ttu-id="c6907-111">Каждое событие MIDI в буфере потока определяется структурой [**мидиевент**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) , которая содержит время события, идентификатор потока, код события и, при необходимости, параметры для события.</span><span class="sxs-lookup"><span data-stu-id="c6907-111">Each of the MIDI events in the stream buffer is specified by a [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) structure, which contains the time for the event, a stream identifier, an event code, and, when appropriate, parameters for the event.</span></span> <span data-ttu-id="c6907-112">Каждая из этих структур **мидиевент** должна начинаться на границе даублеворд.</span><span class="sxs-lookup"><span data-stu-id="c6907-112">Each of these **MIDIEVENT** structures must begin on a doubleword boundary.</span></span> <span data-ttu-id="c6907-113">При необходимости необходимо добавить в конец структуры байты для заполнения, чтобы следующий элемент начинался на границе даублеворд.</span><span class="sxs-lookup"><span data-stu-id="c6907-113">If necessary, pad bytes must be added to the end of the structure to ensure that the next one starts on a doubleword boundary.</span></span>

 

 