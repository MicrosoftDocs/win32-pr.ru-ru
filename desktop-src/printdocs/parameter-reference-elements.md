---
description: Прочитайте об элементах ParameterRef в платформе схемы печати. Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 78df6acf-eb4e-46c1-bf1d-c0a99cf49bff
title: Элементы ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2935317bc4107e2071911ab1df826426b2bcec17
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396529"
---
# <a name="parameterref-elements"></a><span data-ttu-id="43919-105">Элементы ParameterRef</span><span class="sxs-lookup"><span data-stu-id="43919-105">ParameterRef Elements</span></span>

<span data-ttu-id="43919-106">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="43919-106">This topic is not current.</span></span> <span data-ttu-id="43919-107">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="43919-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="43919-108">Элементы ParameterRef специально применяются к элементам Option, что позволяет этому элементу Option ссылаться на определенный элемент Параметердеф.</span><span class="sxs-lookup"><span data-stu-id="43919-108">ParameterRef elements specifically apply to Option elements, allowing the ability for that Option element to refer to a particular ParameterDef element.</span></span> <span data-ttu-id="43919-109">Для этих элементов Option элемент Скоредпроперти, характеризующий параметр, не жестко закодирован в документе PrintCapabilities как значение, а является переменной.</span><span class="sxs-lookup"><span data-stu-id="43919-109">For these Option elements, a ScoredProperty element that characterizes the Option is not hard-coded in the PrintCapabilities document as a Value, but instead is variable.</span></span> <span data-ttu-id="43919-110">Чтобы включить эту вариативность, эти элементы Скоредпроперти содержат элемент ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="43919-110">To enable this variability, these ScoredProperty elements contain a ParameterRef element.</span></span> <span data-ttu-id="43919-111">Элемент Скоредпроперти не может содержать как элемент value, так и элемент ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="43919-111">A ScoredProperty element may not contain both a Value element and a ParameterRef element.</span></span> <span data-ttu-id="43919-112">Элементы Option, содержащие один или несколько элементов ParameterRef, называются параметризованными элементами Option.</span><span class="sxs-lookup"><span data-stu-id="43919-112">Option elements containing one or more ParameterRef elements are called parameterized Option elements.</span></span>

<span data-ttu-id="43919-113">Платформа схемы печати позволяет элементу Option содержать любое количество элементов Скоредпроперти, ссылающихся на элементы параметров, а также любое количество элементов Скоредпроперти, содержащих элементы значения.</span><span class="sxs-lookup"><span data-stu-id="43919-113">The Print Schema Framework allows an Option element to contain any number of ScoredProperty elements that refer to Parameter elements, together with any number of ScoredProperty elements that contain Value elements.</span></span> <span data-ttu-id="43919-114">Платформа также позволяет любому количеству элементов компонента содержать параметризованные элементы Option, а для каждого элемента Feature разрешено любое количество параметризованных элементов Option.</span><span class="sxs-lookup"><span data-stu-id="43919-114">The Framework also allows any number of Feature elements to contain parameterized Option elements, and any number of parameterized Option elements are permitted for each Feature element.</span></span> <span data-ttu-id="43919-115">Кроме того, одна и та же конструкция параметра может называться несколькими различными элементами Option, элементами Option, которые могут принадлежать к одному или разным функциональным элементам.</span><span class="sxs-lookup"><span data-stu-id="43919-115">Also, the same parameter construct can be referred to by several different Option elements, Option elements that can belong to the same or different Feature elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43919-116">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="43919-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43919-117">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="43919-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



