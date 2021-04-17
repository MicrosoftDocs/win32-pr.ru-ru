---
description: Структура ПРОПЕРТИНСТЕКС определяет экземпляр расширенного свойства с полилинией.
ms.assetid: a2316baf-07e2-4617-bb35-e20cfb11fbcb
title: Структура ПРОПЕРТИНСТЕКС (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROPERTYINSTEX
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: f7b196d30e96f9d047f7f923d969d65a918aa4f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673235"
---
# <a name="propertyinstex-structure"></a><span data-ttu-id="7833a-103">Структура ПРОПЕРТИНСТЕКС</span><span class="sxs-lookup"><span data-stu-id="7833a-103">PROPERTYINSTEX structure</span></span>

<span data-ttu-id="7833a-104">Структура **пропертинстекс** определяет экземпляр расширенного свойства с полилинией.</span><span class="sxs-lookup"><span data-stu-id="7833a-104">The **PROPERTYINSTEX** structure defines a freeform, extended property instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="7833a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7833a-105">Syntax</span></span>


```C++
typedef struct _PROPERTYINSTEX {
  WORD    Length;
  WORD    LengthEx;
  ULPVOID lpData;
  union {
    BYTE          Byte[];
    WORD          Word[];
    DWORD         Dword[];
    LARGE_INTEGER LargeInt[];
    SYSTEMTIME    SysTime[];
    TYPED_STRING  TypedString;
  };
} PROPERTYINSTEX;
```



## <a name="members"></a><span data-ttu-id="7833a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="7833a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7833a-107">**Длина**</span><span class="sxs-lookup"><span data-stu-id="7833a-107">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="7833a-108">Длина данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="7833a-108">Length of the data in Bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7833a-109">**ленгсекс**</span><span class="sxs-lookup"><span data-stu-id="7833a-109">**LengthEx**</span></span>
</dt> <dd>

<span data-ttu-id="7833a-110">Длина расширенных данных.</span><span class="sxs-lookup"><span data-stu-id="7833a-110">Length of the extended data.</span></span>

</dd> <dt>

<span data-ttu-id="7833a-111">**лпдата**</span><span class="sxs-lookup"><span data-stu-id="7833a-111">**lpData**</span></span>
</dt> <dd>

<span data-ttu-id="7833a-112">Указатель на Расширенные данные.</span><span class="sxs-lookup"><span data-stu-id="7833a-112">Pointer to the extended data.</span></span>

</dd> <dt>

<span data-ttu-id="7833a-113">**Byte**</span><span class="sxs-lookup"><span data-stu-id="7833a-113">**Byte**</span></span>
</dt> <dd>

<span data-ttu-id="7833a-114">Указатель на **байтовые** данные.</span><span class="sxs-lookup"><span data-stu-id="7833a-114">Pointer to the **BYTE** data.</span></span>

</dd> <dt>

<span data-ttu-id="7833a-115">**Word**</span><span class="sxs-lookup"><span data-stu-id="7833a-115">**Word**</span></span>
</dt> <dd>

<span data-ttu-id="7833a-116">Указатель на данные **слова** .</span><span class="sxs-lookup"><span data-stu-id="7833a-116">Pointer to the **WORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="7833a-117">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="7833a-117">**Dword**</span></span>
</dt> <dd>

<span data-ttu-id="7833a-118">Указатель на данные **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="7833a-118">Pointer to the **DWORD** data.</span></span>

</dd> <dt>

<span data-ttu-id="7833a-119">**ларжеинт**</span><span class="sxs-lookup"><span data-stu-id="7833a-119">**LargeInt**</span></span>
</dt> <dd>

<span data-ttu-id="7833a-120">Указатель на данные **ларжеинт** .</span><span class="sxs-lookup"><span data-stu-id="7833a-120">Pointer to the **LARGEINT** data.</span></span>

</dd> <dt>

<span data-ttu-id="7833a-121">**систиме**</span><span class="sxs-lookup"><span data-stu-id="7833a-121">**SysTime**</span></span>
</dt> <dd>

<span data-ttu-id="7833a-122">Указатель на данные **SYSTEMTIME** .</span><span class="sxs-lookup"><span data-stu-id="7833a-122">Pointer to the **SYSTEMTIME** data.</span></span>

</dd> <dt>

<span data-ttu-id="7833a-123">**типедстринг**</span><span class="sxs-lookup"><span data-stu-id="7833a-123">**TypedString**</span></span>
</dt> <dd>

<span data-ttu-id="7833a-124">Типизированная строка, которая может иметь Расширенные данные.</span><span class="sxs-lookup"><span data-stu-id="7833a-124">A typed string that may have extended data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7833a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="7833a-125">Requirements</span></span>



| <span data-ttu-id="7833a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="7833a-126">Requirement</span></span> | <span data-ttu-id="7833a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7833a-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7833a-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7833a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7833a-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7833a-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7833a-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7833a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7833a-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7833a-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7833a-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7833a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7833a-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7833a-133"><dt>Netmon.h</dt></span></span> </dl> |



 

 




