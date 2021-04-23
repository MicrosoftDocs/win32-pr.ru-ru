---
description: 'API группирования использует следующие функции:'
ms.assetid: 56ea2880-b468-4816-b6c9-5780c807b3f1
title: Группирование функций API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d2970ca68d69b16a32cf7a6d546a5852b07dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663338"
---
# <a name="grouping-api-functions"></a><span data-ttu-id="091a2-103">Группирование функций API</span><span class="sxs-lookup"><span data-stu-id="091a2-103">Grouping API Functions</span></span>

<span data-ttu-id="091a2-104">API группирования использует следующие функции:</span><span class="sxs-lookup"><span data-stu-id="091a2-104">The Grouping API uses the following functions:</span></span>

## <a name="group-initialization-and-cleanup-functions"></a><span data-ttu-id="091a2-105">Функции инициализации и очистки группы</span><span class="sxs-lookup"><span data-stu-id="091a2-105">Group Initialization and Cleanup Functions</span></span>



| <span data-ttu-id="091a2-106">Функция</span><span class="sxs-lookup"><span data-stu-id="091a2-106">Function</span></span>                                       | <span data-ttu-id="091a2-107">Описание</span><span class="sxs-lookup"><span data-stu-id="091a2-107">Description</span></span>                                                                                                            |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="091a2-108">**пирграупшутдовн**</span><span class="sxs-lookup"><span data-stu-id="091a2-108">**PeerGroupShutdown**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown) | <span data-ttu-id="091a2-109">Закрывает одноранговую группу, созданную с помощью [**пирграупстартуп**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) , и уничтожает выделенные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="091a2-109">Closes a peer group created with [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) and disposes of any allocated resources.</span></span> |
| [<span data-ttu-id="091a2-110">**пирграупстартуп**</span><span class="sxs-lookup"><span data-stu-id="091a2-110">**PeerGroupStartup**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupstartup)   | <span data-ttu-id="091a2-111">Инициирует одноранговую группу с помощью запрошенной версии инфраструктуры одноранговой сети.</span><span class="sxs-lookup"><span data-stu-id="091a2-111">Initiates a peer group by using a requested version of the Peer infrastructure.</span></span>                                        |



 

## <a name="group-creation-and-access-functions"></a><span data-ttu-id="091a2-112">Функции создания групп и доступа к ним</span><span class="sxs-lookup"><span data-stu-id="091a2-112">Group Creation and Access Functions</span></span>



