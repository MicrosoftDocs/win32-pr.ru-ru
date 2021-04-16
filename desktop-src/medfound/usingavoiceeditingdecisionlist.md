---
description: Использование списка решений для изменения кодировки голоса
ms.assetid: a3d88483-acc9-47cf-8735-f17bd3b4ad57
title: Использование списка решений для изменения кодировки голоса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970cc40bc5749b9edc1017546020fa3806a9730b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662775"
---
# <a name="using-an-editing-decision-list-for-encoding-voice"></a><span data-ttu-id="b683b-103">Использование списка решений для изменения кодировки голоса</span><span class="sxs-lookup"><span data-stu-id="b683b-103">Using an Editing Decision List for Encoding Voice</span></span>

<span data-ttu-id="b683b-104">Изменение списка решений (ЕДЛ) — это данные, предоставленные кодеку, который предоставляет сведения о том, как закодировать определенные части содержимого.</span><span class="sxs-lookup"><span data-stu-id="b683b-104">An editing decision list (EDL), is data given to a codec that provides information about how specific portions of content should be encoded.</span></span> <span data-ttu-id="b683b-105">Голосовой кодек Windows Media Audio 9 поддерживает простой ЕДЛ, в котором можно указать части содержимого, содержащие музыку.</span><span class="sxs-lookup"><span data-stu-id="b683b-105">The Windows Media Audio 9 Voice codec supports a simple EDL in which you can specify the portions of content that contain music.</span></span> <span data-ttu-id="b683b-106">По умолчанию кодек обнаруживает фрагменты музыки при настройке для кодирования смешанного содержимого.</span><span class="sxs-lookup"><span data-stu-id="b683b-106">By default, the codec detects passages of music itself when configured to encode mixed content.</span></span> <span data-ttu-id="b683b-107">ЕДЛ следует использовать только в том случае, если кодек неправильно обнаруживает типы содержимого.</span><span class="sxs-lookup"><span data-stu-id="b683b-107">You should use an EDL only if the codec is not detecting the content types correctly.</span></span>

<span data-ttu-id="b683b-108">Чтобы использовать ЕДЛ, необходимо установить для голоса кодировщика смешанное содержимое.</span><span class="sxs-lookup"><span data-stu-id="b683b-108">To use an EDL, the voice encoder must be set to encode mixed content.</span></span> <span data-ttu-id="b683b-109">Настройте режим работы кодека "смешанный", задав для свойства [мфпкэй \_ вмавоице \_ ENC \_ мусикспичклассмоде](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) значение 2.</span><span class="sxs-lookup"><span data-stu-id="b683b-109">Configure the mode of the voice codec to "mixed" by setting the [MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) property to 2.</span></span> <span data-ttu-id="b683b-110">Задайте ЕДЛ с помощью свойства [мфпкэй \_ вмавоице \_ ENC \_ ЕДЛ](mfpkey-wmavoice-enc-edlproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="b683b-110">Set the EDL using the [MFPKEY\_WMAVOICE\_ENC\_EDL](mfpkey-wmavoice-enc-edlproperty.md) property.</span></span> <span data-ttu-id="b683b-111">Значением этого свойства является строка, содержащая разделенный запятыми список диапазонов времени в содержимом, которые должны быть закодированы в виде музыки.</span><span class="sxs-lookup"><span data-stu-id="b683b-111">The value of this property is a string containing a comma-delimited list of the time ranges in the content that should be encoded as music.</span></span> <span data-ttu-id="b683b-112">Первый элемент в списке — это версия ЕДЛ, которая всегда имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="b683b-112">The first item in the list is the version of the EDL, which is always 1.</span></span> <span data-ttu-id="b683b-113">Вторым элементом является количество разделов музыки, описанных в списке.</span><span class="sxs-lookup"><span data-stu-id="b683b-113">The second item is the number of music sections described in the list.</span></span> <span data-ttu-id="b683b-114">После второго элемента находится несколько пар значений, равных второму элементу. Каждая пара значений описывает начальную и конечную точки музыкального воспроизведения в содержимом, в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="b683b-114">Following the second item are a number of pairs of values equal to the second item; each pair of values describes the starting and ending point of a music passage in the content, in milliseconds.</span></span>

<span data-ttu-id="b683b-115">Например, строка ЕДЛ "1, 4, 1000, 2000, 5000, 6000, 9000, 10000, 13000, 14000" указывает четыре типа музыкальных данных, каждый из которых имеет одну секунду.</span><span class="sxs-lookup"><span data-stu-id="b683b-115">For example, the EDL string "1, 4, 1000, 2000, 5000, 6000, 9000, 10000, 13000, 14000" specifies four musical passages, each of which is one second long.</span></span> <span data-ttu-id="b683b-116">Если сведения в строке ЕДЛ недопустимы, они игнорируются.</span><span class="sxs-lookup"><span data-stu-id="b683b-116">If the information in the EDL string is invalid, it is ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b683b-117">См. также</span><span class="sxs-lookup"><span data-stu-id="b683b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b683b-118">Использование голосового кодека Windows Media Audio 9</span><span class="sxs-lookup"><span data-stu-id="b683b-118">Using the Windows Media Audio 9 Voice Codec</span></span>](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[<span data-ttu-id="b683b-119">Работа с аудио</span><span class="sxs-lookup"><span data-stu-id="b683b-119">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



