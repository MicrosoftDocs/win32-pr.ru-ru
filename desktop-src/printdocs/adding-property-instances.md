---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: dac287a9-77ca-44d8-8019-b05e4c61dc52
title: Добавление экземпляров свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08e3df1b6c271c37c080968cc775ac11eba2e3ce
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104424142"
---
# <a name="adding-property-instances"></a><span data-ttu-id="36980-104">Добавление экземпляров свойств</span><span class="sxs-lookup"><span data-stu-id="36980-104">Adding Property Instances</span></span>

<span data-ttu-id="36980-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="36980-105">This topic is not current.</span></span> <span data-ttu-id="36980-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="36980-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="36980-107">Схема печати допускает наличие экземпляров свойств в экземпляре параметра.</span><span class="sxs-lookup"><span data-stu-id="36980-107">The Print Schema allows Property instances to be present in an Option instance.</span></span> <span data-ttu-id="36980-108">Экземпляры свойств, определенные в документе PrintCapabilities, не распространяются на экземпляры параметров, сохраненные в PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="36980-108">The Property instances defined in the PrintCapabilities document are not propagated to the Option instances saved in the PrintTicket.</span></span> <span data-ttu-id="36980-109">Элементы свойств не влияют на результат процесса оценки при сравнении двух экземпляров параметров, но Скоредпроперти экземпляры влияют на этот процесс.</span><span class="sxs-lookup"><span data-stu-id="36980-109">Property elements do not affect the result of the scoring process when two Option instances are compared, but ScoredProperty instances do affect this process.</span></span> <span data-ttu-id="36980-110">Все драйверы устройств, реализующие алгоритм оценки, должны соблюдать это соглашение.</span><span class="sxs-lookup"><span data-stu-id="36980-110">All device drivers that implement a scoring algorithm should observe this convention.</span></span> <span data-ttu-id="36980-111">Поставщики PrintCapabilities могут добавлять экземпляры свойств в параметр, если эти экземпляры относятся к конкретному параметру, а не к другим, или если поставщик намеревается, чтобы значение этого свойства отображалось для каждого параметра в функции.</span><span class="sxs-lookup"><span data-stu-id="36980-111">PrintCapabilities providers are permitted to add Property instances to an Option if these instances are specific to that particular Option and no others, or if the provider intends for the value of this Property to appear for every Option in the Feature.</span></span> <span data-ttu-id="36980-112">Например, предположим, что свойство Принтрате зависит от параметра, выбранного для функции Пажересолутион.</span><span class="sxs-lookup"><span data-stu-id="36980-112">For example, suppose that the PrintRate Property is dependent on the Option selected for the PageResolution Feature.</span></span> <span data-ttu-id="36980-113">Если свойство Принтрате было помещено на корневом уровне документа PrintCapabilities, оно будет одним значением и будет отражать только скорость печати для выбранного разрешения.</span><span class="sxs-lookup"><span data-stu-id="36980-113">If the PrintRate Property were placed at the root level of the PrintCapabilities document, it would be single-valued and would reflect only the print rate for the currently selected resolution.</span></span> <span data-ttu-id="36980-114">Однако если свойство Принтрате было помещено в каждый параметр Пажересолутион, то каждый экземпляр свойства Принтрате мог бы отразить скорость печати для параметра Пажересолутион, содержащего его.</span><span class="sxs-lookup"><span data-stu-id="36980-114">However, if the PrintRate Property were placed within each PageResolution Option, each instance of the PrintRate Property could reflect the print rate for the PageResolution Option that contained it.</span></span> <span data-ttu-id="36980-115">Документ PrintCapabilities будет содержать несколько определений для Принтрате, один из которых соответствует каждому параметру Пажересолутион.</span><span class="sxs-lookup"><span data-stu-id="36980-115">The PrintCapabilities document would contain multiple definitions for PrintRate, one corresponding to each PageResolution Option.</span></span> <span data-ttu-id="36980-116">Используя сокращенное представление, PrintCapabilities будет содержать:</span><span class="sxs-lookup"><span data-stu-id="36980-116">Using a shorthand representation, the PrintCapabilities would contain:</span></span>

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:string">800dpi</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:string">600dpi</psf:Value>
    </psf:ScoredProperty>
    <!-- Note: The following Property is not part of the Print Schema Framework -->
    <!-- It is included for illustration purposes. -->
    <!-- It is shown as a privately defined implementation-->
    <Property name="FabrikamES500:PrintRate">
      <Value xsi:type="string">20ppm</Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

<span data-ttu-id="36980-117">В некоторых ситуациях размещение свойства скорости печати в каждом варианте разрешения более удобно для клиента, поскольку клиент может быстро определить, что каждый вариант разрешения имеет скорость печати, без необходимости получения нового документа PrintCapabilities для каждого параметра разрешения.</span><span class="sxs-lookup"><span data-stu-id="36980-117">In some situations, placing a print rate Property within each resolution Option is more convenient for the client, because the client can determine at a glance the effect that each resolution Option has on the print rate, without the need for obtaining a new PrintCapabilities document for each resolution setting.</span></span>

<span data-ttu-id="36980-118">Обратите внимание, что экземпляры свойств также можно добавлять как дочерние элементы элементов компонента.</span><span class="sxs-lookup"><span data-stu-id="36980-118">Note also that Property instances can also be added as child elements of Feature elements.</span></span> <span data-ttu-id="36980-119">Это полезно, если имеются экземпляры свойств или значения экземпляров свойств, характерные для каждой функции.</span><span class="sxs-lookup"><span data-stu-id="36980-119">This is useful if there are Property instances or values of Property instances that are specific to each Feature.</span></span> <span data-ttu-id="36980-120">Например, может существовать свойство, указывающее, разрешено ли одновременное выделение одного параметра для функции или несколько параметров.</span><span class="sxs-lookup"><span data-stu-id="36980-120">For example, there might be a Property that specifies whether only one Option is permitted to be selected at one time for a Feature, or whether multiple Options may be selected.</span></span> <span data-ttu-id="36980-121">Выберите \_ один из них, выберите \_ значение много, которое используется в файлах PPD и ГПД.</span><span class="sxs-lookup"><span data-stu-id="36980-121">This is the PICK\_ONE, PICK\_MANY property used in PPD and GPD files.</span></span> <span data-ttu-id="36980-122">Поскольку некоторые экземпляры компонентов могут быть идентифицированы как \_ один выбор, а другие могут быть идентифицированы как \_ Дополнительные, это свойство должно быть определено для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="36980-122">Because some Feature instances might be identified as PICK\_ONE, while others might be identified as PICK\_MANY, this Property must be defined for each Feature.</span></span> <span data-ttu-id="36980-123">Нахождение свойства в качестве дочернего элемента компонента приводит к взаимосвязи между свойством и функцией.</span><span class="sxs-lookup"><span data-stu-id="36980-123">Locating the Property as a child element of the Feature produces the association between the Property and the Feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36980-124">См. также</span><span class="sxs-lookup"><span data-stu-id="36980-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36980-125">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="36980-125">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



