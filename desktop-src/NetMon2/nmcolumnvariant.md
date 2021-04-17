---
description: Предоставляет линию в верхней области Просмотр событий, которая служит контейнером для всех возможных данных, вставленных в столбец.
ms.assetid: 2ad32c23-5dbe-46be-b0cc-ccf7a6fe8ec3
title: Структура НМКОЛУМНВАРИАНТ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNVARIANT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: e9f70d2d1a0caf63411fcd2b44d5ed8bdcbecd00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664573"
---
# <a name="nmcolumnvariant-structure"></a><span data-ttu-id="5b763-103">Структура НМКОЛУМНВАРИАНТ</span><span class="sxs-lookup"><span data-stu-id="5b763-103">NMCOLUMNVARIANT structure</span></span>

<span data-ttu-id="5b763-104">Структура **нмколумнвариант** предоставляет линию в верхней области Просмотр событий, которая служит контейнером для всех возможных данных, вставленных в столбец.</span><span class="sxs-lookup"><span data-stu-id="5b763-104">The **NMCOLUMNVARIANT** structure provides a line in the top pane of the Event Viewer that serves as a container for all possible data inserted into a column.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b763-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b763-105">Syntax</span></span>


```C++
typedef struct {
  NMCOLUMNTYPE Type;
  union {
    BYTE        Uint8Val;
    char        Sint8Val;
    WORD        Uint16Val;
    short       Sint16Val;
    DWORD       Uint32Val;
    LONG        Sint32Val;
    DOUBLE      Float64Val;
    DWORD       FrameVal;
    BOOL        YesNoVal;
    BOOL        OnOffVal;
    BOOL        TrueFalseVal;
    BYTE        MACAddrVal[MAC_ADDRESS_SIZE];
    IPX_ADDRESS IPXAddrVal;
    DWORD       IPAddrVal;
    DOUBLE      VarTimeVal;
    LPSTR       pStringVal;
  } Value;
} NMCOLUMNVARIANT;
```



## <a name="members"></a><span data-ttu-id="5b763-106">Члены</span><span class="sxs-lookup"><span data-stu-id="5b763-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5b763-107">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5b763-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="5b763-108">Значение из типа перечисления [**нмколумнтипе**](nmcolumntype.md) .</span><span class="sxs-lookup"><span data-stu-id="5b763-108">A value from the [**NMCOLUMNTYPE**](nmcolumntype.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="5b763-109">**Значение**</span><span class="sxs-lookup"><span data-stu-id="5b763-109">**Value**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b763-110">**Uint8Val**</span><span class="sxs-lookup"><span data-stu-id="5b763-110">**Uint8Val**</span></span>
</dt> <dd>

<span data-ttu-id="5b763-111">8-битовое целочисленное значение без знака.</span><span class="sxs-lookup"><span data-stu-id="5b763-111">8-bit unsigned integer value.</span></span>

</dd> <dt>

<span data-ttu-id="5b763-112">**Sint8Val**</span><span class="sxs-lookup"><span data-stu-id="5b763-112">**Sint8Val**</span></span>
</dt> <dd>

<span data-ttu-id="5b763-113">8-битовое целочисленное значение со знаком.</span><span class="sxs-lookup"><span data-stu-id="5b763-113">8-bit signed integer value.</span></span>

</dd> <dt>

<span data-ttu-id="5b763-114">**Uint16Val**</span><span class="sxs-lookup"><span data-stu-id="5b763-114">**Uint16Val**</span></span>
</dt> <dd>

<span data-ttu-id="5b763-115">16-битовое целочисленное значение без знака.</span><span class="sxs-lookup"><span data-stu-id="5b763-115">16-bit unsigned integer value.</span></span>

</dd> <dt>

<span data-ttu-id="5b763-116">**Sint16Val**</span><span class="sxs-lookup"><span data-stu-id="5b763-116">**Sint16Val**</span></span>
</dt> <dd>

<span data-ttu-id="5b763-117">16-разрядное целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="5b763-117">16-bit signed integer value.</span></span>

</dd> <dt>

<span data-ttu-id="5b763-118">**Uint32Val**</span><span class="sxs-lookup"><span data-stu-id="5b763-118">**Uint32Val**</span></span>
</dt> <dd>

<span data-ttu-id="5b763-119">32-битовое целочисленное значение без знака.</span><span class="sxs-lookup"><span data-stu-id="5b763-119">32-bit unsigned integer value.</span></span>

</dd> <dt>

<span data-ttu-id="5b763-120">**Sint32Val**</span><span class="sxs-lookup"><span data-stu-id="5b763-120">**Sint32Val**</span></span>
</dt> <dd>

