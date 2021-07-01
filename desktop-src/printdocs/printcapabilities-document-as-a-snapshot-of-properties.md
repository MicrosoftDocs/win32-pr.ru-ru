---
title: Документ как моментальный снимок свойств
description: Проверьте документ PrintCapabilities в виде моментального снимка свойств. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399c82211c268a72ad2b67082c144c64e46a879
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118649"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a><span data-ttu-id="4c320-105">PrintCapabilities документ в виде моментального снимка свойств</span><span class="sxs-lookup"><span data-stu-id="4c320-105">PrintCapabilities Document as a Snapshot of Properties</span></span>

<span data-ttu-id="4c320-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="4c320-106">This topic is not current.</span></span> <span data-ttu-id="4c320-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4c320-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4c320-108">Устройство, описываемое PrintCapabilities, может иметь свойства, зависящие от состояния или конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="4c320-108">The device described by the PrintCapabilities might have properties that depend on the state or configuration of the device.</span></span> <span data-ttu-id="4c320-109">Хотя PrintCapabilities представляет собой полное пространство конфигурации устройства, поставщик PrintCapabilities создает зависящий от конфигурации экземпляр PrintCapabilities, именуемый документом PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="4c320-109">While the PrintCapabilities represents the full configuration space of a device, the PrintCapabilities provider produces a configuration-dependent instance of the PrintCapabilities called the PrintCapabilities document.</span></span> <span data-ttu-id="4c320-110">Этот документ PrintCapabilities, зависящий от конфигурации, позволяет избежать появления схемы PrintCapabilities с сложностью представления многозначных данных.</span><span class="sxs-lookup"><span data-stu-id="4c320-110">This configuration-dependent PrintCapabilities document avoids burdening the PrintCapabilities Schema with the complexity of representing multivalued data.</span></span> <span data-ttu-id="4c320-111">Что более важно, чтобы освободить потребителя документа PrintCapabilities от нагрузки из многозначного представления данных, все экземпляры свойств и Скоредпроперти в документе PrintCapabilities должны быть однозначными.</span><span class="sxs-lookup"><span data-stu-id="4c320-111">More importantly, to relieve a consumer of the PrintCapabilities document from the burden of extracting the appropriate value from a multivalued data representation, all Property and ScoredProperty instances in a PrintCapabilities document are required to be single-valued.</span></span> <span data-ttu-id="4c320-112">Иными словами, каждое свойство и экземпляр Скоредпроперти в документе PrintCapabilities должны иметь фиксированное значение относительно входной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4c320-112">In other words, each Property and ScoredProperty instance in a PrintCapabilities document must have a fixed Value, relative to the input configuration.</span></span> <span data-ttu-id="4c320-113">Каждый документ PrintCapabilities можно рассматривать как моментальный снимок свойств устройства, когда устройство находится в определенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="4c320-113">Each PrintCapabilities document can be thought of as a snapshot of the properties of the device when the device is in a particular state.</span></span> <span data-ttu-id="4c320-114">Следовательно, прежде чем можно будет создать документ PrintCapabilities, необходимо указать используемую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="4c320-114">Consequently, before a PrintCapabilities document can be constructed, the configuration to be used must be provided.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c320-115">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="4c320-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c320-116">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="4c320-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