| <span data-ttu-id="091a2-113">Функция</span><span class="sxs-lookup"><span data-stu-id="091a2-113">Function</span></span>                                                                       | <span data-ttu-id="091a2-114">Описание</span><span class="sxs-lookup"><span data-stu-id="091a2-114">Description</span></span>                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="091a2-115">**пирграупклосе**</span><span class="sxs-lookup"><span data-stu-id="091a2-115">**PeerGroupClose**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupclose)                                       | <span data-ttu-id="091a2-116">Делает недействительным маркер одноранговой группы, полученный предыдущим вызовом функции [**пирграупкреате**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**пирграупжоин**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)или [**пирграупопен**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) .</span><span class="sxs-lookup"><span data-stu-id="091a2-116">Invalidates the peer group handle obtained by a previous call to the [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), or [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) function.</span></span> |
| [<span data-ttu-id="091a2-117">**пирграупконнект**</span><span class="sxs-lookup"><span data-stu-id="091a2-117">**PeerGroupConnect**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)                                   | <span data-ttu-id="091a2-118">Инициирует поиск по протоколу PNRP для одноранговой группы и пытается подключиться к ней.</span><span class="sxs-lookup"><span data-stu-id="091a2-118">Initiates a PNRP search for a peer group and attempts to connect to it.</span></span> <span data-ttu-id="091a2-119">После успешного вызова этой функции одноранговый узел может взаимодействовать с другими членами одноранговой группы.</span><span class="sxs-lookup"><span data-stu-id="091a2-119">After this function is called successfully, a peer can communicate with other members of the peer group.</span></span>                             |
| [<span data-ttu-id="091a2-120">**пирграупконнектбяддресс**</span><span class="sxs-lookup"><span data-stu-id="091a2-120">**PeerGroupConnectByAddress**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupconnectbyaddress)                 | <span data-ttu-id="091a2-121">Пытается подключиться к одноранговой группе, в которой участвуют другие узлы с известными IPv6-адресами.</span><span class="sxs-lookup"><span data-stu-id="091a2-121">Attempts to connect to the peer group that other peers with known IPv6 addresses are participating in.</span></span>                                                                                                       |
| [<span data-ttu-id="091a2-122">**пирграупкреате**</span><span class="sxs-lookup"><span data-stu-id="091a2-122">**PeerGroupCreate**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)                                     | <span data-ttu-id="091a2-123">Создает новую одноранговую группу.</span><span class="sxs-lookup"><span data-stu-id="091a2-123">Creates a new peer group.</span></span>                                                                                                                                                                                    |
| [<span data-ttu-id="091a2-124">**пирграупкреатеинвитатион**</span><span class="sxs-lookup"><span data-stu-id="091a2-124">**PeerGroupCreateInvitation**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation)                 | <span data-ttu-id="091a2-125">Возвращает XML-строку, которая может использоваться указанным одноранговым узлом для присоединения к группе.</span><span class="sxs-lookup"><span data-stu-id="091a2-125">Returns an XML string that can be used by the specified peer to join a group.</span></span>                                                                                                                                |
| [<span data-ttu-id="091a2-126">**пирграупкреатепассвординвитатион**</span><span class="sxs-lookup"><span data-stu-id="091a2-126">**PeerGroupCreatePasswordInvitation**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupcreatepasswordinvitation) | <span data-ttu-id="091a2-127">Возвращает XML-строку, которая может использоваться указанным одноранговым узлом для присоединения группы с совпадающим паролем.</span><span class="sxs-lookup"><span data-stu-id="091a2-127">Returns an XML string that can be used by the specified peer to join a group with a matching password.</span></span>                                                                                                       |
| [<span data-ttu-id="091a2-128">**пирграупделете**</span><span class="sxs-lookup"><span data-stu-id="091a2-128">**PeerGroupDelete**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupdelete)                                     | <span data-ttu-id="091a2-129">Удаляет локальные данные и сертификат, связанные с одноранговой группой.</span><span class="sxs-lookup"><span data-stu-id="091a2-129">Deletes the local data and certificate associated with a peer group.</span></span>                                                                                                                                         |
| [<span data-ttu-id="091a2-130">**пирграупжетстатус**</span><span class="sxs-lookup"><span data-stu-id="091a2-130">**PeerGroupGetStatus**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus)                               | <span data-ttu-id="091a2-131">Извлекает текущее состояние группы.</span><span class="sxs-lookup"><span data-stu-id="091a2-131">Retrieves the current status of a group.</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="091a2-132">**пирграуписсуекредентиалс**</span><span class="sxs-lookup"><span data-stu-id="091a2-132">**PeerGroupIssueCredentials**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)                 | <span data-ttu-id="091a2-133">Выдает учетные данные, включая ГМК, для определенного удостоверения и при необходимости возвращает строку XML приглашения, которую приглашенный кэширующий узел может использовать для присоединения одноранговой группы.</span><span class="sxs-lookup"><span data-stu-id="091a2-133">Issues credentials, including a GMC, to a specific identity, and optionally returns an invitation XML string the invited peer can use to join a peer group.</span></span>                                                  |
| [<span data-ttu-id="091a2-134">**пирграупжоин**</span><span class="sxs-lookup"><span data-stu-id="091a2-134">**PeerGroupJoin**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)                                         | <span data-ttu-id="091a2-135">Разрешает однорангового узла с приглашением присоединиться к существующей одноранговой группе.</span><span class="sxs-lookup"><span data-stu-id="091a2-135">Allows a peer with an invitation to join an existing peer group.</span></span>                                                                                                                                             |
| [<span data-ttu-id="091a2-136">**пирграупопен**</span><span class="sxs-lookup"><span data-stu-id="091a2-136">**PeerGroupOpen**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupopen)                                         | <span data-ttu-id="091a2-137">Открывает одноранговую группу, которая была создана или соединена одноранговым узлом.</span><span class="sxs-lookup"><span data-stu-id="091a2-137">Opens a peer group that a peer has created or joined.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="091a2-138">**пирграуппарсеинвитатион**</span><span class="sxs-lookup"><span data-stu-id="091a2-138">**PeerGroupParseInvitation**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation)                   | <span data-ttu-id="091a2-139">Возвращает структуру [**\_ \_ сведений о приглашении однорангового узла**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) с подробными сведениями о конкретном приглашении.</span><span class="sxs-lookup"><span data-stu-id="091a2-139">Returns a [**PEER\_INVITATION\_INFO**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) structure with the details of a specific invitation.</span></span>                                                                                        |
| [<span data-ttu-id="091a2-140">**пирграуппассворджоин**</span><span class="sxs-lookup"><span data-stu-id="091a2-140">**PeerGroupPasswordJoin**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergrouppasswordjoin)                         | <span data-ttu-id="091a2-141">Разрешает одноранговому узлу с приглашением и правильным паролем присоединение к одноранговой группе, защищенной паролем.</span><span class="sxs-lookup"><span data-stu-id="091a2-141">Allows a peer with an invitation and the correct password to join a password-protected peer group.</span></span>                                                                                                           |



 

