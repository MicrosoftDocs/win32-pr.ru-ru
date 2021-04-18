---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 8a7dd185-0324-44a0-8405-59a2fdc1efcb
title: Назначение PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a191f341504a92fbb5f4cd00abd2a4357bbecf21
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105684812"
---
# <a name="purpose-of-the-printticket"></a><span data-ttu-id="98da1-104">Назначение PrintTicket</span><span class="sxs-lookup"><span data-stu-id="98da1-104">Purpose of the PrintTicket</span></span>

<span data-ttu-id="98da1-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="98da1-105">This topic is not current.</span></span> <span data-ttu-id="98da1-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="98da1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="98da1-107">Основной целью PrintTicket является выражать конфигурации устройств.</span><span class="sxs-lookup"><span data-stu-id="98da1-107">The primary purpose of the PrintTicket is to express device configurations.</span></span> <span data-ttu-id="98da1-108">В отличие от документа PrintCapabilities, определяющего все возможные конфигурации, которые может предположить устройство (пространство конфигурации устройства), целью PrintTicket является определение отдельной конфигурации, применяемой к объекту задания (в данном случае на странице), который обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="98da1-108">In contrast to the PrintCapabilities document, which defines all possible configurations the device can assume (the device's configuration space), the PrintTicket's purpose is to define a single specific configuration that is applied to the job object (in this case the page) that is being processed.</span></span> <span data-ttu-id="98da1-109">Чтобы повысить переносимость и согласованность конфигураций, конкретные ключевые слова и иерархия, представленные в разделе ключевых слов схемы Print, используются в технологиях PrintCapabilities и PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="98da1-109">To promote portability and consistency of configurations, the specific keywords and hierarchy presented in the Print Schema Keywords section are used by both the PrintCapabilities and the PrintTicket technologies.</span></span> <span data-ttu-id="98da1-110">Кроме того, [платформа схемы печати](print-schema-framework.md) определяет основные конструкции обеих технологий для повышения однозначного, открытого и расширяемого взаимодействия с форматированием заданий и PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="98da1-110">In addition, the [Print Schema Framework](print-schema-framework.md) defines the basic constructs of both technologies, to promote unambiguous, open, and extensible communication of job formatting and PrintCapabilities.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98da1-111">См. также</span><span class="sxs-lookup"><span data-stu-id="98da1-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98da1-112">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="98da1-112">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



