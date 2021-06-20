---
description: Помимо PrintCapabilities, PrintTicket позволяет добавлять дополнительные сведения клиентами в форме элементов свойств.
ms.assetid: 00f1d2c4-3c71-4b64-b689-83b4399aa61d
title: Сведения о конфигурации, не связанные с PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e4ac332d6e9b106ab9d68c29d03366761c01d5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409657"
---
# <a name="configuration-information-not-related-to-printcapabilities"></a><span data-ttu-id="d407e-103">Сведения о конфигурации, не связанные с PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="d407e-103">Configuration Information Not Related to PrintCapabilities</span></span>

<span data-ttu-id="d407e-104">Этот раздел не является актуальным.</span><span class="sxs-lookup"><span data-stu-id="d407e-104">This topic is not current.</span></span> <span data-ttu-id="d407e-105">Самые актуальные сведения см. в [спецификации печати схемы](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d407e-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d407e-106">Помимо предоставления выбора для атрибутов устройств, определенных в PrintCapabilities, PrintTicket позволяет добавлять дополнительные сведения клиентами в форме элементов свойств.</span><span class="sxs-lookup"><span data-stu-id="d407e-106">In addition to providing selections for the device attributes defined in the PrintCapabilities, the PrintTicket allows additional information to be added by clients in the form of Property elements.</span></span> <span data-ttu-id="d407e-107">Схема печати определяет ряд стандартных экземпляров свойств, и поставщик интерфейса может также освобождать экземпляры закрытых свойств.</span><span class="sxs-lookup"><span data-stu-id="d407e-107">The Print Schema defines a number of standard Property instances, and the interface provider is free to introduce private Property instances as well.</span></span> <span data-ttu-id="d407e-108">Например, если члены Организации отправляют большую часть своих заданий печати в центральное средство пакетной обработки, они могут указать для каждого задания экземпляр закрытого свойства, который содержит обратный адрес.</span><span class="sxs-lookup"><span data-stu-id="d407e-108">For example, if members of an organization send most of their print jobs to a central batch facility, they can specify for each job a private Property instance that contains a return address.</span></span> <span data-ttu-id="d407e-109">Это свойство может упростить доставку завершенного задания в инициатор.</span><span class="sxs-lookup"><span data-stu-id="d407e-109">This Property can make it easier to deliver the completed job can be delivered to the originator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d407e-110">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d407e-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d407e-111">Печать спецификации схемы</span><span class="sxs-lookup"><span data-stu-id="d407e-111">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



