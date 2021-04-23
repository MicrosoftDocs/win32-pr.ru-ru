---
title: Настройка потоков с VBR
description: Настройка потоков с VBR
ms.assetid: 83caabb7-b7fa-4b0a-a608-d5a86e4101b8
keywords:
- потоки, Настройка потоков VBR
- потоки, переменная скорость (VBR)
- Переменная скорость (VBR), потоки
- VBR (переменная скорость), потоки
- потоки, интерфейс Ивмпропертиваулт
- ивмпропертиваулт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6667dc9cf66932cf8af90da0b0e59ad27860ab3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103987188"
---
# <a name="configuring-vbr-streams"></a><span data-ttu-id="b38f0-109">Настройка потоков с VBR</span><span class="sxs-lookup"><span data-stu-id="b38f0-109">Configuring VBR Streams</span></span>

<span data-ttu-id="b38f0-110">Вы можете использовать кодирование с переменной скоростью (VBR) для создания высококачественных потоков для локальных файлов, а также для загрузки и воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="b38f0-110">You can use variable bit rate (VBR) encoding to produce high quality streams for local files or for downloading and playing.</span></span> <span data-ttu-id="b38f0-111">Существует три параметра для VBR: на основе качества (один проход), неограниченный (два прохода) и ограничен (два прохода).</span><span class="sxs-lookup"><span data-stu-id="b38f0-111">There are three options for VBR: quality-based (one-pass), unconstrained (two-pass), and constrained (two-pass).</span></span> <span data-ttu-id="b38f0-112">Дополнительные сведения о типах кодирования VBR см. в статье [кодирование с переменной скоростью (VBR)](variable-bit-rate--vbr--encoding.md).</span><span class="sxs-lookup"><span data-stu-id="b38f0-112">For more information about the types of VBR encoding, see [Variable Bit Rate (VBR) Encoding](variable-bit-rate--vbr--encoding.md).</span></span>

<span data-ttu-id="b38f0-113">Вы можете настроить кодирование VBR в профиле, задав свойства с помощью интерфейса [**ивмпропертиваулт**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) .</span><span class="sxs-lookup"><span data-stu-id="b38f0-113">You can configure VBR encoding in a profile by setting properties with the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface.</span></span> <span data-ttu-id="b38f0-114">В следующей таблице описаны свойства, используемые для настройки кодирования VBR.</span><span class="sxs-lookup"><span data-stu-id="b38f0-114">The following table describes the properties used to configure VBR encoding.</span></span>



| <span data-ttu-id="b38f0-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="b38f0-115">Property</span></span>                     | <span data-ttu-id="b38f0-116">Описание</span><span class="sxs-lookup"><span data-stu-id="b38f0-116">Description</span></span>                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b38f0-117">**g \_ всзвбренаблед**</span><span class="sxs-lookup"><span data-stu-id="b38f0-117">**g\_wszVBREnabled**</span></span>         | <span data-ttu-id="b38f0-118">.</span><span class="sxs-lookup"><span data-stu-id="b38f0-118">Boolean value.</span></span> <span data-ttu-id="b38f0-119">Задайте значение true, чтобы использовать кодирование VBR.</span><span class="sxs-lookup"><span data-stu-id="b38f0-119">Set to True to use VBR encoding.</span></span>                                                   |
| <span data-ttu-id="b38f0-120">**g \_ всзвбркуалити**</span><span class="sxs-lookup"><span data-stu-id="b38f0-120">**g\_wszVBRQuality**</span></span>         | <span data-ttu-id="b38f0-121">Значение **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="b38f0-121">**DWORD** value.</span></span> <span data-ttu-id="b38f0-122">Задайте желаемый уровень качества (от 1 до 100) для кодирования VBR с учетом качества.</span><span class="sxs-lookup"><span data-stu-id="b38f0-122">Set to the desired quality level (1 to 100) for quality-based VBR encoding.</span></span>      |
| <span data-ttu-id="b38f0-123">**g \_ всзвбрбитратемакс**</span><span class="sxs-lookup"><span data-stu-id="b38f0-123">**g\_wszVBRBitrateMax**</span></span>      | <span data-ttu-id="b38f0-124">Значение **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="b38f0-124">**DWORD** value.</span></span> <span data-ttu-id="b38f0-125">Задайте максимальную скорость в битах в секунду для кодирования с ограниченным числом VBR.</span><span class="sxs-lookup"><span data-stu-id="b38f0-125">Set to the maximum bit rate, in bits per second, for constrained VBR encoding.</span></span>   |
| <span data-ttu-id="b38f0-126">**g \_ всзвбрбуффервиндовмакс**</span><span class="sxs-lookup"><span data-stu-id="b38f0-126">**g\_wszVBRBufferWindowMax**</span></span> | <span data-ttu-id="b38f0-127">Значение **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="b38f0-127">**DWORD** value.</span></span> <span data-ttu-id="b38f0-128">Задайте максимальное окно буфера (в миллисекундах) для кодирования с ограничением VBR.</span><span class="sxs-lookup"><span data-stu-id="b38f0-128">Set to the maximum buffer window, in milliseconds, for constrained VBR encoding.</span></span> |



 

<span data-ttu-id="b38f0-129">В следующих разделах описано, как использовать различные типы кодирования с переменной скоростью.</span><span class="sxs-lookup"><span data-stu-id="b38f0-129">The following sections describe how to use the different types of variable bit rate encoding.</span></span>



| <span data-ttu-id="b38f0-130">Section</span><span class="sxs-lookup"><span data-stu-id="b38f0-130">Section</span></span>                                                              | <span data-ttu-id="b38f0-131">Описание</span><span class="sxs-lookup"><span data-stu-id="b38f0-131">Description</span></span>                                                                                                        |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b38f0-132">Настройка Quality-Based VBR</span><span class="sxs-lookup"><span data-stu-id="b38f0-132">To Configure Quality-Based VBR</span></span>](to-configure-quality-based-vbr.md) | <span data-ttu-id="b38f0-133">Описывает, как использовать переменное кодирование с переменной скоростью на основе статического уровня качества.</span><span class="sxs-lookup"><span data-stu-id="b38f0-133">Describes how to use variable bit rate encoding based on a static quality level.</span></span>                                   |
| [<span data-ttu-id="b38f0-134">Настройка неограниченных VBR</span><span class="sxs-lookup"><span data-stu-id="b38f0-134">To Configure Unconstrained VBR</span></span>](to-configure-unconstrained-vbr.md) | <span data-ttu-id="b38f0-135">Описывает использование переменной скорости кодирования с переменным битом, основанной на целевом среднем значении скорости без явного значения пиковой нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b38f0-135">Describes how to use variable bit rate encoding based on a target average bit rate without an explicit peak value.</span></span> |
| [<span data-ttu-id="b38f0-136">Настройка ограниченного VBR</span><span class="sxs-lookup"><span data-stu-id="b38f0-136">To Configure Constrained VBR</span></span>](to-configure-constrained-vbr.md)     | <span data-ttu-id="b38f0-137">Описывает, как использовать переменное кодирование с переменной скоростью на основе целевой средней скорости и явного пикового значения.</span><span class="sxs-lookup"><span data-stu-id="b38f0-137">Describes how to use variable bit rate encoding based on a target average bit rate and an explicit peak value.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="b38f0-138">См. также</span><span class="sxs-lookup"><span data-stu-id="b38f0-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b38f0-139">**Настройка потоков**</span><span class="sxs-lookup"><span data-stu-id="b38f0-139">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




