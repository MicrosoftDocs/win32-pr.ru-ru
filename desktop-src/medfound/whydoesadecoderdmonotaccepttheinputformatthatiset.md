---
description: Почему декодер не принимает заданный формат ввода?
ms.assetid: 19aa5677-bc3f-41d7-ad64-7c75021d907b
title: Почему декодер не принимает заданный формат ввода?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32ae4506fb6ed940bf0b4fffcf82ab78562872d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692763"
---
# <a name="why-does-a-decoder-not-accept-the-input-format-that-i-set"></a><span data-ttu-id="77c0a-103">Почему декодер не принимает заданный формат ввода?</span><span class="sxs-lookup"><span data-stu-id="77c0a-103">Why does a decoder not accept the input format that I set?</span></span>

<span data-ttu-id="77c0a-104">Существует множество причин, по которым декодер может отклонить формат.</span><span class="sxs-lookup"><span data-stu-id="77c0a-104">There are many reasons why a decoder might reject a format.</span></span> <span data-ttu-id="77c0a-105">Наиболее распространенные отсутствующие или неправильные данные расширенного формата.</span><span class="sxs-lookup"><span data-stu-id="77c0a-105">The most common is missing or incorrect extended format data.</span></span> <span data-ttu-id="77c0a-106">Расширенные данные формата представляют собой сведения, относящиеся к кодеку, которые добавляются к структуре, описывающей тип носителя.</span><span class="sxs-lookup"><span data-stu-id="77c0a-106">The extended format data is codec-specific information that is appended to the structure describing the media type.</span></span>

<span data-ttu-id="77c0a-107">При перечислении типа выходных данных с помощью объекта кодировщика элемент **пбформат** структуры [**\_ \_ типа мультимедиа DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) будет указывать на структуру **вавеформатекс** .</span><span class="sxs-lookup"><span data-stu-id="77c0a-107">When you enumerate an output type using an encoder object, the **pbFormat** member of the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure will point to a **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="77c0a-108">Эта структура содержит добавленные к нему данные расширенного формата, а размер этих данных хранится в элементе **вавеформатекс. кбсизе** .</span><span class="sxs-lookup"><span data-stu-id="77c0a-108">This structure has extended format data appended to it, and the size of that data is stored in the **WAVEFORMATEX.cbSize** member.</span></span> <span data-ttu-id="77c0a-109">Независимо от контейнера, используемого для хранения сжатых данных, необходимо сохранить структуру **вавеформатекс** и использовать ее в типе ввода для декодера.</span><span class="sxs-lookup"><span data-stu-id="77c0a-109">Regardless of the container used to store the compressed data, you must persist the **WAVEFORMATEX** structure and use it in the input type for the decoder.</span></span> <span data-ttu-id="77c0a-110">Без данных расширенного формата декодер не может распаковать содержимое.</span><span class="sxs-lookup"><span data-stu-id="77c0a-110">Without the extended format data, the decoder cannot decompress the content.</span></span>

<span data-ttu-id="77c0a-111">Для видеоформатов необходимо вручную извлечь данные расширенного формата и добавить их в структуру **видеоинфохеадер** .</span><span class="sxs-lookup"><span data-stu-id="77c0a-111">For video formats, you must manually retrieve the extended format data and append it to the **VIDEOINFOHEADER** structure.</span></span> <span data-ttu-id="77c0a-112">Дополнительные сведения см. [в разделе Использование частных данных видеокодека](usingvideocodecprivatedata.md).</span><span class="sxs-lookup"><span data-stu-id="77c0a-112">For more information, see [Using Video Codec Private Data](usingvideocodecprivatedata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="77c0a-113">См. также</span><span class="sxs-lookup"><span data-stu-id="77c0a-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77c0a-114">Часто задаваемые вопросы</span><span class="sxs-lookup"><span data-stu-id="77c0a-114">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 