<span data-ttu-id="5b763-121">32-битовое целочисленное значение со знаком.</span><span class="sxs-lookup"><span data-stu-id="5b763-121">32-bit signed integer value.</span></span>

</dd> <dt>

<span data-ttu-id="5b763-122">**Float64Val**</span><span class="sxs-lookup"><span data-stu-id="5b763-122">**Float64Val**</span></span>
</dt> <dd>

<span data-ttu-id="5b763-123">64-разрядное значение с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="5b763-123">64-bit float value.</span></span>

</dd> <dt>

<span data-ttu-id="5b763-124">**фрамевал**</span><span class="sxs-lookup"><span data-stu-id="5b763-124">**FrameVal**</span></span>
</dt> <dd>

<span data-ttu-id="5b763-125">Номер кадра.</span><span class="sxs-lookup"><span data-stu-id="5b763-125">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="5b763-126">**есновал**</span><span class="sxs-lookup"><span data-stu-id="5b763-126">**YesNoVal**</span></span>
</dt> <dd>

<span data-ttu-id="5b763-127">Отображается значение Да или нет.</span><span class="sxs-lookup"><span data-stu-id="5b763-127">Displays Yes or No.</span></span>

</dd> <dt>

<span data-ttu-id="5b763-128">**оноффвал**</span><span class="sxs-lookup"><span data-stu-id="5b763-128">**OnOffVal**</span></span>
</dt> <dd>

<span data-ttu-id="5b763-129">Отображение или отключение.</span><span class="sxs-lookup"><span data-stu-id="5b763-129">Displays On or Off.</span></span>

</dd> <dt>

<span data-ttu-id="5b763-130">**труефалсевал**</span><span class="sxs-lookup"><span data-stu-id="5b763-130">**TrueFalseVal**</span></span>
</dt> <dd>

<span data-ttu-id="5b763-131">Отображает значение true или false.</span><span class="sxs-lookup"><span data-stu-id="5b763-131">Displays True or False.</span></span>

</dd> <dt>

<span data-ttu-id="5b763-132">**макаддрвал**</span><span class="sxs-lookup"><span data-stu-id="5b763-132">**MACAddrVal**</span></span>
</dt> <dd>

<span data-ttu-id="5b763-133">MAC-адрес.</span><span class="sxs-lookup"><span data-stu-id="5b763-133">MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="5b763-134">**ипксаддрвал**</span><span class="sxs-lookup"><span data-stu-id="5b763-134">**IPXAddrVal**</span></span>
</dt> <dd>

<span data-ttu-id="5b763-135">IPX-адрес.</span><span class="sxs-lookup"><span data-stu-id="5b763-135">IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="5b763-136">**ипаддрвал**</span><span class="sxs-lookup"><span data-stu-id="5b763-136">**IPAddrVal**</span></span>
</dt> <dd>

<span data-ttu-id="5b763-137">IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="5b763-137">IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5b763-138">**вартимевал**</span><span class="sxs-lookup"><span data-stu-id="5b763-138">**VarTimeVal**</span></span>
</dt> <dd>

<span data-ttu-id="5b763-139">Вариант времени.</span><span class="sxs-lookup"><span data-stu-id="5b763-139">Variant time.</span></span> <span data-ttu-id="5b763-140">Используйте **варианттиметосистемтиме** для преобразования в системное время.</span><span class="sxs-lookup"><span data-stu-id="5b763-140">Use **VariantTimetoSystemTime** to convert to system time.</span></span>

</dd> <dt>

<span data-ttu-id="5b763-141">**пстрингвал**</span><span class="sxs-lookup"><span data-stu-id="5b763-141">**pStringVal**</span></span>
</dt> <dd>

<span data-ttu-id="5b763-142">Указатель на строку.</span><span class="sxs-lookup"><span data-stu-id="5b763-142">Pointer to a string.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b763-143">Требования</span><span class="sxs-lookup"><span data-stu-id="5b763-143">Requirements</span></span>



| <span data-ttu-id="5b763-144">Требование</span><span class="sxs-lookup"><span data-stu-id="5b763-144">Requirement</span></span> | <span data-ttu-id="5b763-145">Значение</span><span class="sxs-lookup"><span data-stu-id="5b763-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5b763-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5b763-146">Minimum supported client</span></span><br/> | <span data-ttu-id="5b763-147">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5b763-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5b763-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5b763-148">Minimum supported server</span></span><br/> | <span data-ttu-id="5b763-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5b763-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5b763-150">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5b763-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b763-151"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b763-151"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b763-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b763-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b763-153">**нмколумнтипе**</span><span class="sxs-lookup"><span data-stu-id="5b763-153">**NMCOLUMNTYPE**</span></span>](nmcolumntype.md)
</dt> </dl>

 

 




