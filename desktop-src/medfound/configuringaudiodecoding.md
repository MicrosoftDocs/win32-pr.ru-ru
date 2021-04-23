---
description: Настройка декодирования звука
ms.assetid: 362bd3bc-1474-4132-a8a8-e5dc0bba80e7
title: Настройка декодирования звука (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da4d6a9d41b5c504ff60f25db20265072218caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808147"
---
# <a name="configuring-audio-decoding-microsoft-media-foundation"></a><span data-ttu-id="68260-103">Настройка декодирования звука (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="68260-103">Configuring Audio Decoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="68260-104">Декодирование содержимого Windows Media Audio намного проще, чем его кодирование.</span><span class="sxs-lookup"><span data-stu-id="68260-104">Decoding Windows Media Audio content is much easier than encoding it.</span></span> <span data-ttu-id="68260-105">После создания объекта звукового декодера задайте тип входных данных с помощью метода **имедиаобжект:: сетинпуттипе** или **Имфтрансформ:: сетинпуттипе** .</span><span class="sxs-lookup"><span data-stu-id="68260-105">After creating an audio decoder object, set the input type by using the **IMediaObject::SetInputType** or **IMFTransform::SetInputType** method.</span></span> <span data-ttu-id="68260-106">Тип носителя, используемый для входных данных декодера, должен соответствовать типу выходных данных, который использовался при кодировании содержимого.</span><span class="sxs-lookup"><span data-stu-id="68260-106">The media type that you use for the decoder input must match the output type that was used when the content was encoded.</span></span> <span data-ttu-id="68260-107">Сюда входят данные расширенного формата, добавленные в структуру **вавеформатекс** .</span><span class="sxs-lookup"><span data-stu-id="68260-107">This includes the extended format data appended to the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="68260-108">Необходимо убедиться, что эти данные верны, так как декодер не может обрабатывать примеры без него.</span><span class="sxs-lookup"><span data-stu-id="68260-108">You must ensure that this data is correct, because the decoder cannot process samples without it.</span></span>

<span data-ttu-id="68260-109">После настройки типа входных данных можно настроить любые функции декодера, которые вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="68260-109">After setting the input type, you can configure any decoder features you want to use.</span></span> <span data-ttu-id="68260-110">Функции декодера, такие как используемые для кодирования, задаются с помощью методов **ипропертибаг** или **ипропертисторе**.</span><span class="sxs-lookup"><span data-stu-id="68260-110">Decoder features, like those used for encoding, are set using the methods of **IPropertyBag** or **IPropertyStore**.</span></span>

<span data-ttu-id="68260-111">После установки типа входных данных и настройки всех функций декодера можно перечислить типы выходных данных, поддерживаемые декодером, выполнив вызовы **имедиаобжект:: жетаутпуттипе** или **Имфтрансформ:: жетаутпуттипе**.</span><span class="sxs-lookup"><span data-stu-id="68260-111">After the input type is set and all decoder features are configured, you can enumerate the output types supported by the decoder by making calls to **IMediaObject::GetOutputType** or **IMFTransform::GetOutputType**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68260-112">См. также</span><span class="sxs-lookup"><span data-stu-id="68260-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68260-113">Работа с аудио</span><span class="sxs-lookup"><span data-stu-id="68260-113">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



