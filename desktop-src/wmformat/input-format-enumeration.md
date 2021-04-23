---
title: Перечисление формата входных данных
description: Перечисление формата входных данных
ms.assetid: 75264598-0226-435a-b71f-6997ff0fcaff
keywords:
- Windows Media Format SDK, перечисления входных форматов
- Windows Media Format SDK, перечисление входных форматов
- Расширенные системные форматы (ASF), перечисления входного формата
- ASF (Расширенный системный формат), перечисления входного формата
- Расширенный системный формат (ASF), перечисление входных форматов
- ASF (Расширенный системный формат), перечисление входных форматов
- перечисления входного формата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e853aeeac5ca470f1b33b611b287cba8fa025dc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487009"
---
# <a name="input-format-enumeration"></a><span data-ttu-id="aec32-110">Перечисление формата входных данных</span><span class="sxs-lookup"><span data-stu-id="aec32-110">Input Format Enumeration</span></span>

<span data-ttu-id="aec32-111">Объект модуля записи получает сведения о форматировании потока из профиля, который вы его предоставляет.</span><span class="sxs-lookup"><span data-stu-id="aec32-111">The writer object gets stream format information from the profile you give it.</span></span> <span data-ttu-id="aec32-112">Сведения о конфигурации потока в профиле предоставляют средству записи все необходимые сведения о том, как данные записываются в файл.</span><span class="sxs-lookup"><span data-stu-id="aec32-112">Stream configuration information in a profile gives the writer all of the information it needs about how the data is to be written in the file.</span></span> <span data-ttu-id="aec32-113">Профиль не предоставляет средству записи никаких сведений о формате входных образцов, которые предоставляет ваше приложение.</span><span class="sxs-lookup"><span data-stu-id="aec32-113">The profile does not provide the writer with any information about the format of the input samples that your application delivers.</span></span> <span data-ttu-id="aec32-114">Форматы входных данных будут неизвестны только для потоков, сжатых с помощью одного из кодеков Windows Media. входные данные для произвольных типов потоков являются прогнозируемыми на основе информации в профиле.</span><span class="sxs-lookup"><span data-stu-id="aec32-114">Input formats will be unknown only for streams compressed with one of the Windows Media codecs; inputs for arbitrary stream types are predictable based on the information in the profile.</span></span>

<span data-ttu-id="aec32-115">Объект модуля записи может взаимодействовать с кодеком для потока, чтобы определить типы входных данных, которые можно использовать.</span><span class="sxs-lookup"><span data-stu-id="aec32-115">The writer object can communicate with the codec for a stream to determine the input types that can be used.</span></span> <span data-ttu-id="aec32-116">Предоставляются методы для перечисления возможных типов входных данных.</span><span class="sxs-lookup"><span data-stu-id="aec32-116">Methods are provided to enumerate the possible input types.</span></span> <span data-ttu-id="aec32-117">Всегда следует нахождение входного типа, соответствующего входному носителю, путем перечисления поддерживаемых типов вместо ручного задания свойств входного носителя.</span><span class="sxs-lookup"><span data-stu-id="aec32-117">You should always find the input type that matches your input media by enumerating the supported types rather than setting the input media properties manually.</span></span> <span data-ttu-id="aec32-118">Дополнительные сведения см. [в разделе Перечисление входных форматов](to-enumerate-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="aec32-118">For more information, see [To Enumerate Input Formats](to-enumerate-input-formats.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aec32-119">См. также</span><span class="sxs-lookup"><span data-stu-id="aec32-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aec32-120">**Функции записи файлов**</span><span class="sxs-lookup"><span data-stu-id="aec32-120">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="aec32-121">**Работа с входными данными**</span><span class="sxs-lookup"><span data-stu-id="aec32-121">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