## <a name="group-and-member-information-functions"></a><span data-ttu-id="091a2-142">Функции для работы со сведениями о группах и членах</span><span class="sxs-lookup"><span data-stu-id="091a2-142">Group and Member Information Functions</span></span>



| <span data-ttu-id="091a2-143">Функция</span><span class="sxs-lookup"><span data-stu-id="091a2-143">Function</span></span>                                                 | <span data-ttu-id="091a2-144">Описание</span><span class="sxs-lookup"><span data-stu-id="091a2-144">Description</span></span>                                                                                                                        |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="091a2-145">**пирграупенуммемберс**</span><span class="sxs-lookup"><span data-stu-id="091a2-145">**PeerGroupEnumMembers**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers)     | <span data-ttu-id="091a2-146">Создает перечисление доступных членов одноранговой группы и связанные сведения о членстве.</span><span class="sxs-lookup"><span data-stu-id="091a2-146">Creates an enumeration of available peer group members and the associated membership information.</span></span>                                  |
| [<span data-ttu-id="091a2-147">**пирграупжетпропертиес**</span><span class="sxs-lookup"><span data-stu-id="091a2-147">**PeerGroupGetProperties**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgetproperties) | <span data-ttu-id="091a2-148">Получает сведения о свойствах указанной группы.</span><span class="sxs-lookup"><span data-stu-id="091a2-148">Retrieves information on the properties of a specified group.</span></span>                                                                      |
| [<span data-ttu-id="091a2-149">**пирграупсетпропертиес**</span><span class="sxs-lookup"><span data-stu-id="091a2-149">**PeerGroupSetProperties**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupsetproperties) | <span data-ttu-id="091a2-150">Задает свойства текущей одноранговой группы.</span><span class="sxs-lookup"><span data-stu-id="091a2-150">Sets the current peer group properties.</span></span> <span data-ttu-id="091a2-151">В версии 1,0 этого API только создатель одноранговой группы может выполнить эту операцию.</span><span class="sxs-lookup"><span data-stu-id="091a2-151">In version 1.0 of this API, only the creator of the peer group can perform this operation.</span></span> |



 

## <a name="records-and-record-management-functions"></a><span data-ttu-id="091a2-152">Функции управления записями и записями</span><span class="sxs-lookup"><span data-stu-id="091a2-152">Records and Record Management Functions</span></span>



