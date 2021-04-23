---
description: Структура ХАНДОФФЕНТРИ определяет определенную запись протокола в структуре ХАНДОФФТАБЛЕ.
ms.assetid: 85793326-3007-4dd9-9325-3447d6e09883
title: Структура ХАНДОФФЕНТРИ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7c04c7bc90fdd0f36beb6aed26a6b84c077eff5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540194"
---
# <a name="handoffentry-structure"></a><span data-ttu-id="ed999-103">Структура ХАНДОФФЕНТРИ</span><span class="sxs-lookup"><span data-stu-id="ed999-103">HANDOFFENTRY structure</span></span>

<span data-ttu-id="ed999-104">Структура **хандоффентри** определяет определенную запись протокола в структуре **хандоффтабле** .</span><span class="sxs-lookup"><span data-stu-id="ed999-104">The **HANDOFFENTRY** structure defines a specific protocol entry in a **HANDOFFTABLE** structure.</span></span>

<span data-ttu-id="ed999-105">Эта структура заполняется сетевой монитор на основе информации в предоставленном пользователем ini-файле, предоставленном при вызове функции [**креатехандоффтабле**](createhandofftable.md) .</span><span class="sxs-lookup"><span data-stu-id="ed999-105">This structure is filled in by Network Monitor based on information in a user supplied .ini file provided when calling the [**CreateHandoffTable**](createhandofftable.md) function.</span></span> <span data-ttu-id="ed999-106">Эта структура никогда не должна быть явно изменена приложением.</span><span class="sxs-lookup"><span data-stu-id="ed999-106">This structure should never be explicitly modified by an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed999-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed999-107">Syntax</span></span>


```C++
typedef struct _SESSIONSTATS {
  DWORD      hoe_sig;
  DWORD      hoe_ProtIdentNumber;
  HPPROTOCOL hoe_ProtocolHandle;
  DWORD      hoe_ProtocolData;
} HANDOFFENTRY, *LPHANDOFFENTRY;
```



## <a name="members"></a><span data-ttu-id="ed999-108">Члены</span><span class="sxs-lookup"><span data-stu-id="ed999-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ed999-109">**описывается \_ SIG**</span><span class="sxs-lookup"><span data-stu-id="ed999-109">**hoe\_sig**</span></span>
</dt> <dd>

<span data-ttu-id="ed999-110">Сигнатура, которая идентифицирует эту запись как запись в таблице передачи.</span><span class="sxs-lookup"><span data-stu-id="ed999-110">Signature that identifies this entry as a handoff table entry.</span></span>

</dd> <dt>

<span data-ttu-id="ed999-111">**описывается \_ протидентнумбер**</span><span class="sxs-lookup"><span data-stu-id="ed999-111">**hoe\_ProtIdentNumber**</span></span>
</dt> <dd>

<span data-ttu-id="ed999-112">Номер протокола, предоставленный пользователем. ini-файлом.</span><span class="sxs-lookup"><span data-stu-id="ed999-112">Protocol number provided by user supplied .ini file.</span></span>

</dd> <dt>

<span data-ttu-id="ed999-113">**описывается \_ протоколхандле**</span><span class="sxs-lookup"><span data-stu-id="ed999-113">**hoe\_ProtocolHandle**</span></span>
</dt> <dd>

<span data-ttu-id="ed999-114">Маркер протокола, созданный с помощью имени протокола, предоставленного пользователем. ini-файлом.</span><span class="sxs-lookup"><span data-stu-id="ed999-114">Handle of protocol created using the protocol name provided by user supplied .ini file.</span></span>

</dd> <dt>

<span data-ttu-id="ed999-115">**описывается \_ протоколдата**</span><span class="sxs-lookup"><span data-stu-id="ed999-115">**hoe\_ProtocolData**</span></span>
</dt> <dd>

<span data-ttu-id="ed999-116">Данные экземпляра протокола, предоставленные пользовательским ini-файлом.</span><span class="sxs-lookup"><span data-stu-id="ed999-116">Protocol instance data provided by user supplied .ini file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed999-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed999-117">Remarks</span></span>

<span data-ttu-id="ed999-118">Эта структура заполняется сетевой монитор когда сетевой монитор создает таблицу передачи.</span><span class="sxs-lookup"><span data-stu-id="ed999-118">This structure is filled in by Network Monitor when Network Monitor creates a handoff table.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed999-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ed999-119">Requirements</span></span>



| <span data-ttu-id="ed999-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ed999-120">Requirement</span></span> | <span data-ttu-id="ed999-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ed999-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ed999-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ed999-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ed999-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ed999-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ed999-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ed999-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ed999-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ed999-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ed999-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ed999-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed999-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed999-127"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed999-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed999-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed999-129">хандоффтабле</span><span class="sxs-lookup"><span data-stu-id="ed999-129">HANDOFFTABLE</span></span>](handofftable.md)
</dt> </dl>

 

 




