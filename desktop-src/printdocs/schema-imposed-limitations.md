---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 420c5c84-abb8-495a-9b74-dc19a16034fb
title: Ограничения Schema-Imposed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc283704ea96e3303de6755a217e454b506bdc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105693934"
---
# <a name="schema-imposed-limitations"></a><span data-ttu-id="0b105-104">Ограничения Schema-Imposed</span><span class="sxs-lookup"><span data-stu-id="0b105-104">Schema-Imposed Limitations</span></span>

<span data-ttu-id="0b105-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="0b105-105">This topic is not current.</span></span> <span data-ttu-id="0b105-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0b105-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0b105-107">Схема PrintCapabilities предоставляет авторам PrintCapabilities значительное количество гибкости и выразительности, которые можно использовать в описаниях устройств.</span><span class="sxs-lookup"><span data-stu-id="0b105-107">The PrintCapabilities Schema provides PrintCapabilities authors with a substantial amount of flexibility and expressiveness that can be utilized in device descriptions.</span></span> <span data-ttu-id="0b105-108">Однако зависимости конфигурации накладывают ограничение на эту гибкость и выразительность.</span><span class="sxs-lookup"><span data-stu-id="0b105-108">However, configuration dependencies impose a limitation on this flexibility and expressiveness.</span></span> <span data-ttu-id="0b105-109">Экземпляры Параметердеф, список элементов компонента, список экземпляров параметров в каждой функции, а также экземпляры Скоредпроперти в каждом параметре не должны содержать зависимости конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0b105-109">ParameterDef instances, the list of Feature elements, the list of Option instances within each Feature, and the ScoredProperty instances within each Option must not contain configuration dependencies.</span></span> <span data-ttu-id="0b105-110">Поставщик документов PrintCapabilities должен обнаружить недопустимые сочетания конфигураций и разрешить их.</span><span class="sxs-lookup"><span data-stu-id="0b105-110">The PrintCapabilities document provider must detect invalid combinations of configurations and must resolve them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b105-111">См. также</span><span class="sxs-lookup"><span data-stu-id="0b105-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b105-112">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="0b105-112">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



