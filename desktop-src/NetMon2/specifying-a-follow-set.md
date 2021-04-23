---
description: Следующий набор задает протоколы, которые следуют за протоколом. Если анализатор не может определить следующий протокол из данных в экземпляре протокола, сетевой монитор использует следующие наборы.
ms.assetid: 9e73c724-a540-42f8-b273-4f02c39d81c4
title: Указание набора следования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9e36268be82d2fed7c3d0c56a078e41dff1733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673328"
---
# <a name="specifying-a-follow-set"></a><span data-ttu-id="42b05-104">Указание набора следования</span><span class="sxs-lookup"><span data-stu-id="42b05-104">Specifying a Follow Set</span></span>

<span data-ttu-id="42b05-105">Следующий набор задает протоколы, которые следуют за протоколом.</span><span class="sxs-lookup"><span data-stu-id="42b05-105">A follow set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="42b05-106">Если анализатор не может определить следующий протокол из данных в экземпляре протокола, сетевой монитор использует следующие наборы.</span><span class="sxs-lookup"><span data-stu-id="42b05-106">Network Monitor uses a follow set when the parser cannot identify the next protocol from the data in a protocol instance.</span></span>

<span data-ttu-id="42b05-107">Например, средство синтаксического анализа NetBIOS задает следующий набор, поскольку данные в протоколе NetBIOS не определяют, какой протокол является следующим.</span><span class="sxs-lookup"><span data-stu-id="42b05-107">For example, the NetBIOS parser specifies a follow set because the data in the NetBIOS protocol does not identify which protocol is next.</span></span> <span data-ttu-id="42b05-108">В результате средство синтаксического анализа NetBIOS должно создать следующий набор всех протоколов, которые могут следовать за.</span><span class="sxs-lookup"><span data-stu-id="42b05-108">As a result the NetBIOS parser must create a follow set of all the protocols that may follow.</span></span>

<span data-ttu-id="42b05-109">В следующем примере кода определяется набор NetBIOS в файле [*Parser.ini*](p.md) .</span><span class="sxs-lookup"><span data-stu-id="42b05-109">The following code example identifies the NetBIOS follow set in the [*Parser.ini*](p.md) file.</span></span> <span data-ttu-id="42b05-110">В наборе ниже содержатся протоколы SMB и Microsoft Remote Procedure Call (MSRPC).</span><span class="sxs-lookup"><span data-stu-id="42b05-110">The follow set contains server message block (SMB), and Microsoft remote procedure call (MSRPC) protocols.</span></span> <span data-ttu-id="42b05-111">Это единственные протоколы, которые могут следовать за экземпляром протокола NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="42b05-111">These are the only protocols that can follow an instance of the NetBIOS protocol.</span></span>

``` syntax
[NETBIOS]
   Comment    = "Network Basic Input/Output System protocol"
   FollowSet  = SMB, MSRPC
   HelpFile   =
```

<span data-ttu-id="42b05-112">Синтаксический анализатор задает следующий набор во время реализации функции [**парсераутоинсталлинфо**](parserautoinstallinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="42b05-112">A parser specifies a follow set during the implementation of the [**ParserAutoInstallInfo**](parserautoinstallinfo.md) function.</span></span> <span data-ttu-id="42b05-113">Средство синтаксического анализа может указывать, какие протоколы предшествуют и какие протоколы следуют.</span><span class="sxs-lookup"><span data-stu-id="42b05-113">A parser can specify which protocols precede, and which protocols follow.</span></span> <span data-ttu-id="42b05-114">Если средство синтаксического анализа задает протоколы, предшествующие, сетевой монитор добавляет протокол синтаксического анализатора к следующим наборам заданных протоколов.</span><span class="sxs-lookup"><span data-stu-id="42b05-114">When a parser specifies the protocols that precede, Network Monitor adds the parser protocol to the follow sets of the specified protocols.</span></span> <span data-ttu-id="42b05-115">Когда средство синтаксического анализа указывает следующие протоколы, сетевой монитор создает новый раздел в Parser.ini файле, который включает в себя следующий набор средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="42b05-115">When a parser specifies the protocols that follow, Network Monitor creates a new section in the Parser.ini file that includes the follow set of the parser.</span></span>

 

 



