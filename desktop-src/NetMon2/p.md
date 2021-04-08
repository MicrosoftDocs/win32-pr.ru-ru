---
description: Глоссарий терминов сетевой монитор, начинающихся с буквы P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 321398fb-683f-4fb1-b6b7-c7826811cacd
title: P (сетевой монитор)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a95ed739acb6f4a59cf8c7a7edb760547f6469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080361"
---
# <a name="p-network-monitor"></a><span data-ttu-id="1dbbe-103">P (сетевой монитор)</span><span class="sxs-lookup"><span data-stu-id="1dbbe-103">P (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="1dbbe-104"><span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**пакетов**</span><span class="sxs-lookup"><span data-stu-id="1dbbe-104"><span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**packet**</span></span>
</dt> <dd>

<span data-ttu-id="1dbbe-105">См. раздел [*Frame*](f.md).</span><span class="sxs-lookup"><span data-stu-id="1dbbe-105">See [*frame*](f.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dbbe-106"><span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**средство синтаксического анализа**</span><span class="sxs-lookup"><span data-stu-id="1dbbe-106"><span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**parser**</span></span>
</dt> <dd>

<span data-ttu-id="1dbbe-107">Компонент, который обнаруживает конкретный протокол в отложенной записи.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-107">A component that detects a specific protocol in a delayed capture.</span></span> <span data-ttu-id="1dbbe-108">Каждое средство синтаксического анализа может обнаружить один протокол.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-108">Each parser can detect one protocol.</span></span> <span data-ttu-id="1dbbe-109">Однако одна библиотека DLL средства синтаксического анализа может содержать несколько синтаксических анализаторов.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-109">However, one parser DLL may contain multiple parsers.</span></span> <span data-ttu-id="1dbbe-110">Также называется средством синтаксического анализа протокола.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-110">Also called a protocol parser.</span></span>

</dd> <dt>

<span data-ttu-id="1dbbe-111"><span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**</span><span class="sxs-lookup"><span data-stu-id="1dbbe-111"><span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**</span></span>
</dt> <dd>

<span data-ttu-id="1dbbe-112">Файл инициализации сетевой монитор, содержащий список всех установленных средств синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-112">A Network Monitor initialization file that contains a list of all the installed parsers.</span></span> <span data-ttu-id="1dbbe-113">Для каждого средства синтаксического анализа существует строка комментария, описывающая средство синтаксического анализа, следующий набор анализатора и файл справки, связанный с анализатором.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-113">For each parser there is a comment string that describes the parser, the follow set of the parser, and any Help file associated with the parser.</span></span> <span data-ttu-id="1dbbe-114">INI-файл средства синтаксического анализа обновляется, когда сетевой монитор вызывает **парсераутоинсталлинфо** или если DLL-библиотека анализатора вызывает **креатехандоффтабле**.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-114">The parser INI file is updated when Network Monitor calls **ParserAutoInstallInfo**, or when the parser DLL calls **CreateHandoffTable**.</span></span>

</dd> <dt>

<span data-ttu-id="1dbbe-115"><span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**Производительности**</span><span class="sxs-lookup"><span data-stu-id="1dbbe-115"><span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**Perfmon**</span></span>
</dt> <dd>

<span data-ttu-id="1dbbe-116">Программное средство, позволяющее просматривать переменные, связанные с производительностью сети, которые указывают на активность процесса.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-116">A software tool that allows you to view network performance-related variables that identify the activity of a process.</span></span>

</dd> <dt>

<span data-ttu-id="1dbbe-117"><span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**неизбирательный режим**</span><span class="sxs-lookup"><span data-stu-id="1dbbe-117"><span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**promiscuous mode**</span></span>
</dt> <dd>

<span data-ttu-id="1dbbe-118">Состояние, в котором плата сетевого адаптера копирует все кадры, передаваемые по сети, независимо от адреса назначения в локальном буфере.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-118">A state in which a network adapter card copies all the frames that pass over the network, regardless of the destination address to a local buffer.</span></span> <span data-ttu-id="1dbbe-119">Этот режим позволяет сетевой монитор записывать и отображать весь сетевой трафик.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-119">This mode enables Network Monitor to capture and display all network traffic.</span></span>

</dd> <dt>

<span data-ttu-id="1dbbe-120"><span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**свойства**</span><span class="sxs-lookup"><span data-stu-id="1dbbe-120"><span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="1dbbe-121">Элемент протокола в средстве синтаксического анализа, описывающий поле данных в кадре, отправляемом с помощью этого протокола.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-121">A protocol element in a parser that describes a data field within a frame that is sent by using that protocol.</span></span>

</dd> <dt>

<span data-ttu-id="1dbbe-122"><span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**база данных свойств**</span><span class="sxs-lookup"><span data-stu-id="1dbbe-122"><span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**property database**</span></span>
</dt> <dd>

<span data-ttu-id="1dbbe-123">Внутренняя база данных, определяющая все свойства, поддерживаемые конкретным протоколом.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-123">An internal database that defines all the properties that a specific protocol supports.</span></span> <span data-ttu-id="1dbbe-124">База данных свойств содержит структуру **PROPERTYINFO** для каждого свойства, определяемого анализатором.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-124">The property database contains a **PROPERTYINFO** structure for each property that the parser defines.</span></span> <span data-ttu-id="1dbbe-125">Сетевой монитор использует сведения в базе данных при присоединении определения свойства к экземпляру свойства, а также при форматировании данных свойства, отображаемых в области сведений пользовательского интерфейса сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-125">Network Monitor uses the information in the database when it attaches a property definition to an instance of the property, and when it formats the property data that is displayed in the details pane of the Network Monitor UI.</span></span>

</dd> <dt>

<span data-ttu-id="1dbbe-126"><span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**уровень протокола**</span><span class="sxs-lookup"><span data-stu-id="1dbbe-126"><span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**protocol level**</span></span>
</dt> <dd>

<span data-ttu-id="1dbbe-127">Логическое группирование свойств протокола.</span><span class="sxs-lookup"><span data-stu-id="1dbbe-127">A logical grouping of protocol properties.</span></span>

</dd> </dl>

 

 



