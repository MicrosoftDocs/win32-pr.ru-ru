---
description: Длительность ускорения потоковой передачи для сетевого источника в миллисекундах.
ms.assetid: 3f9cd762-f393-4130-ba25-d16da0642093
title: Свойство MFNETSOURCE_ACCELERATEDSTREAMINGDURATION (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57980fbe08d3c6f48cf2638b35e88c455e566e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897934"
---
# <a name="mfnetsource_acceleratedstreamingduration-property"></a><span data-ttu-id="16e86-103">МФНЕТСАУРЦЕ \_ акцелератедстреамингдуратион, свойство</span><span class="sxs-lookup"><span data-stu-id="16e86-103">MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION property</span></span>

<span data-ttu-id="16e86-104">Длительность ускорения потоковой передачи для сетевого источника в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="16e86-104">Duration of accelerated streaming for the network source, in milliseconds.</span></span>



<span data-ttu-id="16e86-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="16e86-105">Data type</span></span>

<span data-ttu-id="16e86-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="16e86-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="16e86-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="16e86-107">PROPVARIANT member</span></span>

<span data-ttu-id="16e86-108">**DWORD** (хранится в формате **Long**)</span><span class="sxs-lookup"><span data-stu-id="16e86-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="16e86-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="16e86-109">VT\_I4</span></span>

<span data-ttu-id="16e86-110">**лвал**</span><span class="sxs-lookup"><span data-stu-id="16e86-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="16e86-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16e86-111">Remarks</span></span>

<span data-ttu-id="16e86-112">Константа **мфнетсаурце \_ акцелератедстреамингдуратион** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="16e86-112">The constant **MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION** defines the GUID for this property key.</span></span> <span data-ttu-id="16e86-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="16e86-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="16e86-114">Приложения могут использовать это свойство для настройки сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="16e86-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="16e86-115">Чтобы задать свойство, передайте объект **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="16e86-115">To set the property, pass an **IPropertyStore** object to the source resolver.</span></span> <span data-ttu-id="16e86-116">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="16e86-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="16e86-117">Это свойство применяется к функции быстрого запуска служб Windows Media, которая быстро воспроизводит содержимое, не дожидаясь длительной первоначальной буферизации.</span><span class="sxs-lookup"><span data-stu-id="16e86-117">This property applies to the Fast Start feature of Windows Media Services, which plays content quickly without waiting for lengthy initial buffering.</span></span> <span data-ttu-id="16e86-118">При использовании быстрого запуска сервер, на котором работают службы Windows Media, отправит некоторые данные в начале содержимого быстрее, чем указано в скорости потока содержимого.</span><span class="sxs-lookup"><span data-stu-id="16e86-118">When using Fast Start, the server running Windows Media Services will send some data at the beginning of the content at a faster rate than that specified by the bit rate of the content.</span></span>

<span data-ttu-id="16e86-119">Значение этого свойства по умолчанию равно 10 000 миллисекундам.</span><span class="sxs-lookup"><span data-stu-id="16e86-119">The default value of this property is 10,000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="16e86-120">Требования</span><span class="sxs-lookup"><span data-stu-id="16e86-120">Requirements</span></span>



| <span data-ttu-id="16e86-121">Требование</span><span class="sxs-lookup"><span data-stu-id="16e86-121">Requirement</span></span> | <span data-ttu-id="16e86-122">Значение</span><span class="sxs-lookup"><span data-stu-id="16e86-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="16e86-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="16e86-123">Minimum supported client</span></span><br/> | <span data-ttu-id="16e86-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="16e86-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="16e86-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="16e86-125">Minimum supported server</span></span><br/> | <span data-ttu-id="16e86-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="16e86-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="16e86-127">Header</span><span class="sxs-lookup"><span data-stu-id="16e86-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="16e86-128"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="16e86-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16e86-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16e86-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16e86-130">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="16e86-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="16e86-131">Компоненты сетевого источника</span><span class="sxs-lookup"><span data-stu-id="16e86-131">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="16e86-132">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="16e86-132">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




