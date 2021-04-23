---
description: Поставщик SNMP позволяет клиентским приложениям получать доступ к информации SNMP с помощью инструментарий управления Windows (WMI) (WMI).
ms.assetid: 71e758d9-2ea6-42f5-93b4-d370a96b10cf
ms.tgt_platform: multiple
title: WMI и SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ea7e8385e1fb95ac20d14af31f82444350e044
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272753"
---
# <a name="wmi-and-snmp"></a><span data-ttu-id="cbb94-103">WMI и SNMP</span><span class="sxs-lookup"><span data-stu-id="cbb94-103">WMI and SNMP</span></span>

<span data-ttu-id="cbb94-104">Поставщик SNMP позволяет клиентским приложениям получать доступ к информации SNMP с помощью инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="cbb94-104">The Simple Network Management Protocol (SNMP) provider allows client applications to access SNMP information through Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="cbb94-105">Поставщик SNMP не устанавливается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cbb94-105">The SNMP provider is not installed by default.</span></span> <span data-ttu-id="cbb94-106">Дополнительные сведения об установке поставщика см. в разделе [Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="cbb94-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

<span data-ttu-id="cbb94-107">Протокол SNMP использует схему для определения объектов.</span><span class="sxs-lookup"><span data-stu-id="cbb94-107">Simple Network Management Protocol (SNMP) uses a schema to define objects.</span></span> <span data-ttu-id="cbb94-108">Схема отличается от схемы, используемой в WMI.</span><span class="sxs-lookup"><span data-stu-id="cbb94-108">The schema is different from the schema used in WMI.</span></span> <span data-ttu-id="cbb94-109">Схема CLR и SNMPv2C называется структурой управляющих данных (SMI) и упаковывается в виде файлов MIB.</span><span class="sxs-lookup"><span data-stu-id="cbb94-109">The SNMPv1 and SNMPv2C schema is called the Structure of Management Information (SMI), and is packaged as Management Information Base (MIB) files.</span></span> <span data-ttu-id="cbb94-110">Файлы MIB определяют объекты на стандартном языке — абстрактный синтаксис Notation 1 (ASN. 1), а также ряд определений макросов, которые служат шаблонами для описания объектов.</span><span class="sxs-lookup"><span data-stu-id="cbb94-110">MIB files define objects using a standard language—Abstract Syntax Notation 1 (ASN.1)—and a number of macro definitions that serve as templates for describing the objects.</span></span> <span data-ttu-id="cbb94-111">Макросы предоставляют такие сведения, как имя объекта, идентификатор, синтаксис, описание, права доступа, операции протокола и кодировка протокола.</span><span class="sxs-lookup"><span data-stu-id="cbb94-111">The macros provide information such as the object name, identifier, syntax, description, access rights, protocol operations, and protocol encoding.</span></span> <span data-ttu-id="cbb94-112">В следующей таблице указано, как поставщик SNMP обрабатывает различные аспекты объекта MIB.</span><span class="sxs-lookup"><span data-stu-id="cbb94-112">The following table lists how the SNMP provider handles different aspects of a MIB object.</span></span>



| <span data-ttu-id="cbb94-113">Раздел</span><span class="sxs-lookup"><span data-stu-id="cbb94-113">Topic</span></span>                                                    | <span data-ttu-id="cbb94-114">Описание</span><span class="sxs-lookup"><span data-stu-id="cbb94-114">Description</span></span>                                                 |
|----------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="cbb94-115">Макрос типа уведомления</span><span class="sxs-lookup"><span data-stu-id="cbb94-115">NOTIFICATION-TYPE Macro</span></span>](notification-type-macro.md)   | <span data-ttu-id="cbb94-116">Сопоставление макросов **типа уведомления** из SNMP с WMI.</span><span class="sxs-lookup"><span data-stu-id="cbb94-116">How the **NOTIFICATION-TYPE** macro maps from SNMP to WMI.</span></span>  |
| [<span data-ttu-id="cbb94-117">Макрос типа OBJECT-TYPE</span><span class="sxs-lookup"><span data-stu-id="cbb94-117">OBJECT-TYPE Macro</span></span>](object-type-macro.md)               | <span data-ttu-id="cbb94-118">Способ сопоставления макросов **объектов** из SNMP с WMI.</span><span class="sxs-lookup"><span data-stu-id="cbb94-118">How the **OBJECT-TYPE** macro maps from SNMP to WMI.</span></span>        |
| [<span data-ttu-id="cbb94-119">Макрос ТЕКСТОВОГО соглашения</span><span class="sxs-lookup"><span data-stu-id="cbb94-119">TEXTUAL-CONVENTION Macro</span></span>](textual-convention-macro.md) | <span data-ttu-id="cbb94-120">Сопоставление макросов **ТЕКСТОВОГО соглашения** из SNMP с WMI.</span><span class="sxs-lookup"><span data-stu-id="cbb94-120">How the **TEXTUAL-CONVENTION** macro maps from SNMP to WMI.</span></span> |
| [<span data-ttu-id="cbb94-121">Макрос типа ЛОВУШКи</span><span class="sxs-lookup"><span data-stu-id="cbb94-121">TRAP-TYPE Macro</span></span>](trap-type-macro.md)                   | <span data-ttu-id="cbb94-122">Сопоставление макросов **типа ловушек** с SNMP и WMI.</span><span class="sxs-lookup"><span data-stu-id="cbb94-122">How the **TRAP-TYPE** macro maps from SNMP to WMI.</span></span>          |



 

<span data-ttu-id="cbb94-123">Поставщик SNMP поставляется с компилятором, который преобразует объекты MIB в объекты WMI.</span><span class="sxs-lookup"><span data-stu-id="cbb94-123">The SNMP provider comes with a compiler that translates MIB objects into WMI objects.</span></span> <span data-ttu-id="cbb94-124">Компилятор SNMP также может выводить сообщение об ошибке или другие сообщения.</span><span class="sxs-lookup"><span data-stu-id="cbb94-124">The SNMP compiler can also output error or other messages.</span></span> <span data-ttu-id="cbb94-125">Дополнительные сведения см. в разделе [сообщения об ошибках компилятора SNMP](snmp-compiler-error-messages.md) и [общие информационные сообщения](general-information-messages.md).</span><span class="sxs-lookup"><span data-stu-id="cbb94-125">For more information, see [SNMP compiler Error Messages](snmp-compiler-error-messages.md) and [General Information Messages](general-information-messages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbb94-126">См. также</span><span class="sxs-lookup"><span data-stu-id="cbb94-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbb94-127">Справочник по инструментарию WMI</span><span class="sxs-lookup"><span data-stu-id="cbb94-127">WMI Reference</span></span>](wmi-reference.md)
</dt> <dt>

[<span data-ttu-id="cbb94-128">Поставщики WMI</span><span class="sxs-lookup"><span data-stu-id="cbb94-128">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 



