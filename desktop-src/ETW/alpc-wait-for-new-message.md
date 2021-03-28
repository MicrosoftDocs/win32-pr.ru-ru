---
description: Этот класс является классом типа событий для ALPC ожидание новых событий сообщения. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 7f7fa4b8-ed12-49a0-a84e-37f66af4f5f1
title: Класс ALPC_Wait_For_New_Message
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Wait_For_New_Message
- ALPC_Wait_For_New_Message.IsServerPort
- ALPC_Wait_For_New_Message.PortName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 75cbda11a2a27eec811f8ff47966d12c6a86cf07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984528"
---
# <a name="alpc_wait_for_new_message-class"></a><span data-ttu-id="e62bd-104">ALPC. \_ Ожидание \_ \_ нового \_ класса сообщений</span><span class="sxs-lookup"><span data-stu-id="e62bd-104">ALPC\_Wait\_For\_New\_Message class</span></span>

<span data-ttu-id="e62bd-105">Этот класс является классом типа событий для ALPC ожидание новых событий сообщения.</span><span class="sxs-lookup"><span data-stu-id="e62bd-105">This class is the event type class for ALPC wait for new message events.</span></span>

<span data-ttu-id="e62bd-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="e62bd-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e62bd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e62bd-107">Syntax</span></span>

``` syntax
[EventType(36), EventTypeName("ALPC-Wait-For-New-Message")]
class ALPC_Wait_For_New_Message : ALPC
{
  uint32 IsServerPort;
  string PortName;
};
```

## <a name="members"></a><span data-ttu-id="e62bd-108">Участники</span><span class="sxs-lookup"><span data-stu-id="e62bd-108">Members</span></span>

<span data-ttu-id="e62bd-109">В **ALPC \_ Ожидание \_ \_ нового класса \_ сообщений** входят следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e62bd-109">The **ALPC\_Wait\_For\_New\_Message** class has these types of members:</span></span>

-   [<span data-ttu-id="e62bd-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="e62bd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e62bd-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="e62bd-111">Properties</span></span>

<span data-ttu-id="e62bd-112">В **ALPC \_ Ожидание \_ \_ нового класса \_ сообщений** имеются следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e62bd-112">The **ALPC\_Wait\_For\_New\_Message** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e62bd-113">**иссерверпорт**</span><span class="sxs-lookup"><span data-stu-id="e62bd-113">**IsServerPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e62bd-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e62bd-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e62bd-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e62bd-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e62bd-116">Указывает, является ли порт портом сервера.</span><span class="sxs-lookup"><span data-stu-id="e62bd-116">Indicates if the port is a server port.</span></span>

</dd> <dt>

<span data-ttu-id="e62bd-117">**портнаме**</span><span class="sxs-lookup"><span data-stu-id="e62bd-117">**PortName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e62bd-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e62bd-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e62bd-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e62bd-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e62bd-120">Строка, содержащая имя порта, в котором находится ожидание ALPC.</span><span class="sxs-lookup"><span data-stu-id="e62bd-120">String that contains the name of the port on which ALPC is waiting.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e62bd-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e62bd-121">Requirements</span></span>



| <span data-ttu-id="e62bd-122">Требование</span><span class="sxs-lookup"><span data-stu-id="e62bd-122">Requirement</span></span> | <span data-ttu-id="e62bd-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e62bd-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e62bd-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e62bd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e62bd-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e62bd-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e62bd-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e62bd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e62bd-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e62bd-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