| <span data-ttu-id="091a2-153">Функция</span><span class="sxs-lookup"><span data-stu-id="091a2-153">Function</span></span>                                                 | <span data-ttu-id="091a2-154">Описание</span><span class="sxs-lookup"><span data-stu-id="091a2-154">Description</span></span>                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="091a2-155">**пирграупаддрекорд**</span><span class="sxs-lookup"><span data-stu-id="091a2-155">**PeerGroupAddRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)         | <span data-ttu-id="091a2-156">Добавляет новую запись в одноранговую группу, которая распространяется на все участвующие одноранговые узлы.</span><span class="sxs-lookup"><span data-stu-id="091a2-156">Adds a new record to the peer group, which is propagated to all participating peers.</span></span> |
| [<span data-ttu-id="091a2-157">**пирграупделетерекорд**</span><span class="sxs-lookup"><span data-stu-id="091a2-157">**PeerGroupDeleteRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord)   | <span data-ttu-id="091a2-158">Удаляет запись из одноранговой группы.</span><span class="sxs-lookup"><span data-stu-id="091a2-158">Deletes a record from a peer group.</span></span> <span data-ttu-id="091a2-159">Только создатель записи может удалить ее.</span><span class="sxs-lookup"><span data-stu-id="091a2-159">Only the creator of a record can delete it.</span></span>      |
| [<span data-ttu-id="091a2-160">**пирграупенумрекордс**</span><span class="sxs-lookup"><span data-stu-id="091a2-160">**PeerGroupEnumRecords**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords)     | <span data-ttu-id="091a2-161">Создает перечисление записей одноранговых групп.</span><span class="sxs-lookup"><span data-stu-id="091a2-161">Creates an enumeration of peer group records.</span></span>                                        |
| [<span data-ttu-id="091a2-162">**пирграупжетрекорд**</span><span class="sxs-lookup"><span data-stu-id="091a2-162">**PeerGroupGetRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord)         | <span data-ttu-id="091a2-163">Извлекает определенную запись группы.</span><span class="sxs-lookup"><span data-stu-id="091a2-163">Retrieves a specific group record.</span></span>                                                   |
| [<span data-ttu-id="091a2-164">**пирграупсеарчрекордс**</span><span class="sxs-lookup"><span data-stu-id="091a2-164">**PeerGroupSearchRecords**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) | <span data-ttu-id="091a2-165">Выполняет поиск записей, соответствующих указанным критериям, в локальной базе данных одноранговых групп.</span><span class="sxs-lookup"><span data-stu-id="091a2-165">Searches the local peer group database for records that match the supplied criteria.</span></span> |
| [<span data-ttu-id="091a2-166">**пирграупупдатерекорд**</span><span class="sxs-lookup"><span data-stu-id="091a2-166">**PeerGroupUpdateRecord**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord)   | <span data-ttu-id="091a2-167">Обновляет запись в определенной одноранговой группе.</span><span class="sxs-lookup"><span data-stu-id="091a2-167">Updates a record within a specific peer group.</span></span>                                       |



 

## <a name="group-database-importexport-functions"></a><span data-ttu-id="091a2-168">Функции импорта и экспорта базы данных Group</span><span class="sxs-lookup"><span data-stu-id="091a2-168">Group Database Import/Export Functions</span></span>



| <span data-ttu-id="091a2-169">Функция</span><span class="sxs-lookup"><span data-stu-id="091a2-169">Function</span></span>                                                   | <span data-ttu-id="091a2-170">Описание</span><span class="sxs-lookup"><span data-stu-id="091a2-170">Description</span></span>                                                                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="091a2-171">**пирграупекспортдатабасе**</span><span class="sxs-lookup"><span data-stu-id="091a2-171">**PeerGroupExportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase) | <span data-ttu-id="091a2-172">Экспортирует базу данных одноранговой группы в конкретный файл, который можно перенести на другой компьютер и импортировать с помощью функции [**пирграупимпортдатабасе**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) .</span><span class="sxs-lookup"><span data-stu-id="091a2-172">Exports a peer group database to a specific file, which can be transported to another computer and imported with the [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) function.</span></span> |
| [<span data-ttu-id="091a2-173">**пирграупимпортдатабасе**</span><span class="sxs-lookup"><span data-stu-id="091a2-173">**PeerGroupImportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) | <span data-ttu-id="091a2-174">Импортирует базу данных одноранговой группы из локального файла.</span><span class="sxs-lookup"><span data-stu-id="091a2-174">Imports a peer group database from a local file.</span></span>                                                                                                                                          |



 

