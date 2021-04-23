---
description: Этот класс является классом типа события для ALPC получения сообщений о событиях. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 6aa98240-e559-47b6-ae55-5a6379e08077
title: Класс ALPC_Receive_Message
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Receive_Message
- ALPC_Receive_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 886d3595caa283d5b09939a506952633d2350d41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984533"
---
# <a name="alpc_receive_message-class"></a><span data-ttu-id="a0a36-104">ALPC \_ , \_ класс сообщения</span><span class="sxs-lookup"><span data-stu-id="a0a36-104">ALPC\_Receive\_Message class</span></span>

<span data-ttu-id="a0a36-105">Этот класс является классом типа события для ALPC получения сообщений о событиях.</span><span class="sxs-lookup"><span data-stu-id="a0a36-105">This class is the event type class for ALPC receive message events.</span></span>

<span data-ttu-id="a0a36-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="a0a36-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0a36-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0a36-107">Syntax</span></span>

``` syntax
[EventType(34), EventTypeName("ALPC-Receive-Message")]
class ALPC_Receive_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a><span data-ttu-id="a0a36-108">Участники</span><span class="sxs-lookup"><span data-stu-id="a0a36-108">Members</span></span>

<span data-ttu-id="a0a36-109">Класс **\_ \_ сообщений ALPC получит** следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a0a36-109">The **ALPC\_Receive\_Message** class has these types of members:</span></span>

-   [<span data-ttu-id="a0a36-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a0a36-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a0a36-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a0a36-111">Properties</span></span>

<span data-ttu-id="a0a36-112">Класс **\_ \_ сообщений о получении в ALPC** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a0a36-112">The **ALPC\_Receive\_Message** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a0a36-113">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="a0a36-113">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0a36-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a0a36-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a0a36-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0a36-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a0a36-116">Идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="a0a36-116">Message identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0a36-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a0a36-117">Requirements</span></span>



| <span data-ttu-id="a0a36-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a0a36-118">Requirement</span></span> | <span data-ttu-id="a0a36-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a0a36-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a0a36-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0a36-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a0a36-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a0a36-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a0a36-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0a36-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a0a36-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a0a36-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




