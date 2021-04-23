---
description: '\_Свойство взаимосвязи аудиоендпоинт "PKEY" \_ связывает категорию закрепления "потоковая передача" (KS) с устройством конечной точки аудио.'
ms.assetid: a20e082c-eddb-4b81-b851-49350b87e69a
title: PKEY_AudioEndpoint_Association (Ммдевицеапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe2a7ec4f979e12dd6b548d27e0112c784105074
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656049"
---
# <a name="pkey_audioendpoint_association"></a><span data-ttu-id="c87d5-103">\_Связь АУДИОЕНДПОИНТ \_ PKEY</span><span class="sxs-lookup"><span data-stu-id="c87d5-103">PKEY\_AudioEndpoint\_Association</span></span>

<span data-ttu-id="c87d5-104">Свойство **\_ \_ взаимосвязи аудиоендпоинт "PKEY** " связывает категорию закрепления "потоковая передача" (KS) с устройством конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="c87d5-104">The **PKEY\_AudioEndpoint\_Association** property associates a kernel-streaming (KS) pin category with an audio endpoint device.</span></span> <span data-ttu-id="c87d5-105">INF-файл, устанавливающий звуковой адаптер, назначает категорию закрепления каждому ПИН-коду KS в адаптере.</span><span class="sxs-lookup"><span data-stu-id="c87d5-105">The .inf file that installs an audio adapter assigns a pin category to each KS pin in the adapter.</span></span> <span data-ttu-id="c87d5-106">ПИН-код KS на устройстве адаптера представляет точку, в которую поток аудио попадает или покидает устройство.</span><span class="sxs-lookup"><span data-stu-id="c87d5-106">A KS pin on an adapter device represents the point at which an audio stream enters or leaves the device.</span></span> <span data-ttu-id="c87d5-107">Категория закрепления — это идентификатор GUID, указывающий тип функции, выполняемой ПИН-кодом KS.</span><span class="sxs-lookup"><span data-stu-id="c87d5-107">A pin category is a GUID that specifies the type of function performed by a KS pin.</span></span> <span data-ttu-id="c87d5-108">Например, файл заголовков Ксмедиа. h определяет PIN-код категории GUID КСНОДЕТИПЕ \_ Microphone для указания ПИН-кода KS, который подключается к микрофону, а кснодетипе \_ наушники — для указания ПИН-кода KS, который подключается к наушникам.</span><span class="sxs-lookup"><span data-stu-id="c87d5-108">For example, header file Ksmedia.h defines pin-category GUID KSNODETYPE\_MICROPHONE to indicate a KS pin that connects to a microphone, and KSNODETYPE\_HEADPHONES to indicate a KS pin that connects to headphones.</span></span> <span data-ttu-id="c87d5-109">Дополнительные сведения см. в описании свойств категории ПИН-кодов в документации по Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="c87d5-109">For more information, see the description of pin category properties in the Windows DDK documentation.</span></span>

<span data-ttu-id="c87d5-110">Элементу **VT** структуры **пропвариант** присвоено значение VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="c87d5-110">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="c87d5-111">Элемент **пвсзвал** структуры **пропвариант** указывает на строку расширенных символов, заканчивающуюся НУЛЕМ, которая содержит GUID категории ПИН-кода в KS.</span><span class="sxs-lookup"><span data-stu-id="c87d5-111">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a KS pin category GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="c87d5-112">Требования</span><span class="sxs-lookup"><span data-stu-id="c87d5-112">Requirements</span></span>



| <span data-ttu-id="c87d5-113">Требование</span><span class="sxs-lookup"><span data-stu-id="c87d5-113">Requirement</span></span> | <span data-ttu-id="c87d5-114">Значение</span><span class="sxs-lookup"><span data-stu-id="c87d5-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c87d5-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c87d5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c87d5-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c87d5-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c87d5-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c87d5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c87d5-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c87d5-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c87d5-119">Header</span><span class="sxs-lookup"><span data-stu-id="c87d5-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c87d5-120"><dt>Ммдевицеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="c87d5-120"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c87d5-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c87d5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c87d5-122">**Свойства конечной точки аудио**</span><span class="sxs-lookup"><span data-stu-id="c87d5-122">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="c87d5-123">Основные свойства звука</span><span class="sxs-lookup"><span data-stu-id="c87d5-123">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




