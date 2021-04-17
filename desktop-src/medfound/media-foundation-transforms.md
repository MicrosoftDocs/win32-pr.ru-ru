---
description: Преобразования Media Foundation
ms.assetid: cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0
title: Преобразования Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0518ced06169f6d998bdad1747878d109e0676
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703471"
---
# <a name="media-foundation-transforms"></a><span data-ttu-id="3e3ce-103">Преобразования Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3e3ce-103">Media Foundation Transforms</span></span>

<span data-ttu-id="3e3ce-104">Media Foundation преобразования (МФТС) предоставляют универсальную модель для обработки данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3e3ce-104">Media Foundation transforms (MFTs) provide a generic model for processing media data.</span></span> <span data-ttu-id="3e3ce-105">МФТС используются для декодеров, кодировщиков и обработчиков цифровых сигналов (DSP).</span><span class="sxs-lookup"><span data-stu-id="3e3ce-105">MFTs are used for decoders, encoders, and digital signal processors (DSPs).</span></span> <span data-ttu-id="3e3ce-106">Вкратце, все, что располагается в конвейере мультимедиа между источником мультимедиа и приемником мультимедиа, является MFT.</span><span class="sxs-lookup"><span data-stu-id="3e3ce-106">In short, anything that sits in the media pipeline between the media source and the media sink is an MFT.</span></span>

<span data-ttu-id="3e3ce-107">В этом разделе описывается модель программирования MFT и способы реализации MFT с рекомендациями для конкретных типов МФТС, таких как декодеры.</span><span class="sxs-lookup"><span data-stu-id="3e3ce-107">This section describes the MFT programming model and how to implement an MFT, with recommendations for specific types of MFTs, such as decoders.</span></span>



| <span data-ttu-id="3e3ce-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="3e3ce-108">Topic</span></span>                                                                    | <span data-ttu-id="3e3ce-109">Описание</span><span class="sxs-lookup"><span data-stu-id="3e3ce-109">Description</span></span>                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e3ce-110">О МФТС</span><span class="sxs-lookup"><span data-stu-id="3e3ce-110">About MFTs</span></span>](about-mfts.md)                                             | <span data-ttu-id="3e3ce-111">Содержит краткий обзор МФТС</span><span class="sxs-lookup"><span data-stu-id="3e3ce-111">Provides a brief overview of MFTs</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="3e3ce-112">Базовая модель обработки MFT</span><span class="sxs-lookup"><span data-stu-id="3e3ce-112">Basic MFT Processing Model</span></span>](basic-mft-processing-model.md)             | <span data-ttu-id="3e3ce-113">Более подробно описывается базовая модель обработки данных с помощью MFT.</span><span class="sxs-lookup"><span data-stu-id="3e3ce-113">Describes in more detail the basic model for processing data with an MFT.</span></span>                                                                                                                           |
| [<span data-ttu-id="3e3ce-114">Асинхронный МФТС</span><span class="sxs-lookup"><span data-stu-id="3e3ce-114">Asynchronous MFTs</span></span>](asynchronous-mfts.md)                               | <span data-ttu-id="3e3ce-115">Описывает модель асинхронной обработки, которая является альтернативой базовой модели.</span><span class="sxs-lookup"><span data-stu-id="3e3ce-115">Describes an asynchronous processing model that is an alternative to the basic model.</span></span><br/> <span data-ttu-id="3e3ce-116">Асинхронная обработка появилась в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3e3ce-116">Asynchronous processing was introduced in Windows 7.</span></span> <span data-ttu-id="3e3ce-117">Эта модель поддерживается не для всех MFT.</span><span class="sxs-lookup"><span data-stu-id="3e3ce-117">Not every MFT supports this model.</span></span><br/> |
| [<span data-ttu-id="3e3ce-118">Регистрация и перечисление МФТС</span><span class="sxs-lookup"><span data-stu-id="3e3ce-118">Registering and Enumerating MFTs</span></span>](registering-and-enumerating-mfts.md) | <span data-ttu-id="3e3ce-119">Как зарегистрировать таблицу MFT и как перечислить МФТС в реестре.</span><span class="sxs-lookup"><span data-stu-id="3e3ce-119">How to register an MFT and how to enumerate MFTs in the registry.</span></span>                                                                                                                                   |
| [<span data-ttu-id="3e3ce-120">Поле ограничений использования</span><span class="sxs-lookup"><span data-stu-id="3e3ce-120">Field of Use Restrictions</span></span>](field-of-use-restrictions.md)               | <span data-ttu-id="3e3ce-121">Описывает механизм разблокировки MFT с ограничениями на использование полей.</span><span class="sxs-lookup"><span data-stu-id="3e3ce-121">Describes the mechanism for unlocking an MFT that has field-of-use restrictions.</span></span>                                                                                                                    |
| [<span data-ttu-id="3e3ce-122">Сравнение преобразований MFT и объектов DMO</span><span class="sxs-lookup"><span data-stu-id="3e3ce-122">Comparison of MFTs and DMOs</span></span>](comparison-of-mfts-and-dmos.md)           | <span data-ttu-id="3e3ce-123">Содержит сводку различий между МФТС и дмос.</span><span class="sxs-lookup"><span data-stu-id="3e3ce-123">Summarizes the differences between MFTs and DMOs.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="3e3ce-124">Запись пользовательского MFT</span><span class="sxs-lookup"><span data-stu-id="3e3ce-124">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)                         | <span data-ttu-id="3e3ce-125">Рекомендации по написанию настраиваемой таблицы MFT.</span><span class="sxs-lookup"><span data-stu-id="3e3ce-125">Guidelines for writing a custom MFT.</span></span>                                                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="3e3ce-126">См. также</span><span class="sxs-lookup"><span data-stu-id="3e3ce-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e3ce-127">Конвейер Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3e3ce-127">Media Foundation Pipeline</span></span>](media-foundation-pipeline.md)
</dt> <dt>

[<span data-ttu-id="3e3ce-128">Архитектура Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3e3ce-128">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="3e3ce-129">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="3e3ce-129">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