## <a name="direct-connection-functions"></a><span data-ttu-id="091a2-175">Функции прямого подключения</span><span class="sxs-lookup"><span data-stu-id="091a2-175">Direct Connection Functions</span></span>



| <span data-ttu-id="091a2-176">Функция</span><span class="sxs-lookup"><span data-stu-id="091a2-176">Function</span></span>                                                                 | <span data-ttu-id="091a2-177">Описание</span><span class="sxs-lookup"><span data-stu-id="091a2-177">Description</span></span>                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="091a2-178">**пирграупклоседиректконнектион**</span><span class="sxs-lookup"><span data-stu-id="091a2-178">**PeerGroupCloseDirectConnection**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) | <span data-ttu-id="091a2-179">Закрывает определенное прямое соединение между двумя одноранговыми узлами.</span><span class="sxs-lookup"><span data-stu-id="091a2-179">Closes a specific direct connection between two peers.</span></span>              |
| [<span data-ttu-id="091a2-180">**пирграупенумконнектионс**</span><span class="sxs-lookup"><span data-stu-id="091a2-180">**PeerGroupEnumConnections**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections)             | <span data-ttu-id="091a2-181">Создает перечисление активных в данный момент подключений на одноранговом узле.</span><span class="sxs-lookup"><span data-stu-id="091a2-181">Creates an enumeration of connections currently active on the peer.</span></span> |
| [<span data-ttu-id="091a2-182">**пирграупопендиректконнектион**</span><span class="sxs-lookup"><span data-stu-id="091a2-182">**PeerGroupOpenDirectConnection**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)   | <span data-ttu-id="091a2-183">Устанавливает прямое соединение с другим одноранговым узлом в одноранговой группе.</span><span class="sxs-lookup"><span data-stu-id="091a2-183">Establishes a direct connection with another peer in a peer group.</span></span>  |
| [<span data-ttu-id="091a2-184">**пирграупсенддата**</span><span class="sxs-lookup"><span data-stu-id="091a2-184">**PeerGroupSendData**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata)                           | <span data-ttu-id="091a2-185">Отправляет данные участнику через соседа или прямое соединение.</span><span class="sxs-lookup"><span data-stu-id="091a2-185">Sends data to a member over a neighbor or direct connection.</span></span>        |



 

## <a name="group-events-infrastructure"></a><span data-ttu-id="091a2-186">Инфраструктура событий группы</span><span class="sxs-lookup"><span data-stu-id="091a2-186">Group Events Infrastructure</span></span>



| <span data-ttu-id="091a2-187">Функция</span><span class="sxs-lookup"><span data-stu-id="091a2-187">Function</span></span>                                                     | <span data-ttu-id="091a2-188">Описание</span><span class="sxs-lookup"><span data-stu-id="091a2-188">Description</span></span>                                                                                    |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="091a2-189">**пирграупжетевентдата**</span><span class="sxs-lookup"><span data-stu-id="091a2-189">**PeerGroupGetEventData**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)       | <span data-ttu-id="091a2-190">Позволяет приложению извлекать данные, возвращенные событием группирования.</span><span class="sxs-lookup"><span data-stu-id="091a2-190">Allows an application to retrieve the data returned by a grouping event.</span></span>                       |
| [<span data-ttu-id="091a2-191">**пирграупрегистеревент**</span><span class="sxs-lookup"><span data-stu-id="091a2-191">**PeerGroupRegisterEvent**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)     | <span data-ttu-id="091a2-192">Регистрирует одноранговый узел для конкретных событий одноранговой группы.</span><span class="sxs-lookup"><span data-stu-id="091a2-192">Registers a peer for specific peer group events.</span></span>                                               |
| [<span data-ttu-id="091a2-193">**пирграупунрегистеревент**</span><span class="sxs-lookup"><span data-stu-id="091a2-193">**PeerGroupUnregisterEvent**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) | <span data-ttu-id="091a2-194">Отменяет регистрацию однорангового узла на основе уведомления о событиях однорангового узла, связанных с переданным обработчиком событий.</span><span class="sxs-lookup"><span data-stu-id="091a2-194">Unregisters a peer from notification of peer events associated with the supplied event handle.</span></span> |



 

