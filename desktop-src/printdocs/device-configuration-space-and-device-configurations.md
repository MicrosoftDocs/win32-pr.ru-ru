---
title: Область конфигурации устройства
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 598299c3-159f-4cad-b6a5-d282cd5bb4a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120e12b6480675dba6e735390f4820a8782edc5c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105693896"
---
# <a name="device-configuration-space-and-device-configurations"></a><span data-ttu-id="f15f4-104">Пространство конфигурации устройства и конфигурации устройств</span><span class="sxs-lookup"><span data-stu-id="f15f4-104">Device Configuration Space and Device Configurations</span></span>

<span data-ttu-id="f15f4-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="f15f4-105">This topic is not current.</span></span> <span data-ttu-id="f15f4-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f15f4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f15f4-107">*Пространство конфигурации* устройства — это набор всех возможных значений, которые могут быть назначены всем атрибутам устройства.</span><span class="sxs-lookup"><span data-stu-id="f15f4-107">A device's *configuration space* is the set of all possible values that can be assigned to all of the attributes of the device.</span></span> <span data-ttu-id="f15f4-108">Ниже приведены две наиболее важные причины для описания пространства конфигурации устройства в PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="f15f4-108">The two most important reasons to describe the configuration space of the device in the PrintCapabilities are as follows.</span></span>

1.  <span data-ttu-id="f15f4-109">Эта информация значительно повышает понимание возможностей устройства.</span><span class="sxs-lookup"><span data-stu-id="f15f4-109">The information contributes significantly to an increased understanding of the device's capabilities.</span></span> <span data-ttu-id="f15f4-110">Эта информация упрощает для клиента PrintCapabilities создание элементов пользовательского интерфейса, что упрощает для конечных пользователей выбор конкретной конфигурации для обработки задания служб.</span><span class="sxs-lookup"><span data-stu-id="f15f4-110">This information makes it easier for a client of the PrintCapabilities to generate user interface (UI) elements, which makes it easier for the end user to select a particular configuration to process a job.</span></span> <span data-ttu-id="f15f4-111">Предоставляя более подробные сведения о возможностях устройства для приложения и в конечном итоге конечному пользователю, цель печати пользователя может быть более эффективной.</span><span class="sxs-lookup"><span data-stu-id="f15f4-111">By providing more details of the device's capabilities to the application and ultimately to the end user, the user's printing intent can be more effectively fulfilled.</span></span>

2.  <span data-ttu-id="f15f4-112">Некоторые свойства устройства, представленные в PrintCapabilities, могут зависеть от конкретной конфигурации, выбранной клиентом.</span><span class="sxs-lookup"><span data-stu-id="f15f4-112">Certain device properties presented in the PrintCapabilities might be dependent on the particular configuration selected by the client.</span></span>

<span data-ttu-id="f15f4-113">Некоторые сведения не должны включаться в PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="f15f4-113">Some information should not be incorporated into the PrintCapabilities.</span></span> <span data-ttu-id="f15f4-114">Сюда входят сведения, которые не влияют на способ создания задания, не накладывают ограничения на способ создания задания, а также на свойства устройства.</span><span class="sxs-lookup"><span data-stu-id="f15f4-114">This includes information that does not affect the way a job is created, does not impose constraints on the way a job is created, nor otherwise affects the device properties.</span></span> <span data-ttu-id="f15f4-115">Например, устройство может сообщать сведения о состоянии, например набор заданий, ожидающих обработки.</span><span class="sxs-lookup"><span data-stu-id="f15f4-115">For example, a device might be able to report status information, such as the set of jobs waiting to be processed.</span></span> <span data-ttu-id="f15f4-116">Эта информация не влияет на информацию, необходимую для форматирования задания, и не предоставляет указания о возможностях устройства.</span><span class="sxs-lookup"><span data-stu-id="f15f4-116">This information has no effect on the information needed to format the job, nor does it provide any indication of the capabilities available in the device.</span></span> <span data-ttu-id="f15f4-117">По этой причине этот тип сведений не обязательно должен присутствовать в PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="f15f4-117">For this reason, this type of information does not need to be present in the PrintCapabilities.</span></span>

## <a name="device-constraints"></a><span data-ttu-id="f15f4-118">Ограничения устройств</span><span class="sxs-lookup"><span data-stu-id="f15f4-118">Device Constraints</span></span>

<span data-ttu-id="f15f4-119">Многие устройства не поддерживают все возможные конфигурации в конфигурационной области из-за ограничения на устройстве.</span><span class="sxs-lookup"><span data-stu-id="f15f4-119">Many devices do not support all possible configurations in the configuration space due to a constraint on the device.</span></span> <span data-ttu-id="f15f4-120">Например, устройство может быть ограничено выполнением двусторонней печати на прозрачном носителе.</span><span class="sxs-lookup"><span data-stu-id="f15f4-120">For example, a device can be constrained from performing duplex printing on transparent media.</span></span> <span data-ttu-id="f15f4-121">Ограничение может представлять физическое ограничение: некоторые типы носителей просто слишком жесткы для перемещения по определенным путям бумаги на устройстве и поэтому не могут быть помещены в некоторые входные слоты или направляться в некоторые выходные ячейки. В настоящее время ответственность за проверку конфигурации, представленной входным объектом PrintTicket, несет поставщик PrintCapabilities или PrintTicket, чтобы убедиться, что он не представляет недопустимую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="f15f4-121">A constraint can represent a physical limitation: some media types are simply too rigid to travel through certain paper paths in the device, and so cannot be placed in some input slots or be routed to some output bins. Currently it is the responsibility of the PrintCapabilities or PrintTicket provider to validate the configuration represented by the input PrintTicket, to verify that it does not represent an invalid configuration.</span></span> <span data-ttu-id="f15f4-122">Если конфигурация недопустима, поставщик PrintCapabilities или PrintTicket должен изменить конфигурацию таким образом, чтобы она стала допустимой.</span><span class="sxs-lookup"><span data-stu-id="f15f4-122">If the configuration is invalid, the PrintCapabilities or PrintTicket provider should modify the configuration in such a way that it becomes valid.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f15f4-123">См. также</span><span class="sxs-lookup"><span data-stu-id="f15f4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f15f4-124">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="f15f4-124">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



