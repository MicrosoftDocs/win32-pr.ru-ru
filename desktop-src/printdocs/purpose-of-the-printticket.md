---
description: Цель PrintTicket — определить одну конкретную конфигурацию, которая применяется к обрабатываемому объекту задания.
ms.assetid: 8a7dd185-0324-44a0-8405-59a2fdc1efcb
title: Назначение PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d0166e150beedf354e4fb2c99a84e94c519fd5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405337"
---
# <a name="purpose-of-the-printticket"></a><span data-ttu-id="02983-103">Назначение PrintTicket</span><span class="sxs-lookup"><span data-stu-id="02983-103">Purpose of the PrintTicket</span></span>

<span data-ttu-id="02983-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="02983-104">This topic is not current.</span></span> <span data-ttu-id="02983-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="02983-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="02983-106">Основной целью PrintTicket является выражать конфигурации устройств.</span><span class="sxs-lookup"><span data-stu-id="02983-106">The primary purpose of the PrintTicket is to express device configurations.</span></span> <span data-ttu-id="02983-107">В отличие от документа PrintCapabilities, определяющего все возможные конфигурации, которые может предположить устройство (пространство конфигурации устройства), целью PrintTicket является определение отдельной конфигурации, применяемой к объекту задания (в данном случае на странице), который обрабатывается.</span><span class="sxs-lookup"><span data-stu-id="02983-107">In contrast to the PrintCapabilities document, which defines all possible configurations the device can assume (the device's configuration space), the PrintTicket's purpose is to define a single specific configuration that is applied to the job object (in this case the page) that is being processed.</span></span> <span data-ttu-id="02983-108">Чтобы повысить переносимость и согласованность конфигураций, конкретные ключевые слова и иерархия, представленные в разделе ключевых слов схемы Print, используются в технологиях PrintCapabilities и PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="02983-108">To promote portability and consistency of configurations, the specific keywords and hierarchy presented in the Print Schema Keywords section are used by both the PrintCapabilities and the PrintTicket technologies.</span></span> <span data-ttu-id="02983-109">Кроме того, [платформа схемы печати](print-schema-framework.md) определяет основные конструкции обеих технологий для повышения однозначного, открытого и расширяемого взаимодействия с форматированием заданий и PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="02983-109">In addition, the [Print Schema Framework](print-schema-framework.md) defines the basic constructs of both technologies, to promote unambiguous, open, and extensible communication of job formatting and PrintCapabilities.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02983-110">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="02983-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02983-111">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="02983-111">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



