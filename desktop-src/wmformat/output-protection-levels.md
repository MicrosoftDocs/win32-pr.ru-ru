---
title: Уровни защиты выходных данных
description: Уровни защиты выходных данных
ms.assetid: 89a9fc13-5ade-4a33-8304-05a2ec999fc1
keywords:
- Windows Media Format SDK, уровни защиты выходных данных (ОПЛ)
- Управление цифровыми правами (DRM), уровни защиты выходных данных (ОПЛ)
- DRM (Управление цифровыми правами), уровни защиты выходных данных (ОПЛ)
- уровни защиты выходных данных (ОПЛ)
- ОПЛ (уровни защиты выходных данных)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5e5c1e08615b55aa1fb63e6d0c4e7bb82887c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986240"
---
# <a name="output-protection-levels"></a><span data-ttu-id="1c7ca-108">Уровни защиты выходных данных</span><span class="sxs-lookup"><span data-stu-id="1c7ca-108">Output Protection Levels</span></span>

<span data-ttu-id="1c7ca-109">Уровни защиты выходных данных (Оплс) — это числовые оценки, связанные с различными технологиями, которые получают мультимедийное содержимое.</span><span class="sxs-lookup"><span data-stu-id="1c7ca-109">Output protection levels (OPLs) are numerical ratings associated with various technologies that receive digital media content.</span></span> <span data-ttu-id="1c7ca-110">Поддержка технологии уровня a зависит от того, насколько безопасна эта технология.</span><span class="sxs-lookup"><span data-stu-id="1c7ca-110">The level a technology supports depends upon how secure it is.</span></span> <span data-ttu-id="1c7ca-111">Система ОПЛ, представленная в Windows Media DRM 10, позволяет создавать лицензии с большей гибкостью, чем в предыдущих версиях.</span><span class="sxs-lookup"><span data-stu-id="1c7ca-111">The OPL system, introduced in Windows Media DRM 10, enables licenses to be created with more flexibility than in previous versions.</span></span> <span data-ttu-id="1c7ca-112">Можно указать минимальное Оплс, необходимое для воспроизведения и копирования.</span><span class="sxs-lookup"><span data-stu-id="1c7ca-112">You can specify minimum OPLs required for playback and for copying.</span></span> <span data-ttu-id="1c7ca-113">Кроме того, можно указать исключения для минимума ОПЛ, чтобы разрешить недостаточную оценку технологии или запретить технологию с ОПЛ, которая превышает минимальное значение.</span><span class="sxs-lookup"><span data-stu-id="1c7ca-113">In addition, you can specify exceptions to the minimum OPL, either to allow a technology not rated high enough, or to disallow a technology with an OPL that exceeds the minimum.</span></span>

<span data-ttu-id="1c7ca-114">Указав ограничения на лицензии с помощью Оплс, владельцу содержимого необходимо использовать только два действия (копирование и воспроизведение), где предыдущие версии имели отдельные действия, определенные для различных типов устройств, поддерживаемых для копирования (SDMI, без SDMI и компакт-диска Red Book Audio).</span><span class="sxs-lookup"><span data-stu-id="1c7ca-114">By specifying restrictions to licenses using OPLs, a content owner need only use two actions (Copy and Play), where previous versions had separate actions defined for the various kinds of devices supported for copying (SDMI, non-SDMI, and Red Book audio CD).</span></span>

<span data-ttu-id="1c7ca-115">**Примечание** . DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="1c7ca-115">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c7ca-116">См. также</span><span class="sxs-lookup"><span data-stu-id="1c7ca-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c7ca-117">**Функции цифровых Rights Management**</span><span class="sxs-lookup"><span data-stu-id="1c7ca-117">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="1c7ca-118">**Работа с уровнями защиты выходных данных**</span><span class="sxs-lookup"><span data-stu-id="1c7ca-118">**Working with Output Protection Levels**</span></span>](working-with-output-protection-levels.md)
</dt> </dl>

 

 




