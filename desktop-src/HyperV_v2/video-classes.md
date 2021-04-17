---
description: Все виртуальные машины показывают наличие эмулированного видеоконтроллера S3 и виртуального видеоконтроллера с ускорением.
ms.assetid: 93BDC827-E84A-4460-A2DD-18EE87254426
title: Классы видео
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8687dc1f4c00c363ca9277c8404b338a0b7f7851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498024"
---
# <a name="video-classes"></a><span data-ttu-id="214fe-103">Классы видео</span><span class="sxs-lookup"><span data-stu-id="214fe-103">Video classes</span></span>

<span data-ttu-id="214fe-104">Все виртуальные машины показывают наличие эмулированного видеоконтроллера S3 и виртуального видеоконтроллера с ускорением.</span><span class="sxs-lookup"><span data-stu-id="214fe-104">All virtual machines reflect the presence of an emulated S3 video controller and an accelerated, synthetic video controller.</span></span>

<span data-ttu-id="214fe-105">С каждым контроллером экрана связан объект head видео.</span><span class="sxs-lookup"><span data-stu-id="214fe-105">Each display controller has a video head object associated with it.</span></span> <span data-ttu-id="214fe-106">Только один контроллер экрана может быть активным на виртуальной машине в любое время.</span><span class="sxs-lookup"><span data-stu-id="214fe-106">Only one display controller can be active in a virtual machine at any time.</span></span>

<span data-ttu-id="214fe-107">Для каждого активного удаленного сеанса, подключенного к виртуальной машине, имеется подключение терминала.</span><span class="sxs-lookup"><span data-stu-id="214fe-107">A terminal connection is present for every active remote session connected to a virtual machine.</span></span>

<span data-ttu-id="214fe-108">Ниже перечислены классы WMI виртуализации, связанные с видео.</span><span class="sxs-lookup"><span data-stu-id="214fe-108">The following are virtualization WMI classes related to video.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="214fe-109">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="214fe-109">In this section</span></span>



| <span data-ttu-id="214fe-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="214fe-110">Topic</span></span>                                                                                  | <span data-ttu-id="214fe-111">Описание</span><span class="sxs-lookup"><span data-stu-id="214fe-111">Description</span></span>                                                                                                                |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="214fe-112">**Мсвм \_ S3DisplayController**</span><span class="sxs-lookup"><span data-stu-id="214fe-112">**Msvm\_S3DisplayController**</span></span>](msvm-s3displaycontroller.md)<br/>               | <span data-ttu-id="214fe-113">Представляет состояние эмулированного контроллера S3, присутствующего в каждой конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="214fe-113">Represents the state of the emulated S3 controller that is present in each virtual machine configuration.</span></span><br/>       |
| [<span data-ttu-id="214fe-114">**Мсвм \_ синсетикдисплайконтроллер**</span><span class="sxs-lookup"><span data-stu-id="214fe-114">**Msvm\_SyntheticDisplayController**</span></span>](msvm-syntheticdisplaycontroller.md)<br/> | <span data-ttu-id="214fe-115">Представляет состояние искусственного контроллера экрана, присутствующего в каждой конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="214fe-115">Represents the state of the synthetic display controller that is present in each virtual machine configuration.</span></span><br/> |
| [<span data-ttu-id="214fe-116">**Мсвм \_ системтерминалконнектион**</span><span class="sxs-lookup"><span data-stu-id="214fe-116">**Msvm\_SystemTerminalConnection**</span></span>](msvm-systemterminalconnection.md)<br/>     | <span data-ttu-id="214fe-117">Связывает виртуальную машину с терминальным подключением.</span><span class="sxs-lookup"><span data-stu-id="214fe-117">Associates a virtual machine with a terminal connection.</span></span><br/>                                                        |
| [<span data-ttu-id="214fe-118">**Мсвм \_ терминалконнектион**</span><span class="sxs-lookup"><span data-stu-id="214fe-118">**Msvm\_TerminalConnection**</span></span>](msvm-terminalconnection.md)<br/>                 | <span data-ttu-id="214fe-119">Указывает состояние активного удаленного сеанса, взаимодействующего с виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="214fe-119">Indicates the state of an active remote session interacting with a virtual machine.</span></span><br/>                             |
| [<span data-ttu-id="214fe-120">**Мсвм \_ видеохеад**</span><span class="sxs-lookup"><span data-stu-id="214fe-120">**Msvm\_VideoHead**</span></span>](msvm-videohead.md)<br/>                                   | <span data-ttu-id="214fe-121">Описывает основную поверхность рисования на контроллере экрана.</span><span class="sxs-lookup"><span data-stu-id="214fe-121">Describes the primary drawing surface on a display controller.</span></span><br/>                                                  |
| [<span data-ttu-id="214fe-122">**Мсвм \_ видеохеадонконтроллер**</span><span class="sxs-lookup"><span data-stu-id="214fe-122">**Msvm\_VideoHeadOnController**</span></span>](msvm-videoheadoncontroller.md)<br/>           | <span data-ttu-id="214fe-123">Связывает головной диск с видеоконтроллером, который его содержит.</span><span class="sxs-lookup"><span data-stu-id="214fe-123">Associates a video head with the video controller that includes it.</span></span><br/>                                             |



 

 

 




