---
title: Использование функции обратного вызова для обработки сообщений драйвера
description: Использование функции обратного вызова для обработки сообщений драйвера
ms.assetid: 7fef400f-5040-4d33-9a2f-bb12aa9369e0
keywords:
- звуковая волна, функции обратного вызова
- блоки звуковых данных, функции обратного вызова
- звуковая волна, обработка сообщений драйвера
- блоки звуковых данных, обработка сообщений драйверов
- Обработка сообщений драйвера
- Функция Вавеинопен
- Функция Вавеаутопен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3e7541a00b43b5fb2267a17d4de8bb017823c3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105661711"
---
# <a name="using-a-callback-function-to-process-driver-messages"></a><span data-ttu-id="17d67-110">Использование функции обратного вызова для обработки сообщений драйвера</span><span class="sxs-lookup"><span data-stu-id="17d67-110">Using a Callback Function to Process Driver Messages</span></span>

<span data-ttu-id="17d67-111">Вы можете написать собственную функцию обратного вызова для обработки сообщений, отправленных драйвером устройства.</span><span class="sxs-lookup"><span data-stu-id="17d67-111">You can write your own callback function to process messages sent by the device driver.</span></span> <span data-ttu-id="17d67-112">Чтобы использовать функцию обратного вызова, укажите флаг функции ОБРАТНОго вызова \_ в параметре *фдвопен* и адрес обратного вызова в параметре *Двкаллбакк* функции [**вавеинопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) или [**вавеаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) .</span><span class="sxs-lookup"><span data-stu-id="17d67-112">To use a callback function, specify the CALLBACK\_FUNCTION flag in the *fdwOpen* parameter and the address of the callback in the *dwCallback* parameter of the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) or [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function.</span></span>

<span data-ttu-id="17d67-113">Сообщения, отправленные в функцию обратного вызова, похожи на сообщения, отправленные в окно, за исключением того, что они имеют два параметра **типа DWORD** вместо параметров **uint** и **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="17d67-113">Messages sent to a callback function are similar to messages sent to a window, except they have two **DWORD** parameters instead of a **UINT** and a **DWORD** parameter.</span></span> <span data-ttu-id="17d67-114">Дополнительные сведения об этих сообщениях см. в разделе [воспроизведение Waveform-Audio файлов](playing-waveform-audio-files.md).</span><span class="sxs-lookup"><span data-stu-id="17d67-114">For details on these messages, see [Playing Waveform-Audio Files](playing-waveform-audio-files.md).</span></span>

<span data-ttu-id="17d67-115">Чтобы передать данные экземпляра из приложения в функцию обратного вызова, используйте один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="17d67-115">To pass instance data from an application to a callback function, use one of the following techniques:</span></span>

-   <span data-ttu-id="17d67-116">Передайте данные экземпляра с помощью параметра *двинстанце* функции, которая открывает драйвер устройства.</span><span class="sxs-lookup"><span data-stu-id="17d67-116">Pass the instance data using the *dwInstance* parameter of the function that opens the device driver.</span></span>
-   <span data-ttu-id="17d67-117">Передайте данные экземпляра с помощью элемента **двусер** структуры [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) , определяющего блок звуковых данных, отправляемый в драйвер устройства.</span><span class="sxs-lookup"><span data-stu-id="17d67-117">Pass the instance data using the **dwUser** member of the [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure that identifies an audio data block being sent to a device driver.</span></span>

<span data-ttu-id="17d67-118">Если требуется более 32 бит данных экземпляра, передайте указатель в структуру, содержащую дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="17d67-118">If you need more than 32 bits of instance data, pass a pointer to a structure containing the additional information.</span></span>

 

 