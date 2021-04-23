---
description: Этот класс является классом типа событий для ALPC ожидание событий ответа. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 9aaa2c93-41cc-4025-80f9-b7740a37c4d8
title: Класс ALPC_Wait_For_Reply
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Wait_For_Reply
- ALPC_Wait_For_Reply.MessageID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 898077511db25ec7f53bc075ecb845d04e540626
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984525"
---
# <a name="alpc_wait_for_reply-class"></a><span data-ttu-id="790d6-104">ALPC. \_ Ожидание \_ \_ класса ответа</span><span class="sxs-lookup"><span data-stu-id="790d6-104">ALPC\_Wait\_For\_Reply class</span></span>

<span data-ttu-id="790d6-105">Этот класс является классом типа событий для ALPC ожидание событий ответа.</span><span class="sxs-lookup"><span data-stu-id="790d6-105">This class is the event type class for ALPC wait for reply events.</span></span>

<span data-ttu-id="790d6-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="790d6-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="790d6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="790d6-107">Syntax</span></span>

``` syntax
[EventType(35), EventTypeName("ALPC-Wait-For-Reply")]
class ALPC_Wait_For_Reply : ALPC
{
  uint32 MessageID;
};
```

## <a name="members"></a><span data-ttu-id="790d6-108">Участники</span><span class="sxs-lookup"><span data-stu-id="790d6-108">Members</span></span>

<span data-ttu-id="790d6-109">Классу « **\_ ожидание в классе \_ \_ ответов** » в ALPC имеются следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="790d6-109">The **ALPC\_Wait\_For\_Reply** class has these types of members:</span></span>

-   [<span data-ttu-id="790d6-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="790d6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="790d6-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="790d6-111">Properties</span></span>

<span data-ttu-id="790d6-112">Эти свойства имеют класс **ALPC \_ Wait \_ для класса \_ Reply** .</span><span class="sxs-lookup"><span data-stu-id="790d6-112">The **ALPC\_Wait\_For\_Reply** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="790d6-113">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="790d6-113">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="790d6-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="790d6-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="790d6-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="790d6-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="790d6-116">Идентификатор сообщения.</span><span class="sxs-lookup"><span data-stu-id="790d6-116">Message identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="790d6-117">Требования</span><span class="sxs-lookup"><span data-stu-id="790d6-117">Requirements</span></span>



| <span data-ttu-id="790d6-118">Требование</span><span class="sxs-lookup"><span data-stu-id="790d6-118">Requirement</span></span> | <span data-ttu-id="790d6-119">Значение</span><span class="sxs-lookup"><span data-stu-id="790d6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="790d6-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="790d6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="790d6-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="790d6-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="790d6-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="790d6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="790d6-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="790d6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




