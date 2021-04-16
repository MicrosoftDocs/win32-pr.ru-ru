---
description: Структура диапазона определяет диапазон допустимых значений свойств.
ms.assetid: 7bd14410-f5c1-487b-8776-405567991e5a
title: Структура диапазона (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RANGE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: bf465636f315e60e43350bb370e2002b8a96e635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662895"
---
# <a name="range-structure"></a><span data-ttu-id="ecf73-103">Структура диапазона</span><span class="sxs-lookup"><span data-stu-id="ecf73-103">RANGE structure</span></span>

<span data-ttu-id="ecf73-104">Структура **диапазона** определяет диапазон допустимых значений свойств.</span><span class="sxs-lookup"><span data-stu-id="ecf73-104">The **RANGE** structure defines a range of valid property values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecf73-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ecf73-105">Syntax</span></span>


```C++
typedef struct range {
  DWORD MinValue;
  DWORD MaxValue;
} RANGE, *LPRANGE;
```



## <a name="members"></a><span data-ttu-id="ecf73-106">Члены</span><span class="sxs-lookup"><span data-stu-id="ecf73-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ecf73-107">**MinValue**</span><span class="sxs-lookup"><span data-stu-id="ecf73-107">**MinValue**</span></span>
</dt> <dd>

<span data-ttu-id="ecf73-108">Наименьшее возможное значение в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="ecf73-108">Lowest possible value in a range.</span></span>

</dd> <dt>

<span data-ttu-id="ecf73-109">**MaxValue**</span><span class="sxs-lookup"><span data-stu-id="ecf73-109">**MaxValue**</span></span>
</dt> <dd>

<span data-ttu-id="ecf73-110">Наибольшее возможное значение в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="ecf73-110">Highest possible value in a range.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ecf73-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ecf73-111">Remarks</span></span>

<span data-ttu-id="ecf73-112">Структура **диапазона** используется для указания допустимого диапазона чисел для свойства протокола.</span><span class="sxs-lookup"><span data-stu-id="ecf73-112">The **RANGE** structure is used to specify a valid range of numbers for a protocol property.</span></span> <span data-ttu-id="ecf73-113">Если элементу **квалификатора** класса **PropertyInfo** задано значение **prop \_ куал \_ Range**, то элемент **лпранже** структуры [PropertyInfo](propertyinfo.md) должен предоставить указатель на структуру **диапазона** .</span><span class="sxs-lookup"><span data-stu-id="ecf73-113">If the **DataQualifier** member of the **PROPERTYINFO** structure is set to **PROP\_QUAL\_RANGE**, the **lpRange** member of the [PROPERTYINFO](propertyinfo.md) structure must provide a pointer to a **RANGE** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecf73-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ecf73-114">Requirements</span></span>



| <span data-ttu-id="ecf73-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ecf73-115">Requirement</span></span> | <span data-ttu-id="ecf73-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ecf73-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ecf73-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ecf73-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ecf73-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ecf73-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ecf73-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ecf73-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ecf73-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ecf73-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ecf73-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ecf73-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecf73-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecf73-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecf73-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ecf73-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecf73-124">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="ecf73-124">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> </dl>

 

 




