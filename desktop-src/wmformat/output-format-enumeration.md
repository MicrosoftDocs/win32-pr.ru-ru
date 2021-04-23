---
title: Перечисление формата вывода
description: Перечисление формата вывода
ms.assetid: 53d5724b-f875-4b2e-92fa-279f46111f29
keywords:
- Windows Media Format SDK, перечисления формата вывода
- Расширенные системные форматы (ASF), перечисления формата вывода
- ASF (Расширенный системный формат), перечисления формата вывода
- Windows Media Format SDK, интерфейс Ивмреадертипенеготиатион
- Расширенный системный формат (ASF), интерфейс Ивмреадертипенеготиатион
- ASF (Расширенный системный формат), интерфейс Ивмреадертипенеготиатион
- перечисления формата вывода
- ивмреадертипенеготиатион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d49999c3da2afd05b0d2231d259d24a50356eb4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069522"
---
# <a name="output-format-enumeration"></a><span data-ttu-id="67a55-111">Перечисление формата вывода</span><span class="sxs-lookup"><span data-stu-id="67a55-111">Output Format Enumeration</span></span>

<span data-ttu-id="67a55-112">Объект Reader и синхронный объект Reader взаимодействуют с кодеками для перечисления возможных форматов вывода для сжатых потоков.</span><span class="sxs-lookup"><span data-stu-id="67a55-112">Both the reader object and the synchronous reader object communicate with the codecs to enumerate the possible output formats for compressed streams.</span></span> <span data-ttu-id="67a55-113">При чтении файла, содержащего содержимое, сжатое с помощью одного или нескольких кодеков Windows Media, можно просмотреть возможные форматы вывода, чтобы выбрать тот, который лучше подходит для ваших нужд.</span><span class="sxs-lookup"><span data-stu-id="67a55-113">When you read a file containing content compressed with one or more of the Windows Media codecs, you can examine the possible output formats to choose the one that best suits your needs.</span></span> <span data-ttu-id="67a55-114">Для удобства каждый кодек имеет формат вывода по умолчанию, для которого задан наиболее часто используемый формат.</span><span class="sxs-lookup"><span data-stu-id="67a55-114">For convenience, each codec has a default output format which is set to the most commonly used format.</span></span> <span data-ttu-id="67a55-115">Дополнительные сведения о перечислении Output см. [в разделе Работа с выходами](working-with-outputs.md).</span><span class="sxs-lookup"><span data-stu-id="67a55-115">For more information about output enumeration, see [Working with Outputs](working-with-outputs.md).</span></span>

<span data-ttu-id="67a55-116">Вы можете внести определенные изменения в выходной формат в зависимости от типа носителя.</span><span class="sxs-lookup"><span data-stu-id="67a55-116">You can make certain changes to an output format depending upon the media type.</span></span> <span data-ttu-id="67a55-117">Например, для видеопотоков можно изменить размер и глубину цвета.</span><span class="sxs-lookup"><span data-stu-id="67a55-117">For video streams, for example, you can change the frame size and color depth.</span></span> <span data-ttu-id="67a55-118">Объекты чтения поддерживают интерфейс для тестирования изменений, внесенных в формат вывода, именуемый [**ивмреадертипенеготиатион**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation).</span><span class="sxs-lookup"><span data-stu-id="67a55-118">The reading objects both support an interface to test changes you make to the output format, called [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation).</span></span>

## <a name="related-topics"></a><span data-ttu-id="67a55-119">См. также</span><span class="sxs-lookup"><span data-stu-id="67a55-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67a55-120">**Функции чтения файлов**</span><span class="sxs-lookup"><span data-stu-id="67a55-120">**File Reading Features**</span></span>](file-reading-features.md)
</dt> </dl>

 

 




