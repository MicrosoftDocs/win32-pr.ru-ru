---
title: Работа с входными данными
description: Работа с входными данными
ms.assetid: 72daa7ca-4264-46bf-91ac-8b95fdbfd41c
keywords:
- Windows Media Format SDK, работа с входными данными
- Расширенный формат систем (ASF), работа с входными данными
- ASF (Расширенный системный формат), работа с входными данными
- профили, работа с входными данными
- потоки, работа с входными данными
- кодеки, работа с входными данными
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e7016b5304b0d77e130b68d9a9feef15ffe54d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486720"
---
# <a name="working-with-inputs"></a><span data-ttu-id="c5d74-109">Работа с входными данными</span><span class="sxs-lookup"><span data-stu-id="c5d74-109">Working with Inputs</span></span>

<span data-ttu-id="c5d74-110">Так же, как правильная конфигурация потока в профиле требуется для сжатия потока, необходимо также убедиться, что тип несжатого носителя, передаваемый в модуль записи, описывается точно.</span><span class="sxs-lookup"><span data-stu-id="c5d74-110">Just as the proper stream configuration in the profile is required to get the codec to compress a stream, you must also ensure that the type of uncompressed media you pass to the writer is accurately described.</span></span> <span data-ttu-id="c5d74-111">Каждый кодек Windows Media имеет связанный тип ввода по умолчанию, но поддерживаются несколько типов входных данных.</span><span class="sxs-lookup"><span data-stu-id="c5d74-111">Every Windows Media codec has an associated default input type, but several input types are supported.</span></span> <span data-ttu-id="c5d74-112">Вы можете проверить Поддерживаемые входные данные и выбрать один из них, соответствующий вашим данным.</span><span class="sxs-lookup"><span data-stu-id="c5d74-112">You can examine the supported inputs and select the one that matches your data.</span></span> <span data-ttu-id="c5d74-113">Процесс работы с входными данными приводится в следующих шагах.</span><span class="sxs-lookup"><span data-stu-id="c5d74-113">The process of working with inputs is summarized in the following steps:</span></span>

1.  <span data-ttu-id="c5d74-114">Когда вы загружаете профиль для использования модулем записи, объект модуля записи назначает входной номер для каждого соединения в профиле.</span><span class="sxs-lookup"><span data-stu-id="c5d74-114">When you load a profile for the writer to use, the writer object assigns an input number for each connection in the profile.</span></span> <span data-ttu-id="c5d74-115">Дополнительные сведения о загрузке профилей для модуля записи см. [в разделе Использование профилей с модулем записи](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="c5d74-115">For more information about loading profiles for the writer, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span> <span data-ttu-id="c5d74-116">Если вы не используете взаимное исключение с помощью битовой скорости, для каждого потока существует одно соединение.</span><span class="sxs-lookup"><span data-stu-id="c5d74-116">Unless you are using mutual exclusion by bit rate, there is one connection for each stream.</span></span> <span data-ttu-id="c5d74-117">Потоки, которые являются взаимоисключающими по скорости потока, совместно используют одно соединение.</span><span class="sxs-lookup"><span data-stu-id="c5d74-117">Streams that are mutually exclusive by bit rate share a single connection.</span></span>
2.  <span data-ttu-id="c5d74-118">Приложение должно указать входные номера для файла.</span><span class="sxs-lookup"><span data-stu-id="c5d74-118">Your application should identify the input numbers for the file.</span></span> <span data-ttu-id="c5d74-119">Дополнительные сведения об идентификации входных номеров см. [в разделе Определение входных данных по номеру](to-identify-inputs-by-number.md).</span><span class="sxs-lookup"><span data-stu-id="c5d74-119">For more information about identifying input numbers, see [To Identify Inputs By Number](to-identify-inputs-by-number.md).</span></span>
3.  <span data-ttu-id="c5d74-120">Для каждого входа необходимо убедиться, что входной формат соответствует вашим данным.</span><span class="sxs-lookup"><span data-stu-id="c5d74-120">For each input, you should ensure that the input format matches your data.</span></span> <span data-ttu-id="c5d74-121">Можно перечислить входные форматы, поддерживаемые пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="c5d74-121">You can enumerate the input formats supported by the SDK.</span></span> <span data-ttu-id="c5d74-122">Дополнительные сведения см. [в разделе Перечисление входных форматов](to-enumerate-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="c5d74-122">For more information, see [To Enumerate Input Formats](to-enumerate-input-formats.md).</span></span> <span data-ttu-id="c5d74-123">Нельзя перечислить входные форматы произвольных потоков или потоков, которые уже сжаты.</span><span class="sxs-lookup"><span data-stu-id="c5d74-123">You cannot enumerate the input formats of arbitrary streams or streams that are already compressed.</span></span> <span data-ttu-id="c5d74-124">Дополнительные сведения об этих особых случаях см. в разделе [случайные и предварительно сжатые входные потоки](arbitrary-and-precompressed-stream-inputs.md).</span><span class="sxs-lookup"><span data-stu-id="c5d74-124">For more information about these special cases, see [Arbitrary and Precompressed Stream Inputs](arbitrary-and-precompressed-stream-inputs.md).</span></span>
4.  <span data-ttu-id="c5d74-125">Назначьте правильный формат входных данных для каждого соединения.</span><span class="sxs-lookup"><span data-stu-id="c5d74-125">Assign the correct input format for each connection.</span></span> <span data-ttu-id="c5d74-126">Дополнительные сведения см. в разделе [Назначение входных форматов](assigning-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="c5d74-126">For more information, see [Assigning Input Formats](assigning-input-formats.md).</span></span>
5.  <span data-ttu-id="c5d74-127">Некоторые функции кодеков и модулей записи настраиваются во время кодирования, а не в профиле.</span><span class="sxs-lookup"><span data-stu-id="c5d74-127">Some codec and writer features are configured at encoding time instead of in the profile.</span></span> <span data-ttu-id="c5d74-128">Для настройки этих функций необходимо использовать входные параметры.</span><span class="sxs-lookup"><span data-stu-id="c5d74-128">To configure these features, you must use input settings.</span></span> <span data-ttu-id="c5d74-129">Дополнительные сведения см. [в разделе Настройка входных параметров](to-set-input-settings.md).</span><span class="sxs-lookup"><span data-stu-id="c5d74-129">For more information, see [To Set Input Settings](to-set-input-settings.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5d74-130">См. также</span><span class="sxs-lookup"><span data-stu-id="c5d74-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5d74-131">**Запись файлов ASF**</span><span class="sxs-lookup"><span data-stu-id="c5d74-131">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




