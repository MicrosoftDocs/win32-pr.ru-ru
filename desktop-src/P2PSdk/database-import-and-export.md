---
description: При использовании одноранговых диаграмм или инфраструктур одноранговых групп сведения (записи), публикуемые одноранговыми узлами в графе или группе, хранятся в виде базы данных на каждом одноранговом компьютере.
ms.assetid: 1412b2eb-c97d-4415-998c-5f21eaadcc66
title: Импорт и экспорт базы данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b48fc09259c06e6ebaf537d26c7288d0ad09c501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998548"
---
# <a name="database-import-and-export"></a><span data-ttu-id="fe03c-103">Импорт и экспорт базы данных</span><span class="sxs-lookup"><span data-stu-id="fe03c-103">Database Import and Export</span></span>

<span data-ttu-id="fe03c-104">При использовании одноранговых диаграмм или инфраструктур одноранговых групп сведения (записи), публикуемые одноранговыми узлами в графе или группе, хранятся в виде базы данных на каждом одноранговом компьютере.</span><span class="sxs-lookup"><span data-stu-id="fe03c-104">When using the Peer Graphing or the Peer Grouping Infrastructures, the information (records) that peers publish to a graph or group is stored as a database on each peer computer.</span></span> <span data-ttu-id="fe03c-105">Чтобы перенести приложение с одного компьютера на другой, можно экспортировать одноранговую диаграмму или базу данных с одноранговой группировкой с одного компьютера, а затем импортировать ее в другую.</span><span class="sxs-lookup"><span data-stu-id="fe03c-105">To migrate an application from one computer to another computer, you can export a Peer Graphing or Peer Grouping database from one computer, and then import it to another.</span></span>

<span data-ttu-id="fe03c-106">В следующем списке приведены важные сведения о работе с базами данных.</span><span class="sxs-lookup"><span data-stu-id="fe03c-106">The following list identifies important information about working with databases:</span></span>

-   <span data-ttu-id="fe03c-107">Можно импортировать только базу данных с тем же графом и ИДЕНТИФИКАТОРом однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="fe03c-107">You can only import a database that has the same graph and peer ID.</span></span>
-   <span data-ttu-id="fe03c-108">Невозможно вызвать функции импорта и экспорта, если были вызваны [**пирграфлистен**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten), [**пирграупконнект**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)или [**пирграфконнект**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) .</span><span class="sxs-lookup"><span data-stu-id="fe03c-108">You cannot call the import and export functions if [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten), [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect), or [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) have been called.</span></span>

<span data-ttu-id="fe03c-109">**Инфраструктура одноранговых диаграмм** использует следующие вызовы для импорта и экспорта базы данных записи.</span><span class="sxs-lookup"><span data-stu-id="fe03c-109">**Peer Graphing Infrastructure** uses the following calls to import and export a record database:</span></span>

-   [<span data-ttu-id="fe03c-110">**пирграфекспортдатабасе**</span><span class="sxs-lookup"><span data-stu-id="fe03c-110">**PeerGraphExportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase)
-   [<span data-ttu-id="fe03c-111">**пирграфимпортдатабасе**</span><span class="sxs-lookup"><span data-stu-id="fe03c-111">**PeerGraphImportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase)

<span data-ttu-id="fe03c-112">**Инфраструктура одноранговых групп** использует следующие вызовы для импорта и экспорта базы данных записей.</span><span class="sxs-lookup"><span data-stu-id="fe03c-112">**Peer Grouping Infrastructure** uses the following calls to import and export a record database:</span></span>

-   [<span data-ttu-id="fe03c-113">**пирграупекспортдатабасе**</span><span class="sxs-lookup"><span data-stu-id="fe03c-113">**PeerGroupExportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)
-   [<span data-ttu-id="fe03c-114">**пирграупимпортдатабасе**</span><span class="sxs-lookup"><span data-stu-id="fe03c-114">**PeerGroupImportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase)

 

 



