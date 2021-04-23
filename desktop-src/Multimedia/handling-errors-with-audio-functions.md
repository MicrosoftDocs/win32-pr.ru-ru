---
title: Обработка ошибок с помощью звуковых функций
description: Обработка ошибок с помощью звуковых функций
ms.assetid: 76f132f1-61dc-4bfc-9e4a-7c841a487794
keywords:
- мультимедийные аудио, волны, ошибки
- аудио, звуковые ошибки волны
- мультимедийные аудио, вспомогательные звуковые ошибки
- звук, вспомогательные ошибки аудио
- звуковая волна, ошибки
- Вспомогательные аудио, ошибки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfcc803ae741635b3b29fb9909f530fe041e477a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337009"
---
# <a name="handling-errors-with-audio-functions"></a><span data-ttu-id="805ca-109">Обработка ошибок с помощью звуковых функций</span><span class="sxs-lookup"><span data-stu-id="805ca-109">Handling Errors with Audio Functions</span></span>

<span data-ttu-id="805ca-110">Функции аудио-и вспомогательного аудио при возникновении ошибки возвращают ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="805ca-110">The waveform-audio and auxiliary-audio functions return a nonzero value when an error occurs.</span></span> <span data-ttu-id="805ca-111">Windows предоставляет функции, которые преобразуют эти значения ошибок в текстовые описания ошибок.</span><span class="sxs-lookup"><span data-stu-id="805ca-111">Windows provides functions that convert these error values into textual descriptions of the errors.</span></span> <span data-ttu-id="805ca-112">Приложение по-прежнему должно проверять значения ошибок, чтобы определить, как продолжать работу, но текстовые описания ошибок можно использовать в диалоговых окнах, описывающих ошибки для пользователей.</span><span class="sxs-lookup"><span data-stu-id="805ca-112">The application must still examine the error values to determine how to proceed, but textual descriptions of errors can be used in dialog boxes that describe errors to users.</span></span>

<span data-ttu-id="805ca-113">Для получения текстовых описаний значений ошибок звука можно использовать следующие функции:</span><span class="sxs-lookup"><span data-stu-id="805ca-113">You can use the following functions to retrieve textual descriptions of audio error values:</span></span>



| <span data-ttu-id="805ca-114">Функция</span><span class="sxs-lookup"><span data-stu-id="805ca-114">Function</span></span>                                           | <span data-ttu-id="805ca-115">Описание</span><span class="sxs-lookup"><span data-stu-id="805ca-115">Description</span></span>                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="805ca-116">**вавеинжетеррортекст**</span><span class="sxs-lookup"><span data-stu-id="805ca-116">**waveInGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)   | <span data-ttu-id="805ca-117">Получает текстовое описание указанной ошибки ввода аудио-сигнала.</span><span class="sxs-lookup"><span data-stu-id="805ca-117">Retrieves a textual description of a specified waveform-audio input error.</span></span>  |
| [<span data-ttu-id="805ca-118">**вавеаутжетеррортекст**</span><span class="sxs-lookup"><span data-stu-id="805ca-118">**waveOutGetErrorText**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext) | <span data-ttu-id="805ca-119">Получает текстовое описание указанной ошибки вывода звуковой волны.</span><span class="sxs-lookup"><span data-stu-id="805ca-119">Retrieves a textual description of a specified waveform-audio output error.</span></span> |



 

<span data-ttu-id="805ca-120">Единственными звуковыми функциями, не возвращающими значения ошибок, являются [**ауксжетнумдевс**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**вавеинжетнумдевс**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)и [**вавеаутжетнумдевс**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs).</span><span class="sxs-lookup"><span data-stu-id="805ca-120">The only audio functions that do not return error values are [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs), and [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs).</span></span> <span data-ttu-id="805ca-121">Эти функции возвращают нуль, если в системе нет устройств или если они столкнулись с ошибками.</span><span class="sxs-lookup"><span data-stu-id="805ca-121">These functions return zero if no devices are present in a system or if they encounter any errors.</span></span>

 

 