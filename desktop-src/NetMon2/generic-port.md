---
description: Содержит номер порта, используемый для протоколов IP или IPX.
ms.assetid: 730f6ee6-7b7d-4e10-91ee-a4ba87aae5aa
title: Объединение GENERIC_PORT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GENERIC_PORT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3b684ffea65e85854d2928931f492fb247cc0b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990910"
---
# <a name="generic_port-union"></a><span data-ttu-id="3d830-103">УНИВЕРСАЛЬНое \_ объединение портов</span><span class="sxs-lookup"><span data-stu-id="3d830-103">GENERIC\_PORT union</span></span>

<span data-ttu-id="3d830-104">**Универсальная структура \_ порта** содержит номер порта, используемый для протоколов IP или IPX.</span><span class="sxs-lookup"><span data-stu-id="3d830-104">The **GENERIC\_PORT** structure contains a port number used for IP or IPX protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d830-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d830-105">Syntax</span></span>


```C++
typedef union {
  BYTE IPPort;
  WORD ByteSwappedIPXPort;
} GENERIC_PORT;
```



## <a name="members"></a><span data-ttu-id="3d830-106">Члены</span><span class="sxs-lookup"><span data-stu-id="3d830-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3d830-107">**иппорт**</span><span class="sxs-lookup"><span data-stu-id="3d830-107">**IPPort**</span></span>
</dt> <dd>

<span data-ttu-id="3d830-108">Номер IP-порта, введенный в.</span><span class="sxs-lookup"><span data-stu-id="3d830-108">IP port number filled in.</span></span>

</dd> <dt>

<span data-ttu-id="3d830-109">**битесваппедипкспорт**</span><span class="sxs-lookup"><span data-stu-id="3d830-109">**ByteSwappedIPXPort**</span></span>
</dt> <dd>

<span data-ttu-id="3d830-110">Номер порта IPX, введенный в.</span><span class="sxs-lookup"><span data-stu-id="3d830-110">IPX port number filled in.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3d830-111">Требования</span><span class="sxs-lookup"><span data-stu-id="3d830-111">Requirements</span></span>



| <span data-ttu-id="3d830-112">Требование</span><span class="sxs-lookup"><span data-stu-id="3d830-112">Requirement</span></span> | <span data-ttu-id="3d830-113">Значение</span><span class="sxs-lookup"><span data-stu-id="3d830-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3d830-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d830-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3d830-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3d830-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3d830-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d830-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3d830-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3d830-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3d830-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3d830-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d830-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d830-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




