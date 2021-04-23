---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: c48b9821-9194-47d9-a3ec-b10dbbdf14cc
title: Обзор функций PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a70945fcc18e08615a9674a90a023f4ee12a76e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105656741"
---
# <a name="overview-of-printticket-functionality"></a><span data-ttu-id="16a0c-104">Обзор функций PrintTicket</span><span class="sxs-lookup"><span data-stu-id="16a0c-104">Overview of PrintTicket Functionality</span></span>

<span data-ttu-id="16a0c-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="16a0c-105">This topic is not current.</span></span> <span data-ttu-id="16a0c-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="16a0c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="16a0c-107">PrintTicket использует формат на основе XML для представления сведений о конфигурации устройства с помощью конструкций функций, параметров и параметров платформы схемы печати.</span><span class="sxs-lookup"><span data-stu-id="16a0c-107">The PrintTicket utilizes an XML-based format for expressing device configuration information using the Feature/Option and parameter constructs of the Print Schema Framework.</span></span> <span data-ttu-id="16a0c-108">Сюда входят все стандартные типы элементов, а также возможности расширяемости платформы схемы печати.</span><span class="sxs-lookup"><span data-stu-id="16a0c-108">This includes all of the standard element types as well as the extensibility capabilities of the Print Schema Framework.</span></span> <span data-ttu-id="16a0c-109">Предполагается, что PrintTicket является автономным описанием того, как обрабатывается одна страница.</span><span class="sxs-lookup"><span data-stu-id="16a0c-109">A PrintTicket is assumed to be a self-contained description of how a single page is to be processed.</span></span> <span data-ttu-id="16a0c-110">Действия, связанные с извлечением и созданием такого элемента PrintTicket из определенного формата документа, здесь не рассматриваются.</span><span class="sxs-lookup"><span data-stu-id="16a0c-110">The steps involved in extracting and constructing such a PrintTicket from a particular document format are not covered here.</span></span>

<span data-ttu-id="16a0c-111">PrintTicket можно использовать для получения документа PrintCapabilities, описывающего характеристики устройства для конкретной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="16a0c-111">A PrintTicket can be used to obtain a PrintCapabilities document describing the characteristics of the device for a particular configuration.</span></span> <span data-ttu-id="16a0c-112">Кроме того, PrintTicket можно отправить с помощью набора инструкций по подготовке к просмотру, чтобы получить страницу выходных данных, отображаемых и обработанных в соответствии с конфигурацией, указанной в PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="16a0c-112">Alternatively, the PrintTicket can be submitted with a set of rendering instructions to produce a page of output rendered and processed according to the configuration specified in the PrintTicket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16a0c-113">См. также</span><span class="sxs-lookup"><span data-stu-id="16a0c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16a0c-114">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="16a0c-114">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



