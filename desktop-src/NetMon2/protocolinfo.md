---
description: Структура ПРОТОКОЛИНФО описывает протокол.
ms.assetid: 7f936c93-a942-4591-9abc-59872df0964e
title: Структура ПРОТОКОЛИНФО (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ed1410148a72c57b860fdfdaee447dcca505d99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674084"
---
# <a name="protocolinfo-structure"></a><span data-ttu-id="503a0-103">Структура ПРОТОКОЛИНФО</span><span class="sxs-lookup"><span data-stu-id="503a0-103">PROTOCOLINFO structure</span></span>

<span data-ttu-id="503a0-104">Структура **протоколинфо** описывает протокол.</span><span class="sxs-lookup"><span data-stu-id="503a0-104">The **PROTOCOLINFO** structure describes a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="503a0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="503a0-105">Syntax</span></span>


```C++
typedef struct _PROTOCOLINFO {
  DWORD              ProtocolID;
  LPPROPERTYDATABASE PropertyDatabase;
  BYTE               ProtocolName[16];
  BYTE               HelpFile[16];
  BYTE               Comment[128];
} PROTOCOLINFO, *LPPROTOCOLINFO;
```



## <a name="members"></a><span data-ttu-id="503a0-106">Члены</span><span class="sxs-lookup"><span data-stu-id="503a0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="503a0-107">**протоколид**</span><span class="sxs-lookup"><span data-stu-id="503a0-107">**ProtocolID**</span></span>
</dt> <dd>

<span data-ttu-id="503a0-108">Назначенный системой идентификатор протокола для указанного сеанса выполнения.</span><span class="sxs-lookup"><span data-stu-id="503a0-108">System-assigned protocol identifier of the specified run session.</span></span>

</dd> <dt>

<span data-ttu-id="503a0-109">**пропертидатабасе**</span><span class="sxs-lookup"><span data-stu-id="503a0-109">**PropertyDatabase**</span></span>
</dt> <dd>

<span data-ttu-id="503a0-110">База данных свойств указанного протокола.</span><span class="sxs-lookup"><span data-stu-id="503a0-110">Property database of the specified protocol.</span></span>

</dd> <dt>

<span data-ttu-id="503a0-111">**ProtocolName**</span><span class="sxs-lookup"><span data-stu-id="503a0-111">**ProtocolName**</span></span>
</dt> <dd>

<span data-ttu-id="503a0-112">Сокращенное имя протокола.</span><span class="sxs-lookup"><span data-stu-id="503a0-112">Abbreviated protocol name.</span></span>

</dd> <dt>

<span data-ttu-id="503a0-113">**HelpFile**</span><span class="sxs-lookup"><span data-stu-id="503a0-113">**HelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="503a0-114">Необязательное имя файла справки, связанное с протоколом.</span><span class="sxs-lookup"><span data-stu-id="503a0-114">Optional Help file name associated with the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="503a0-115">**Комментарий**</span><span class="sxs-lookup"><span data-stu-id="503a0-115">**Comment**</span></span>
</dt> <dd>

<span data-ttu-id="503a0-116">Комментарий, описывающий протокол.</span><span class="sxs-lookup"><span data-stu-id="503a0-116">A comment describing the protocol.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="503a0-117">Требования</span><span class="sxs-lookup"><span data-stu-id="503a0-117">Requirements</span></span>



| <span data-ttu-id="503a0-118">Требование</span><span class="sxs-lookup"><span data-stu-id="503a0-118">Requirement</span></span> | <span data-ttu-id="503a0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="503a0-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="503a0-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="503a0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="503a0-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="503a0-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="503a0-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="503a0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="503a0-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="503a0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="503a0-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="503a0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="503a0-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="503a0-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




