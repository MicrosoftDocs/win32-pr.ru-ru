---
description: Декодер Windows Media Audio Voice декодирует потоки, закодированные кодировщиком Windows Media Audio Voice.
ms.assetid: 8bb5c8bd-949f-4faa-b679-8854f78076a4
title: Декодер Windows Media Audio Voice (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4565a511f2816d2914ec96f3ae89f3af5dd19016
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694890"
---
# <a name="windows-media-audio-voice-decoder"></a><span data-ttu-id="ed16a-103">Декодер Windows Media Audio Voice</span><span class="sxs-lookup"><span data-stu-id="ed16a-103">Windows Media Audio Voice Decoder</span></span>

<span data-ttu-id="ed16a-104">Декодер Windows Media Audio Voice декодирует потоки, закодированные [**кодировщиком Windows Media Audio Voice**](windowsmediaaudiovoiceencoder.md).</span><span class="sxs-lookup"><span data-stu-id="ed16a-104">The Windows Media Audio Voice decoder decodes streams that were encoded by the [**Windows Media Audio Voice Encoder**](windowsmediaaudiovoiceencoder.md).</span></span>

## <a name="class-identifier"></a><span data-ttu-id="ed16a-105">Идентификатор класса</span><span class="sxs-lookup"><span data-stu-id="ed16a-105">Class Identifier</span></span>

<span data-ttu-id="ed16a-106">Идентификатор класса (CLSID) для декодера Windows Media Audio Voice представлен константой **CLSID \_ квмспдекмедиаобжект**.</span><span class="sxs-lookup"><span data-stu-id="ed16a-106">The class identifier (CLSID) for the Windows Media Audio Voice decoder is represented by the constant **CLSID\_CWMSPDecMediaObject**.</span></span> <span data-ttu-id="ed16a-107">Вы можете создать экземпляр декодера голоса, вызвав **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="ed16a-107">You can create an instance of the voice decoder by calling **CoCreateInstance**.</span></span>

## <a name="input-formats"></a><span data-ttu-id="ed16a-108">Форматы входных данных</span><span class="sxs-lookup"><span data-stu-id="ed16a-108">Input Formats</span></span>

<span data-ttu-id="ed16a-109">Содержимое в кодировке Windows Media Audio Voice определяется тегом формата 0x00.</span><span class="sxs-lookup"><span data-stu-id="ed16a-109">Windows Media Audio Voice encoded content is identified by the format tag 0x00A.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed16a-110">Требования</span><span class="sxs-lookup"><span data-stu-id="ed16a-110">Requirements</span></span>



| <span data-ttu-id="ed16a-111">Требование</span><span class="sxs-lookup"><span data-stu-id="ed16a-111">Requirement</span></span> | <span data-ttu-id="ed16a-112">Значение</span><span class="sxs-lookup"><span data-stu-id="ed16a-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed16a-113">Клиент</span><span class="sxs-lookup"><span data-stu-id="ed16a-113">Client</span></span><br/> | <span data-ttu-id="ed16a-114">Windows XP, Windows Vista или Windows 7</span><span class="sxs-lookup"><span data-stu-id="ed16a-114">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="ed16a-115">Header</span><span class="sxs-lookup"><span data-stu-id="ed16a-115">Header</span></span><br/> | <dl> <span data-ttu-id="ed16a-116"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed16a-116"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="ed16a-117">DLL</span><span class="sxs-lookup"><span data-stu-id="ed16a-117">DLL</span></span><br/>    | <dl> <span data-ttu-id="ed16a-118"><dt>Wmspdmod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed16a-118"><dt>Wmspdmod.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed16a-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed16a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed16a-120">Объекты кодека</span><span class="sxs-lookup"><span data-stu-id="ed16a-120">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="ed16a-121">Использование кодека Windows Media Audio Voice</span><span class="sxs-lookup"><span data-stu-id="ed16a-121">Using the Windows Media Audio Voice Codec</span></span>](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[<span data-ttu-id="ed16a-122">Кодировщик Windows Media Audio Voice</span><span class="sxs-lookup"><span data-stu-id="ed16a-122">Windows Media Audio Voice Encoder</span></span>](windowsmediaaudiovoiceencoder.md)
</dt> </dl>

 

 




