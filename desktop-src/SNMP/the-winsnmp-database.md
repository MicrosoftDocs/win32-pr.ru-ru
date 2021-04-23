---
title: База данных WinSNMP
description: В реализации Microsoft WinSNMP хранится административная информация в базе данных.
ms.assetid: 0a0d9731-d800-4eaa-8230-25469a0b0285
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea83573cad12c05f6dd4b7e2375df5941e05fadb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486709"
---
# <a name="the-winsnmp-database"></a><span data-ttu-id="88e27-103">База данных WinSNMP</span><span class="sxs-lookup"><span data-stu-id="88e27-103">The WinSNMP Database</span></span>

<span data-ttu-id="88e27-104">В реализации Microsoft WinSNMP хранится административная информация в базе данных.</span><span class="sxs-lookup"><span data-stu-id="88e27-104">The Microsoft WinSNMP implementation maintains a store of administrative information in a database.</span></span> <span data-ttu-id="88e27-105">База данных содержит следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="88e27-105">The database includes the following information:</span></span>

-   <span data-ttu-id="88e27-106">Свойства сети и версии.</span><span class="sxs-lookup"><span data-stu-id="88e27-106">Network and version properties.</span></span>

    <span data-ttu-id="88e27-107">Реализация использует эти свойства для определения сетевого транспортного протокола и платформы SNMP-версий, используемых для завершения запросов на передачу.</span><span class="sxs-lookup"><span data-stu-id="88e27-107">The implementation uses these properties to determine which network transport protocol and SNMP version framework to use to complete transmission requests.</span></span> <span data-ttu-id="88e27-108">Дополнительные сведения см. в разделе [About SNMP Versions](about-snmp-versions.md).</span><span class="sxs-lookup"><span data-stu-id="88e27-108">For more information, see [About SNMP Versions](about-snmp-versions.md).</span></span>

-   <span data-ttu-id="88e27-109">Режим преобразования сущностей и контекста.</span><span class="sxs-lookup"><span data-stu-id="88e27-109">Entity and context translation mode.</span></span>

    <span data-ttu-id="88e27-110">В реализации этот режим используется для интерпретации понятных пользователю имен для объектов SNMP и контекстов.</span><span class="sxs-lookup"><span data-stu-id="88e27-110">The implementation uses this mode to interpret user-friendly names for SNMP entities and contexts.</span></span> <span data-ttu-id="88e27-111">Дополнительные сведения см. [в разделе Установка режима преобразования сущностей и контекста](setting-the-entity-and-context-translation-mode.md).</span><span class="sxs-lookup"><span data-stu-id="88e27-111">For more information, see [Setting the Entity and Context Translation Mode](setting-the-entity-and-context-translation-mode.md).</span></span>

-   <span data-ttu-id="88e27-112">Параметр политики повторной передачи.</span><span class="sxs-lookup"><span data-stu-id="88e27-112">Retransmission policy setting.</span></span>

    <span data-ttu-id="88e27-113">Реализация использует этот параметр, чтобы определить, следует ли выполнять политику повторной передачи приложения.</span><span class="sxs-lookup"><span data-stu-id="88e27-113">The implementation uses this setting to determine whether or not it should execute the application's retransmission policy.</span></span> <span data-ttu-id="88e27-114">Реализация хранит значение времени ожидания и число повторных попыток для каждой целевой сущности.</span><span class="sxs-lookup"><span data-stu-id="88e27-114">The implementation stores a time-out value and a retry count for each destination entity.</span></span> <span data-ttu-id="88e27-115">Дополнительные сведения см. в статье о повторной [передаче](about-retransmission.md) и [управлении политикой](managing-the-retransmission-policy.md)повторной передачи.</span><span class="sxs-lookup"><span data-stu-id="88e27-115">For more information, see [About Retransmission](about-retransmission.md) and [Managing the Retransmission Policy](managing-the-retransmission-policy.md).</span></span>

 

 




