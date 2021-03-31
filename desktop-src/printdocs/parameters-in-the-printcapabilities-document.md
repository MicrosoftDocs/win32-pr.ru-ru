---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: Параметры в документе PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfcfee581014bdb57ff70adebaf5f4c8b6fedc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351832"
---
# <a name="parameters-in-the-printcapabilities-document"></a><span data-ttu-id="a73bd-104">Параметры в документе PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="a73bd-104">Parameters in the PrintCapabilities Document</span></span>

<span data-ttu-id="a73bd-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="a73bd-105">This topic is not current.</span></span> <span data-ttu-id="a73bd-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a73bd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a73bd-107">Как обсуждалось в [элементах ссылки на параметры](parameter-reference-elements.md), на элементы параметеринит могут ссылаться в экземплярах параметров, но конструкция параметра также имеет использование, которое не зависит от этого типа элемента.</span><span class="sxs-lookup"><span data-stu-id="a73bd-107">As discussed in [Parameter Reference Elements](parameter-reference-elements.md), ParameterInit elements may be referenced from within Option instances, but the parameter construct also has a use that is independent of this type of element.</span></span>

<span data-ttu-id="a73bd-108">Примером атрибута конфигурации устройства, который хорошо подходит для представления параметров, является Копикаунт.</span><span class="sxs-lookup"><span data-stu-id="a73bd-108">An example of a device configuration attribute that is well suited for parameter representation is CopyCount.</span></span> <span data-ttu-id="a73bd-109">Допустимые значения для этого атрибута конфигурации устройства можно легко и четко определить, не перечисляя их явным образом.</span><span class="sxs-lookup"><span data-stu-id="a73bd-109">The allowed values for this device configuration attribute can be easily and concisely defined without listing each of them explicitly.</span></span> <span data-ttu-id="a73bd-110">Несмотря на то, что для перечисления каждого значения Копикаунт можно использовать собственный вариант, некоторые атрибуты конфигурации устройства просто не могут быть представлены с помощью конструкции "функция-параметр".</span><span class="sxs-lookup"><span data-stu-id="a73bd-110">Although it would be possible, though tedious, to list each CopyCount value in its own Option, some device configuration attributes simply cannot be represented using a Feature/Option construct.</span></span> <span data-ttu-id="a73bd-111">В качестве примера рассмотрим устройство, которое принимает текстовую строку, которая затем используется для создания виртуального водяного знака на каждой странице выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a73bd-111">As an example, consider a device that accepts a text string that is then used to produce a virtual watermark on each output page.</span></span> <span data-ttu-id="a73bd-112">Набор всех возможных текстовых строк нельзя легко перечислить явным образом, но текстовую строку можно легко описать с помощью элемента Параметердеф.</span><span class="sxs-lookup"><span data-stu-id="a73bd-112">The set of all possible text strings cannot easily be explicitly enumerated, but the text string can easily be described using a ParameterDef element.</span></span>

<span data-ttu-id="a73bd-113">В документе о ключевых словах «Печать схемы» определено несколько часто используемых конструкций параметров, но поставщики PrintCapabilities могут самостоятельно определять дополнительные собственные конструкции.</span><span class="sxs-lookup"><span data-stu-id="a73bd-113">The Print Schema Keywords document defines a number of commonly used parameter constructs, but PrintCapabilities providers are free to define additional ones of their own.</span></span> <span data-ttu-id="a73bd-114">Однако эти закрытые конструкции параметров не переносятся на другие устройства из-за того факта, что PrintCapabilities документ, предоставленный другой стороной, не определяет такую конструкцию параметра.</span><span class="sxs-lookup"><span data-stu-id="a73bd-114">However, these privately-defined parameter constructs are not portable to other devices, due to the fact that a PrintCapabilities document provided by another party does not define such a parameter construct.</span></span> <span data-ttu-id="a73bd-115">Независимо от того, определена ли схема или частный тип, экземпляр Параметердеф должен присутствовать в документе PrintCapabilities до того, как параметр распознается и используется клиентами.</span><span class="sxs-lookup"><span data-stu-id="a73bd-115">Whether schema-defined or privately-defined, the ParameterDef instance must be present in the PrintCapabilities document before the parameter is recognized and used by clients.</span></span> <span data-ttu-id="a73bd-116">Эти параметры называются *назначенными параметрами*.</span><span class="sxs-lookup"><span data-stu-id="a73bd-116">These parameters are referred to as *designated parameters*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a73bd-117">См. также</span><span class="sxs-lookup"><span data-stu-id="a73bd-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a73bd-118">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="a73bd-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



