---
description: Этот класс является классом типа событий для ALPC "Отправка сообщения о событиях". Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 7f12259b-f737-4bef-9dea-2ffe3517e0da
title: Класс ALPC_Send_Message
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Send_Message
- ALPC_Send_Message.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: c9437626341f0ac57136645d40a8389436e8af1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154854"
---
# <a name="alpc_send_message-class"></a><span data-ttu-id="81db3-104">ALPC. \_ Отправка \_ класса сообщения</span><span class="sxs-lookup"><span data-stu-id="81db3-104">ALPC\_Send\_Message class</span></span>

<span data-ttu-id="81db3-105">Этот класс является классом типа событий для ALPC "Отправка сообщения о событиях".</span><span class="sxs-lookup"><span data-stu-id="81db3-105">This class is the event type class for ALPC send message events.</span></span>

<span data-ttu-id="81db3-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="81db3-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="81db3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81db3-107">Syntax</span></span>

``` syntax
[EventType(33), EventTypeName("ALPC-Send-Message")]
class ALPC_Send_Message : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a><span data-ttu-id="81db3-108">Участники</span><span class="sxs-lookup"><span data-stu-id="81db3-108">Members</span></span>

<span data-ttu-id="81db3-109">Класс **\_ \_ сообщения ALPC Send** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="81db3-109">The **ALPC\_Send\_Message** class has these types of members:</span></span>

-   [<span data-ttu-id="81db3-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="81db3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="81db3-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="81db3-111">Properties</span></span>

<span data-ttu-id="81db3-112">Класс **\_ \_ сообщения ALPC Send** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="81db3-112">The **ALPC\_Send\_Message** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81db3-113">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="81db3-113">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81db3-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81db3-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81db3-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="81db3-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81db3-116">Идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="81db3-116">Message identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81db3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="81db3-117">Requirements</span></span>



| <span data-ttu-id="81db3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="81db3-118">Requirement</span></span> | <span data-ttu-id="81db3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="81db3-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="81db3-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81db3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="81db3-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81db3-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="81db3-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81db3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="81db3-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="81db3-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




