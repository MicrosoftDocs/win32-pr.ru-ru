---
description: Этот раздел не является актуальным. Самые актуальные сведения см. в спецификации печати схемы.
ms.assetid: 00f1d2c4-3c71-4b64-b689-83b4399aa61d
title: Сведения о конфигурации, не связанные с PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26bbc1b37d430158d6e8c020aa5994fe4e28f4af
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105674564"
---
# <a name="configuration-information-not-related-to-printcapabilities"></a><span data-ttu-id="6212e-104">Сведения о конфигурации, не связанные с PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="6212e-104">Configuration Information Not Related to PrintCapabilities</span></span>

<span data-ttu-id="6212e-105">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="6212e-105">This topic is not current.</span></span> <span data-ttu-id="6212e-106">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6212e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6212e-107">Помимо предоставления выбора для атрибутов устройств, определенных в PrintCapabilities, PrintTicket позволяет добавлять дополнительные сведения клиентами в форме элементов свойств.</span><span class="sxs-lookup"><span data-stu-id="6212e-107">In addition to providing selections for the device attributes defined in the PrintCapabilities, the PrintTicket allows additional information to be added by clients in the form of Property elements.</span></span> <span data-ttu-id="6212e-108">Схема печати определяет ряд стандартных экземпляров свойств, и поставщик интерфейса может также освобождать экземпляры закрытых свойств.</span><span class="sxs-lookup"><span data-stu-id="6212e-108">The Print Schema defines a number of standard Property instances, and the interface provider is free to introduce private Property instances as well.</span></span> <span data-ttu-id="6212e-109">Например, если члены Организации отправляют большую часть своих заданий печати в центральное средство пакетной обработки, они могут указать для каждого задания экземпляр закрытого свойства, который содержит обратный адрес.</span><span class="sxs-lookup"><span data-stu-id="6212e-109">For example, if members of an organization send most of their print jobs to a central batch facility, they can specify for each job a private Property instance that contains a return address.</span></span> <span data-ttu-id="6212e-110">Это свойство может упростить доставку завершенного задания в инициатор.</span><span class="sxs-lookup"><span data-stu-id="6212e-110">This Property can make it easier to deliver the completed job can be delivered to the originator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6212e-111">См. также</span><span class="sxs-lookup"><span data-stu-id="6212e-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6212e-112">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="6212e-112">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



