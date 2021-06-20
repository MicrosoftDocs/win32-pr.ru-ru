---
description: PrintCapabilities описывает конфигурации или состояния, доступные на устройстве, которые часто могут быть помещены в несколько различных конфигураций.
ms.assetid: 094472fc-28ca-4d7a-a8be-cc4623d02ff2
title: Общие сведения о PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c8f61d1ee4125a9a1ac5f9ddb07cf226cd7094e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408527"
---
# <a name="overview-of-the-printcapabilities"></a><span data-ttu-id="e0c55-103">Общие сведения о PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="e0c55-103">Overview of the PrintCapabilities</span></span>

<span data-ttu-id="e0c55-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="e0c55-104">This topic is not current.</span></span> <span data-ttu-id="e0c55-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e0c55-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e0c55-106">PrintCapabilities описывает конфигурации или состояния, доступные на устройстве.</span><span class="sxs-lookup"><span data-stu-id="e0c55-106">The PrintCapabilities describe the configurations or states available on a device.</span></span> <span data-ttu-id="e0c55-107">Устройство, описываемое PrintCapabilities, часто может быть помещено в несколько различных конфигураций.</span><span class="sxs-lookup"><span data-stu-id="e0c55-107">A device that is described by PrintCapabilities can often be placed in a number of different configurations.</span></span> <span data-ttu-id="e0c55-108">В случае печатающего устройства обычные атрибуты печати включают двустороннюю печать, разрешение и размер носителя.</span><span class="sxs-lookup"><span data-stu-id="e0c55-108">In the case of a printing device, typical printing attributes include duplex printing, resolution, and media size.</span></span> <span data-ttu-id="e0c55-109">Если устройство поддерживает эти атрибуты, они являются частью конфигурации для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="e0c55-109">If the device supports these attributes, they are part of the configuration for that device.</span></span> <span data-ttu-id="e0c55-110">Пользователь выбирает определенную конфигурацию, присваивая конкретное значение каждому из доступных атрибутов. Например, дуплекс: Онесидед, разрешение: 600 точек на дюйм и Медиасизе: Legal.</span><span class="sxs-lookup"><span data-stu-id="e0c55-110">The user selects a particular configuration by assigning a specific value to each of the available attributes; for example, Duplex: OneSided, Resolution: 600 dpi, and MediaSize: Legal.</span></span>

<span data-ttu-id="e0c55-111">PrintCapabilities построены на платформе схемы печати, которая определяет элементы, которые могут использоваться в PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="e0c55-111">The PrintCapabilities are built on the Print Schema Framework, which defines the elements that can be used in the PrintCapabilities.</span></span> <span data-ttu-id="e0c55-112">Ключевые слова схемы Print определяют часто используемые иерархии элементов или ключевые слова для повышения переносимости информации и намерения между отдельными клиентами.</span><span class="sxs-lookup"><span data-stu-id="e0c55-112">The Print Schema Keywords define commonly-used element hierarchies, or keywords, for the purpose of promoting portability of the information and intent between individual clients.</span></span> <span data-ttu-id="e0c55-113">Однако ключевые слова схемы Print также разрешают частные расширения, чтобы PrintCapabilities можно было адаптировать в соответствии с конкретными потребностями.</span><span class="sxs-lookup"><span data-stu-id="e0c55-113">However, the Print Schema Keywords also allow private extensions so that PrintCapabilities can be tailored to meet specific needs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0c55-114">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e0c55-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0c55-115">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="e0c55-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