## <a name="group-time-conversion-functions"></a><span data-ttu-id="091a2-195">Функции преобразования времени группирования</span><span class="sxs-lookup"><span data-stu-id="091a2-195">Group Time Conversion Functions</span></span>



| <span data-ttu-id="091a2-196">Функция</span><span class="sxs-lookup"><span data-stu-id="091a2-196">Function</span></span>                                                                     | <span data-ttu-id="091a2-197">Описание</span><span class="sxs-lookup"><span data-stu-id="091a2-197">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="091a2-198">**пирграуппиртиметауниверсалтиме**</span><span class="sxs-lookup"><span data-stu-id="091a2-198">**PeerGroupPeerTimeToUniversalTime**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergrouppeertimetouniversaltime) | <span data-ttu-id="091a2-199">Преобразует значение времени ссылки, поддерживаемое одноранговой группой, в локализованное значение времени, подходящее для вывода на одноранговый компьютер.</span><span class="sxs-lookup"><span data-stu-id="091a2-199">Converts the peer group-maintained reference time value to a localized time value appropriate for display on a peer computer.</span></span> |
| [<span data-ttu-id="091a2-200">**пирграупуниверсалтиметопиртиме**</span><span class="sxs-lookup"><span data-stu-id="091a2-200">**PeerGroupUniversalTimeToPeerTime**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupuniversaltimetopeertime) | <span data-ttu-id="091a2-201">Преобразует значение местного времени из однорангового компьютера в общее значение времени одноранговой группы.</span><span class="sxs-lookup"><span data-stu-id="091a2-201">Converts a local time value from a peer's computer to a common peer group time value.</span></span>                                         |



 

## <a name="group-configuration-functions"></a><span data-ttu-id="091a2-202">Функции конфигурации группы</span><span class="sxs-lookup"><span data-stu-id="091a2-202">Group Configuration Functions</span></span>



| <span data-ttu-id="091a2-203">Функция</span><span class="sxs-lookup"><span data-stu-id="091a2-203">Function</span></span>                                               | <span data-ttu-id="091a2-204">Описание</span><span class="sxs-lookup"><span data-stu-id="091a2-204">Description</span></span>                                                                                                                       |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="091a2-205">**пирграупекспортконфиг**</span><span class="sxs-lookup"><span data-stu-id="091a2-205">**PeerGroupExportConfig**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig) | <span data-ttu-id="091a2-206">Экспортирует конфигурацию группы для однорангового узла в виде XML-строки, содержащей удостоверение, имя группы и ГМК для удостоверения.</span><span class="sxs-lookup"><span data-stu-id="091a2-206">Exports the group configuration for a peer as an XML string that contains the identity, group name, and the GMC for the identity.</span></span> |
| [<span data-ttu-id="091a2-207">**пирграупимпортконфиг**</span><span class="sxs-lookup"><span data-stu-id="091a2-207">**PeerGroupImportConfig**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) | <span data-ttu-id="091a2-208">Импортирует конфигурацию одноранговой группы для удостоверения на основе конкретных параметров в указанной XML-строке конфигурации.</span><span class="sxs-lookup"><span data-stu-id="091a2-208">Imports a peer group configuration for an identity based on the specific settings in a supplied XML configuration string.</span></span>         |



 

 

 



