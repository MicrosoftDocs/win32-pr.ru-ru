---
description: Структура МАКФРАМЕ — это объединение наиболее распространенных начальных протоколов.
ms.assetid: ec7e3a54-a47f-4390-a137-9574c63c9a11
title: Объединение МАКФРАМЕ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MACFRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a7901daf467a63586543c52ca8a214d5d0094982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662450"
---
# <a name="macframe-union"></a><span data-ttu-id="20402-103">Объединение МАКФРАМЕ</span><span class="sxs-lookup"><span data-stu-id="20402-103">MACFRAME union</span></span>

<span data-ttu-id="20402-104">Структура **макфраме** — это объединение наиболее распространенных начальных протоколов.</span><span class="sxs-lookup"><span data-stu-id="20402-104">The **MACFRAME** structure is a union of the most common initial protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="20402-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20402-105">Syntax</span></span>


```C++
typedef union {
  LPBYTE      MacHeader;
  LPETHERNET  Ethernet;
  LPTOKENRING Tokenring;
  LPFDDI      Fddi;
} MACFRAME, *LPMACFRAME;
```



## <a name="members"></a><span data-ttu-id="20402-106">Члены</span><span class="sxs-lookup"><span data-stu-id="20402-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="20402-107">**мачеадер**</span><span class="sxs-lookup"><span data-stu-id="20402-107">**MacHeader**</span></span>
</dt> <dd>

<span data-ttu-id="20402-108">Универсальный указатель на кадр.</span><span class="sxs-lookup"><span data-stu-id="20402-108">Generic pointer to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="20402-109">**Ethernet**</span><span class="sxs-lookup"><span data-stu-id="20402-109">**Ethernet**</span></span>
</dt> <dd>

<span data-ttu-id="20402-110">Указатель Ethernet на кадр.</span><span class="sxs-lookup"><span data-stu-id="20402-110">Ethernet pointer to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="20402-111">**токенринг**</span><span class="sxs-lookup"><span data-stu-id="20402-111">**Tokenring**</span></span>
</dt> <dd>

<span data-ttu-id="20402-112">Указатель кольца маркера на кадр.</span><span class="sxs-lookup"><span data-stu-id="20402-112">Token ring pointer to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="20402-113">**FDDI**</span><span class="sxs-lookup"><span data-stu-id="20402-113">**Fddi**</span></span>
</dt> <dd>

<span data-ttu-id="20402-114">FDDI-указатель на кадр.</span><span class="sxs-lookup"><span data-stu-id="20402-114">FDDI pointer to a frame.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20402-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20402-115">Remarks</span></span>

<span data-ttu-id="20402-116">Эта структура чаще всего используется в качестве наложения.</span><span class="sxs-lookup"><span data-stu-id="20402-116">This structure is most frequently used as an overlay.</span></span> <span data-ttu-id="20402-117">Чтобы сделать свойства первого протокола доступными, приведите кадр к тому же типу, что и для протокола.</span><span class="sxs-lookup"><span data-stu-id="20402-117">To make the properties of the first protocol accessible, cast the frame as the same type as the protocol.</span></span>

## <a name="requirements"></a><span data-ttu-id="20402-118">Требования</span><span class="sxs-lookup"><span data-stu-id="20402-118">Requirements</span></span>



| <span data-ttu-id="20402-119">Требование</span><span class="sxs-lookup"><span data-stu-id="20402-119">Requirement</span></span> | <span data-ttu-id="20402-120">Значение</span><span class="sxs-lookup"><span data-stu-id="20402-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="20402-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="20402-121">Minimum supported client</span></span><br/> | <span data-ttu-id="20402-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="20402-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="20402-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="20402-123">Minimum supported server</span></span><br/> | <span data-ttu-id="20402-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="20402-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="20402-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="20402-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="20402-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="20402-126"><dt>Netmon.h</dt></span></span> </dl> |



 

 




