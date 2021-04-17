---
description: 'Возвращает состояние подключения устройства. Это свойство применяется только к элементам типа "устройство" (корневые элементы). Возможные значения: &\# 0034; connected&\# 0034;, &\# 0034; disconnected&\# 0034; или null (если это свойство не применяется к элементу). Только для чтения.'
ms.assetid: 44b1713a-5859-4973-8495-e8a67f2344b2
title: Свойство Item. Коннектстатус
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.ConnectStatus
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 48e12c35ad98746f5a263680e74a09c814bbc65a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711961"
---
# <a name="itemconnectstatus-property"></a><span data-ttu-id="9cc29-106">Свойство Item. Коннектстатус</span><span class="sxs-lookup"><span data-stu-id="9cc29-106">Item.ConnectStatus property</span></span>

<span data-ttu-id="9cc29-107">Возвращает состояние подключения устройства.</span><span class="sxs-lookup"><span data-stu-id="9cc29-107">Retrieves the connection status of the device.</span></span> <span data-ttu-id="9cc29-108">Это свойство применяется только к элементам типа "устройство" (корневые элементы).</span><span class="sxs-lookup"><span data-stu-id="9cc29-108">This property applies only to items of type device (root items).</span></span> <span data-ttu-id="9cc29-109">Возможные значения: "Connected", "disconnected" или **null** (если это свойство не применяется к элементу).</span><span class="sxs-lookup"><span data-stu-id="9cc29-109">Possible values are "connected", "disconnected", or **NULL** (if this property does not apply to the item).</span></span> <span data-ttu-id="9cc29-110">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9cc29-110">Read-only.</span></span>

<span data-ttu-id="9cc29-111">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9cc29-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cc29-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9cc29-112">Syntax</span></span>


```JScript
propVal = Item.ConnectStatus
```



## <a name="property-value"></a><span data-ttu-id="9cc29-113">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9cc29-113">Property value</span></span>

<span data-ttu-id="9cc29-114">Строка, которая получает состояние подключения.</span><span class="sxs-lookup"><span data-stu-id="9cc29-114">String that receives the connection status.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cc29-115">Требования</span><span class="sxs-lookup"><span data-stu-id="9cc29-115">Requirements</span></span>



| <span data-ttu-id="9cc29-116">Требование</span><span class="sxs-lookup"><span data-stu-id="9cc29-116">Requirement</span></span> | <span data-ttu-id="9cc29-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9cc29-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cc29-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9cc29-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9cc29-119">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9cc29-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9cc29-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9cc29-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9cc29-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9cc29-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9cc29-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9cc29-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cc29-123"><dt>Wiascr.dll (версия 4,90 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="9cc29-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




