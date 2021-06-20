---
description: Платформа схемы печати определяет пространство имен, включающее элементы и XML-атрибуты, определенные в ключевых словах «Печать схемы».
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: Объекты и имена, определенные в ключевых словах «Печать схемы»
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73aabdac90de6743388ca1f4d44e1ad52c020dbd
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408557"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a><span data-ttu-id="77276-103">Объекты и имена, определенные в ключевых словах «Печать схемы»</span><span class="sxs-lookup"><span data-stu-id="77276-103">Objects and Names Defined in the Print Schema Keywords</span></span>

<span data-ttu-id="77276-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="77276-104">This topic is not current.</span></span> <span data-ttu-id="77276-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="77276-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="77276-106">Платформа схемы печати определяет пространство имен, включающее элементы и XML-атрибуты, определенные в ключевых словах «Печать схемы».</span><span class="sxs-lookup"><span data-stu-id="77276-106">The Print Schema Framework defines a namespace that includes the elements and XML attributes defined in the Print Schema Keywords.</span></span> <span data-ttu-id="77276-107">Сюда входят такие элементы, как функция, параметр и Скоредпроперти; имена атрибутов, такие как имя и распространение; значения и для атрибутов XML, таких как CONSTRAINED.</span><span class="sxs-lookup"><span data-stu-id="77276-107">This includes elements such as Feature, Option, and ScoredProperty; attribute names such as name and propagate; and values for XML attributes such as constrained.</span></span> <span data-ttu-id="77276-108">Иными словами, каждое использование имени, определенного в ключевых словах схемы Print, должно быть явно дополнено этим пространством имен или должно быть неявно связано с этим пространством имен с помощью атрибута xmlns по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="77276-108">In other words, every use of a name that is defined in the Print Schema Keywords should be explicitly qualified with this namespace, or should be implicitly associated with this namespace by the use of a default xmlns attribute.</span></span> <span data-ttu-id="77276-109">В документе «печать ключевых слов схемы» определяются экземпляры открытых элементов, которые могут присутствовать в любом заданном контексте или расположении.</span><span class="sxs-lookup"><span data-stu-id="77276-109">The Print Schema Keywords document defines the public element instances that may appear in any given context or location.</span></span> <span data-ttu-id="77276-110">Экземпляры элементов должны отображаться только в контексте или расположении, определенном в платформе схемы печати.</span><span class="sxs-lookup"><span data-stu-id="77276-110">Element instances must appear only within the context or location designated in the Print Schema Framework.</span></span> <span data-ttu-id="77276-111">Например, <ПСФ: параметр Name = "PSK: Letter" > экземпляр, определенный в ключевом слове Print Schema, должен появиться в <ПСФ: Feature Name = "PSK: Пажемедиасизе" > (также определено в ключевых словах схемы печати).</span><span class="sxs-lookup"><span data-stu-id="77276-111">For example, the <psf:Option name= "psk:Letter"> instance that is defined in the Print Schema Keywords must appear within the <psf:Feature name = "psk:PageMediaSize"> instance (also defined in the Print Schema Keywords).</span></span> <span data-ttu-id="77276-112">У вас нет возможности использовать данный экземпляр параметра вне указанного контекста.</span><span class="sxs-lookup"><span data-stu-id="77276-112">You do not have the freedom to use a given Option instance outside of its specified context.</span></span>

<span data-ttu-id="77276-113">Закрыто определенные экземпляры элементов могут появляться в любом месте, если тип элемента отображается в контексте, разрешенном платформой схемы печати.</span><span class="sxs-lookup"><span data-stu-id="77276-113">Privately-defined element instances may appear anywhere as long as the element type appears in a context allowed by the Print Schema Framework.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77276-114">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="77276-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77276-115">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="77276-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



