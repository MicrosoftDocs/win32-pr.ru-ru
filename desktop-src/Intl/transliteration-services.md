---
description: Службы транслитерации ELS сопоставляют текст UTF-16 от одной системы записи к другой системе письма.
ms.assetid: 32e46c52-5c3c-4e22-8f4e-05286ee213ba
title: Службы транслитерации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc00b96d56e6b05e70b352c81da0280e9ef35043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156582"
---
# <a name="transliteration-services"></a><span data-ttu-id="d80e9-103">Службы транслитерации</span><span class="sxs-lookup"><span data-stu-id="d80e9-103">Transliteration Services</span></span>

<span data-ttu-id="d80e9-104">Службы транслитерации ELS сопоставляют текст UTF-16 от одной системы записи к другой системе письма.</span><span class="sxs-lookup"><span data-stu-id="d80e9-104">The ELS transliteration services map UTF-16 text from one writing system to another writing system.</span></span> <span data-ttu-id="d80e9-105">Каждая служба фактически представляет собой данные, применяемые к определенному набору входных и выходных сценариев Юникода, а сам Транслитерация является внутренним по отношению к платформе ELS.</span><span class="sxs-lookup"><span data-stu-id="d80e9-105">Each service is really data applying to a specific set of input and output Unicode scripts, and the actual transliteration is internal to the ELS platform.</span></span> <span data-ttu-id="d80e9-106">Приложение может дополнительно перечислить доступные службы для конкретных входных и выходных скриптов и выбрать требуемую службу.</span><span class="sxs-lookup"><span data-stu-id="d80e9-106">The application can optionally enumerate the available services for specific input and output scripts and select the service that it requires.</span></span>

<span data-ttu-id="d80e9-107">Платформа поддерживает метаданные для служб транслитерации ELS.</span><span class="sxs-lookup"><span data-stu-id="d80e9-107">The platform maintains metadata for the ELS transliteration services.</span></span> <span data-ttu-id="d80e9-108">Метаданные для каждой службы предоставляют описание службы и список входных и выходных скриптов, поддерживаемых службой.</span><span class="sxs-lookup"><span data-stu-id="d80e9-108">Metadata for each service provides a description of the service and lists the input and output scripts that the service supports.</span></span> <span data-ttu-id="d80e9-109">Метаданные представлены структурой [**\_ \_ сведений службы сопоставления**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) , полученной функцией [**маппингжетсервицес**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) .</span><span class="sxs-lookup"><span data-stu-id="d80e9-109">The metadata is represented by a [**MAPPING\_SERVICE\_INFO**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) structure retrieved by the [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) function.</span></span>

## <a name="input-to-a-transliteration-service"></a><span data-ttu-id="d80e9-110">Входные данные для службы транслитерации</span><span class="sxs-lookup"><span data-stu-id="d80e9-110">Input to a Transliteration Service</span></span>

<span data-ttu-id="d80e9-111">В качестве входных данных для службы транслитерации используется текст UTF-16 в одной системе записи.</span><span class="sxs-lookup"><span data-stu-id="d80e9-111">The input to a transliteration service is UTF-16 text in one writing system.</span></span>

## <a name="output-of-a-transliteration-service"></a><span data-ttu-id="d80e9-112">Выходные данные службы транслитерации</span><span class="sxs-lookup"><span data-stu-id="d80e9-112">Output of a Transliteration Service</span></span>

<span data-ttu-id="d80e9-113">В качестве выходных данных службы транслитерации используется текст UTF-16, сопоставленный со второй системой записи.</span><span class="sxs-lookup"><span data-stu-id="d80e9-113">The output of a transliteration service is UTF-16 text mapped to a second writing system.</span></span> <span data-ttu-id="d80e9-114">Если подходящее сопоставление транслитерации для любого фрагмента входного текста не поддерживается, то фрагмент остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="d80e9-114">If no appropriate transliteration mapping is available for any given chunk of the input text, the chunk remains unchanged.</span></span>

## <a name="transliteration-service-operation"></a><span data-ttu-id="d80e9-115">Операция службы транслитерации</span><span class="sxs-lookup"><span data-stu-id="d80e9-115">Transliteration Service Operation</span></span>

