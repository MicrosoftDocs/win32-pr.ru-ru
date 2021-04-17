---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: d67518e3-c379-4a50-aeda-31afaa7f05dd
title: Синтаксис схемы печати
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2503b3f44ff8b4bdda41f0feefe374c27d78bd41
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105693928"
---
# <a name="syntax-of-the-print-schema"></a><span data-ttu-id="8854e-104">Синтаксис схемы печати</span><span class="sxs-lookup"><span data-stu-id="8854e-104">Syntax of the Print Schema</span></span>

<span data-ttu-id="8854e-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="8854e-105">This topic is not current.</span></span> <span data-ttu-id="8854e-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8854e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8854e-107">Схема печати выражается в синтаксисе XML.</span><span class="sxs-lookup"><span data-stu-id="8854e-107">The Print Schema is expressed in XML syntax.</span></span> <span data-ttu-id="8854e-108">Поэтому читатели должны иметь представление о синтаксисе XML и таких терминах, как элемент, тег элемента, содержимое элемента, атрибут и пространство имен.</span><span class="sxs-lookup"><span data-stu-id="8854e-108">Readers are therefore expected to be familiar with XML syntax and terms such as element, element tag, element content, attribute, and namespace.</span></span> <span data-ttu-id="8854e-109">Платформа для печати схемы состоит из небольшого числа типов элементов. Каждый тип элемента служит определенной цели в технологиях, созданных на основе схемы печати.</span><span class="sxs-lookup"><span data-stu-id="8854e-109">The Print Schema Framework is composed of a small number of element types; each element type serves a specific purpose in the technologies built on the Print Schema.</span></span>

<span data-ttu-id="8854e-110">Типы элементов различаются по тегу XML-элемента.</span><span class="sxs-lookup"><span data-stu-id="8854e-110">Element types are distinguished by their XML element tag.</span></span> <span data-ttu-id="8854e-111">Платформа схемы печати определяет общую структуру и организацию зависимых технологий, обозначая каждый тип элемента, какие типы элементов допускаются в качестве дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="8854e-111">The Print Schema Framework defines the overall structure and organization of the dependent technologies, by denoting for each element type which element types are allowed as child elements.</span></span>

<span data-ttu-id="8854e-112">Многие типы элементов отличаются от других тем же типом с помощью атрибута Name, который играет важную роль в схеме.</span><span class="sxs-lookup"><span data-stu-id="8854e-112">Many element types are differentiated from others of the same type by the name attribute, which plays a significant role in the schema.</span></span> <span data-ttu-id="8854e-113">Атрибут Name служит для обнаружения экземпляров каждого типа элемента.</span><span class="sxs-lookup"><span data-stu-id="8854e-113">The name attribute serves to identify instances of each element type.</span></span> <span data-ttu-id="8854e-114">Ключевые слова схемы Print определяют набор значений для атрибута Name для многих типов элементов.</span><span class="sxs-lookup"><span data-stu-id="8854e-114">The Print Schema Keywords defines a set of values for the name attribute for many of the element types.</span></span> <span data-ttu-id="8854e-115">В большинстве случаев поставщики могут назначать атрибуту name собственные значения.</span><span class="sxs-lookup"><span data-stu-id="8854e-115">In most cases, providers can assign their own values to the name attribute.</span></span> <span data-ttu-id="8854e-116">Им нужно только убедиться в том, что значения QName определены в пространстве имен, уникальном для поставщика.</span><span class="sxs-lookup"><span data-stu-id="8854e-116">They need only ensure the values are XML QNames qualified with a namespace that is unique to the provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8854e-117">См. также</span><span class="sxs-lookup"><span data-stu-id="8854e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8854e-118">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="8854e-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



