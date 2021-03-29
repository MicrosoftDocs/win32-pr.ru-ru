---
description: Свойство PKEY \_ аудиоендпоинт \_ жакксубтипе содержит идентификатор GUID категории вывода для устройства конечной точки аудио.
ms.assetid: 5d712823-73e3-4872-a1ea-c166ed41ffa0
title: PKEY_AudioEndpoint_JackSubType (Ммдевицеапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3546c9741dcfd6065372f0a88a3ce3a921daad8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142433"
---
# <a name="pkey_audioendpoint_jacksubtype"></a><span data-ttu-id="fc590-103">PKEY \_ аудиоендпоинт \_ жакксубтипе</span><span class="sxs-lookup"><span data-stu-id="fc590-103">PKEY\_AudioEndpoint\_JackSubType</span></span>

<span data-ttu-id="fc590-104">Свойство **PKEY \_ аудиоендпоинт \_ жакксубтипе** содержит идентификатор GUID категории вывода для устройства конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="fc590-104">The **PKEY\_AudioEndpoint\_JackSubType** property contains an output category GUID for an audio endpoint device.</span></span> <span data-ttu-id="fc590-105">В файле заголовка Ксмедиа. h определяются идентификаторы GUID. каждый GUID указывает тип соединения.</span><span class="sxs-lookup"><span data-stu-id="fc590-105">The header file Ksmedia.h defines the GUIDs; each GUID specifies the type of connection.</span></span> <span data-ttu-id="fc590-106">Эти идентификаторы GUID также имеют связанные категории закрепления.</span><span class="sxs-lookup"><span data-stu-id="fc590-106">These GUIDs also have associated pin categories.</span></span> <span data-ttu-id="fc590-107">Например, файл заголовков Ксмедиа. h определяет идентификатор **GUID \_ кснодетипе \_ дисплайпорт** для порта дисплея, который подключается с помощью ПИН-кода KS, определенного GUID **пиннаме \_ дисплайпорт \_ out**.</span><span class="sxs-lookup"><span data-stu-id="fc590-107">For example, header file Ksmedia.h defines the GUID **KSNODETYPE\_DISPLAYPORT\_INTERFACE** for a display port that connects with the KS pin defined by the GUID **PINNAME\_DISPLAYPORT\_OUT**.</span></span>

<span data-ttu-id="fc590-108">Дополнительные сведения см. в описании свойств категории ПИН-кодов в документации по Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="fc590-108">For more information, see the description of pin category properties in the Windows DDK documentation.</span></span>

<span data-ttu-id="fc590-109">Элементу **VT** структуры **пропвариант** присвоено значение **VT \_ LPWSTR**.</span><span class="sxs-lookup"><span data-stu-id="fc590-109">The **vt** member of the **PROPVARIANT** structure is set to **VT\_LPWSTR**.</span></span>

<span data-ttu-id="fc590-110">Элемент **пвсзвал** структуры **пропвариант** указывает на строку расширенных символов, заканчивающуюся нулем и содержащую GUID категории.</span><span class="sxs-lookup"><span data-stu-id="fc590-110">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a category GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc590-111">Требования</span><span class="sxs-lookup"><span data-stu-id="fc590-111">Requirements</span></span>



| <span data-ttu-id="fc590-112">Требование</span><span class="sxs-lookup"><span data-stu-id="fc590-112">Requirement</span></span> | <span data-ttu-id="fc590-113">Значение</span><span class="sxs-lookup"><span data-stu-id="fc590-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc590-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc590-114">Minimum supported client</span></span><br/> | <span data-ttu-id="fc590-115">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fc590-115">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fc590-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc590-116">Minimum supported server</span></span><br/> | <span data-ttu-id="fc590-117">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="fc590-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fc590-118">Header</span><span class="sxs-lookup"><span data-stu-id="fc590-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc590-119"><dt>Ммдевицеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc590-119"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc590-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc590-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc590-121">**Свойства конечной точки аудио**</span><span class="sxs-lookup"><span data-stu-id="fc590-121">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="fc590-122">Основные свойства звука</span><span class="sxs-lookup"><span data-stu-id="fc590-122">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