<span data-ttu-id="d80e9-116">Служба транслитерации сопоставляет текст Юникода из входного скрипта с выходным скриптом, символом или термином по условию, соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="d80e9-116">A transliteration service maps Unicode text from an input script to an output script, character by character or term by term, as appropriate.</span></span> <span data-ttu-id="d80e9-117">Приложение может выбрать получение определенной службы транслитерации, указав входные и выходные скрипты при вызове [**маппингжетсервицес**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)или указав идентификатор GUID службы.</span><span class="sxs-lookup"><span data-stu-id="d80e9-117">The application can choose to obtain the specific transliteration service of interest by specifying input and output scripts when calling [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices), or by providing the service GUID.</span></span> <span data-ttu-id="d80e9-118">Кроме того, для приложения можно перечислить все доступные службы транслитерации, указав категорию службы «Транслитерация» при вызове **маппингжетсервицес**.</span><span class="sxs-lookup"><span data-stu-id="d80e9-118">Another option for the application is to enumerate all available transliteration services by specifying the service category "Transliteration" when calling **MappingGetServices**.</span></span> <span data-ttu-id="d80e9-119">В этом случае приложение вызывает каждую службу и сравнивает результаты с исходным текстом, чтобы узнать, были ли результаты изменены операцией определенной службы.</span><span class="sxs-lookup"><span data-stu-id="d80e9-119">In this case, the application calls each service and compares the results with the original text to see if the results have been changed by the operation of a particular service.</span></span>

<span data-ttu-id="d80e9-120">Приложение может запрашивать распознавание текста для службы ELSного транслитерации с помощью вызова [**маппингрекогнизетекст**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext).</span><span class="sxs-lookup"><span data-stu-id="d80e9-120">The application can request text recognition for an ELS transliteration service with a call to [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext).</span></span> <span data-ttu-id="d80e9-121">При получении запроса служба транслитерации выделяет буфер для хранения данных, а затем выполняет распознавание текста для каждой кодовой точки во входной строке, предоставляемой приложением.</span><span class="sxs-lookup"><span data-stu-id="d80e9-121">When it receives the request, the transliteration service allocates a buffer to contain the transliterated data, and then performs text recognition for each code point in the input string supplied by the application.</span></span>

> [!Note]  
> <span data-ttu-id="d80e9-122">Исходный текст и перетранслитерированный текст могут иметь разную длину.</span><span class="sxs-lookup"><span data-stu-id="d80e9-122">The original text and the transliterated text might have different lengths.</span></span>

 

## <a name="transliteration-service-guids"></a><span data-ttu-id="d80e9-123">Идентификаторы GUID службы транслитерации</span><span class="sxs-lookup"><span data-stu-id="d80e9-123">Transliteration Service GUIDs</span></span>

<span data-ttu-id="d80e9-124">Идентификаторы GUID для служб транслитерации объявляются в Елссрвк. h, как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="d80e9-124">The GUIDs for the transliteration services are declared in Elssrvc.h, as shown in the following code.</span></span>


```C++
// {A3A8333B-F4FC-42f6-A0C4-0462FE7317CB}
static const GUID ELS_GUID_TRANSLITERATION_HANT_TO_HANS =
    { 0xA3A8333B, 0xF4FC, 0x42f6, { 0xA0, 0xC4, 0x04, 0x62, 0xFE, 0x73, 0x17, 0xCB } };

// {3CACCDC8-5590-42dc-9A7B-B5A6B5B3B63B}
static const GUID ELS_GUID_TRANSLITERATION_HANS_TO_HANT =
    { 0x3CACCDC8, 0x5590, 0x42dc, { 0x9A, 0x7B, 0xB5, 0xA6, 0xB5, 0xB3, 0xB6, 0x3B } };

// {D8B983B1-F8BF-4a2b-BCD5-5B5EA20613E1}
static const GUID ELS_GUID_TRANSLITERATION_MALAYALAM_TO_LATIN =
    { 0xD8B983B1, 0xF8BF, 0x4a2b, { 0xBC, 0xD5, 0x5B, 0x5E, 0xA2, 0x06, 0x13, 0xE1 } };

// {C4A4DCFE-2661-4d02-9835-F48187109803}
static const GUID ELS_GUID_TRANSLITERATION_DEVANAGARI_TO_LATIN =
    { 0xC4A4DCFE, 0x2661, 0x4d02, { 0x98, 0x35, 0xF4, 0x81, 0x87, 0x10, 0x98, 0x03 } };

// {3DD12A98-5AFD-4903-A13F-E17E6C0BFE01}
static const GUID ELS_GUID_TRANSLITERATION_CYRILLIC_TO_LATIN =
    { 0x3DD12A98, 0x5AFD, 0x4903, { 0xA1, 0x3F, 0xE1, 0x7E, 0x6C, 0x0B, 0xFE, 0x01 } };

// {F4DFD825-91A4-489f-855E-9AD9BEE55727}
static const GUID ELS_GUID_TRANSLITERATION_BENGALI_TO_LATIN =
    { 0xF4DFD825, 0x91A4, 0x489f, { 0x85, 0x5E, 0x9A, 0xD9, 0xBE, 0xE5, 0x57, 0x27 } };
```



## <a name="related-topics"></a><span data-ttu-id="d80e9-125">См. также</span><span class="sxs-lookup"><span data-stu-id="d80e9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d80e9-126">О расширенных лингвистических службах</span><span class="sxs-lookup"><span data-stu-id="d80e9-126">About Extended Linguistic Services</span></span>](about-extended-linguistic-services.md)
</dt> </dl>

 

 



