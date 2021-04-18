---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 2377763b-9b3b-49ec-ab6c-476b8009ddcb
title: Обязанности потребителей документа PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b74cfc1885ecc5599365bc6eadcef30ef4c4ae3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105713323"
---
# <a name="responsibilities-of-consumers-of-the-printcapabilities-document"></a><span data-ttu-id="f398b-104">Обязанности потребителей документа PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="f398b-104">Responsibilities of Consumers of the PrintCapabilities Document</span></span>

<span data-ttu-id="f398b-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="f398b-105">This topic is not current.</span></span> <span data-ttu-id="f398b-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f398b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f398b-107">Потребители документов PrintCapabilities имеют определенные обязательства, которые они должны правилами, прежде чем они смогут использовать документ PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="f398b-107">Consumers of PrintCapabilities documents have certain obligations they must uphold before they can use a PrintCapabilities document.</span></span> <span data-ttu-id="f398b-108">Следующие требования применяются к клиентам PrintCapabilities документа.</span><span class="sxs-lookup"><span data-stu-id="f398b-108">The following requirements apply to clients of a PrintCapabilities document.</span></span>

-   <span data-ttu-id="f398b-109">Они не должны отклонять или не обрабатывать синтаксически допустимые PrintCapabilities; то есть любой документ PrintCapabilities, который соответствует схеме PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="f398b-109">They must not reject or fail to process any syntactically valid PrintCapabilities; that is, any PrintCapabilities document that conforms to the PrintCapabilities Schema.</span></span>

-   <span data-ttu-id="f398b-110">Они должны иметь возможность обойти непредвиденное присутствие или отсутствие частного определенного содержимого.</span><span class="sxs-lookup"><span data-stu-id="f398b-110">They must be able to work around the unexpected presence or absence of privately-defined content.</span></span> <span data-ttu-id="f398b-111">Это включает в себя закрытое содержимое, которое отображается в экземплярах элементов, определяемых схемой печати.</span><span class="sxs-lookup"><span data-stu-id="f398b-111">This includes privately-defined content that appears within instances of Print Schema-defined elements.</span></span>

-   <span data-ttu-id="f398b-112">Они должны иметь возможность обойти необязательное содержимое схемы печати, которое отсутствует.</span><span class="sxs-lookup"><span data-stu-id="f398b-112">They must be able to work around optional Print Schema content that is absent.</span></span>

-   <span data-ttu-id="f398b-113">Они должны знать, когда следует запрашивать новый документ.</span><span class="sxs-lookup"><span data-stu-id="f398b-113">They must be aware of when to request a new document.</span></span>

    -   <span data-ttu-id="f398b-114">Значения экземпляров свойств зависят от конфигурации (следовательно, зависит от моментального снимка).</span><span class="sxs-lookup"><span data-stu-id="f398b-114">Values of Property instances are configuration-dependent (hence, snapshot-dependent).</span></span> <span data-ttu-id="f398b-115">При доступе к экземпляру свойства необходимо обновить моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="f398b-115">You must update the snapshot when you access a Property instance.</span></span>

    -   <span data-ttu-id="f398b-116">Экземпляры компонентов, параметров и Скоредпроперти, которые должны быть скопированы в PrintTicket, являются статическими.</span><span class="sxs-lookup"><span data-stu-id="f398b-116">Feature, Option and ScoredProperty instances that are to be copied to a PrintTicket are by definition static.</span></span> <span data-ttu-id="f398b-117">Это значит, что они не (и не должны быть) зависят от конфигурации устройства.</span><span class="sxs-lookup"><span data-stu-id="f398b-117">That is, they are not (and must not be) dependent on the device configuration.</span></span> <span data-ttu-id="f398b-118">При доступе к экземплярам этих типов не требуется получать новый документ PrintCapabilities при изменении конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f398b-118">If you access any instances of these types, you do not need to obtain a new PrintCapabilities document when the configuration changes.</span></span>

-   <span data-ttu-id="f398b-119">Потребители PrintCapabilities, которые являются клиентами ПОЛЬЗОВАТЕЛЬСКОГО интерфейса, должны иметь возможность использовать информацию в документе PrintCapabilities для создания пользовательского интерфейса и создания допустимого PrintTicket из выбора пользователя.</span><span class="sxs-lookup"><span data-stu-id="f398b-119">Consumers of PrintCapabilities that are user interface (UI) clients must be able to use information in a PrintCapabilities document to construct a user interface and to construct a valid PrintTicket from the user selections.</span></span> <span data-ttu-id="f398b-120">Сюда входит знание того, какие экземпляры Параметеринит должны быть указаны, и проверка указанных экземпляров.</span><span class="sxs-lookup"><span data-stu-id="f398b-120">This includes knowing which ParameterInit instances must be specified, and validating those instances that are specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f398b-121">См. также</span><span class="sxs-lookup"><span data-stu-id="f398b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f398b-122">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="f398b-122">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



