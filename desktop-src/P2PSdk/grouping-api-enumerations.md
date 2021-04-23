---
description: 'API группирования использует следующие перечисления:'
ms.assetid: 7f7e926c-e8dc-48c0-b5b9-0dc98686a174
title: Группирование перечислений API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ce48a9f4b3b3894be90b809bc29d83496642d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663339"
---
# <a name="grouping-api-enumerations"></a><span data-ttu-id="e0672-103">Группирование перечислений API</span><span class="sxs-lookup"><span data-stu-id="e0672-103">Grouping API Enumerations</span></span>

<span data-ttu-id="e0672-104">API группирования использует следующие перечисления:</span><span class="sxs-lookup"><span data-stu-id="e0672-104">The Grouping API uses the following enumerations:</span></span>



| <span data-ttu-id="e0672-105">Перечисление</span><span class="sxs-lookup"><span data-stu-id="e0672-105">Enumeration</span></span>                                                                        | <span data-ttu-id="e0672-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e0672-106">Description</span></span>                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0672-107">**\_ \_ Схема проверки подлинности одноранговых групп \_**</span><span class="sxs-lookup"><span data-stu-id="e0672-107">**PEER\_GROUP\_AUTHENTICATION\_SCHEME**</span></span>](/windows/desktop/api/P2P/ne-p2p-peer_group_authentication_scheme)    | <span data-ttu-id="e0672-108">Определяет набор возможных схем проверки подлинности, которые можно использовать для проверки подлинности узлов, присоединяющихся к одноранговой группе.</span><span class="sxs-lookup"><span data-stu-id="e0672-108">Defines the set of possible authentication schemes that can be used to authenticate peers joining a peer group.</span></span>                                                                                                                                           |
| [<span data-ttu-id="e0672-109">**\_ \_ Тип события одноранговой группы \_**</span><span class="sxs-lookup"><span data-stu-id="e0672-109">**PEER\_GROUP\_EVENT\_TYPE**</span></span>](/windows/desktop/api/P2P/ne-p2p-peer_group_event_type)                          | <span data-ttu-id="e0672-110">Содержит конкретные типы событий одноранговых узлов, которые могут встречаться в одноранговой группе.</span><span class="sxs-lookup"><span data-stu-id="e0672-110">Contains the specific peer event types that can occur within a peer group.</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="e0672-111">**\_ \_ \_ Флаги учетных данных для вопроса одноранговой группы \_**</span><span class="sxs-lookup"><span data-stu-id="e0672-111">**PEER\_GROUP\_ISSUE\_CREDENTIAL\_FLAGS**</span></span>](/windows/win32/api/p2p/ne-p2p-peer_group_issue_credential_flags) | <span data-ttu-id="e0672-112">Указывает, хранятся ли учетные данные пользователя в группе.</span><span class="sxs-lookup"><span data-stu-id="e0672-112">Specifies if user credentials are stored within a group.</span></span>                                                                                                                                                                                                  |
| [<span data-ttu-id="e0672-113">**\_ \_ флаги свойств одноранговой группы \_**</span><span class="sxs-lookup"><span data-stu-id="e0672-113">**PEER\_GROUP\_PROPERTY\_FLAGS**</span></span>](/windows/desktop/api/P2P/ne-p2p-peer_group_property_flags)                  | <span data-ttu-id="e0672-114">Задает параметры членства в одноранговой группе.</span><span class="sxs-lookup"><span data-stu-id="e0672-114">Specifies peer group membership settings.</span></span>                                                                                                                                                                                                                 |
| [<span data-ttu-id="e0672-115">**состояние одноранговой \_ группы \_**</span><span class="sxs-lookup"><span data-stu-id="e0672-115">**PEER\_GROUP\_STATUS**</span></span>](/windows/desktop/api/P2P/ne-p2p-peer_group_status)                                   | <span data-ttu-id="e0672-116">Указывает, есть ли у одноранговой группы соединения.</span><span class="sxs-lookup"><span data-stu-id="e0672-116">Indicates whether or not the peer group has connections present.</span></span>                                                                                                                                                                                          |
| [<span data-ttu-id="e0672-117">**\_ \_ тип изменения однорангового элемента \_**</span><span class="sxs-lookup"><span data-stu-id="e0672-117">**PEER\_MEMBER\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/P2P/ne-p2p-peer_member_change_type)                      | <span data-ttu-id="e0672-118">Определяет набор возможных членств одноранговой группы и состояний присутствия для однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="e0672-118">Defines the set of possible peer group membership and presence states for a peer.</span></span>                                                                                                                                                                         |
| [<span data-ttu-id="e0672-119">**Флаги одноранговых \_ членов \_**</span><span class="sxs-lookup"><span data-stu-id="e0672-119">**PEER\_MEMBER\_FLAGS**</span></span>](/windows/desktop/api/P2P/ne-p2p-peer_member_flags)                                   | <span data-ttu-id="e0672-120">Позволяет приложению указать, следует ли перечислять все элементы или только существующие, при вызове функции [**пирграупенуммемберс**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) или указать, имеется ли элемент в одноранговой группе.</span><span class="sxs-lookup"><span data-stu-id="e0672-120">Allows an application to specify whether all members or only present ones should be enumerated when the [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) function is called, or to indicate whether or not a member is present within the peer group.</span></span> |



 

 

 



