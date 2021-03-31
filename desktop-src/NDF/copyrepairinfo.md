---
title: Функция Копирепаиринфо (Ндаттрибутилс. h)
description: Создает копию структуры Репаиринфо.
ms.assetid: a1147ce6-9a90-4a46-8fe4-da3353391a13
keywords:
- Копирепаиринфо функция NDF
topic_type:
- apiref
api_name:
- CopyRepairInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a24d15ec5a8a69b3c8c40700273ebcb6f32bcfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988436"
---
# <a name="copyrepairinfo-function"></a><span data-ttu-id="f1108-104">Функция Копирепаиринфо</span><span class="sxs-lookup"><span data-stu-id="f1108-104">CopyRepairInfo function</span></span>

<span data-ttu-id="f1108-105">Функция **копирепаиринфо** создает копию структуры [**репаиринфо**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) .</span><span class="sxs-lookup"><span data-stu-id="f1108-105">The **CopyRepairInfo** function creates a copy of a [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1108-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1108-106">Syntax</span></span>


```C++
HRESULT CopyRepairInfo(
  _Out_       RepairInfo *Dest,
  _In_  const RepairInfo *Source
);
```



## <a name="parameters"></a><span data-ttu-id="f1108-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1108-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1108-108">*Конечный адрес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f1108-108">*Dest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1108-109">Тип: \**[**репаиринфо**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="f1108-109">Type: \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\** _</span></span>

<span data-ttu-id="f1108-110">Обновляемая структура.</span><span class="sxs-lookup"><span data-stu-id="f1108-110">The structure to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="f1108-111">_Source \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="f1108-111">_Source\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1108-112">Тип: \**const [**репаиринфо**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="f1108-112">Type: \**const [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\** _</span></span>

<span data-ttu-id="f1108-113">Существующая копируемая структура.</span><span class="sxs-lookup"><span data-stu-id="f1108-113">The existing structure to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1108-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f1108-114">Return value</span></span>

<span data-ttu-id="f1108-115">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f1108-115">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f1108-116">Возможные возвращаемые значения включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="f1108-116">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="f1108-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f1108-117">Return code</span></span>                                                                                   | <span data-ttu-id="f1108-118">Описание</span><span class="sxs-lookup"><span data-stu-id="f1108-118">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f1108-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f1108-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f1108-120">Операция успешно выполнена.</span><span class="sxs-lookup"><span data-stu-id="f1108-120">The operation succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="f1108-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f1108-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f1108-122">Один или несколько параметров указаны неправильно.</span><span class="sxs-lookup"><span data-stu-id="f1108-122">One or more parameters has not been provided correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="f1108-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f1108-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f1108-124">Недостаточно памяти для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="f1108-124">There is not enough memory available to complete this operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f1108-125">Требования</span><span class="sxs-lookup"><span data-stu-id="f1108-125">Requirements</span></span>



| <span data-ttu-id="f1108-126">Требование</span><span class="sxs-lookup"><span data-stu-id="f1108-126">Requirement</span></span> | <span data-ttu-id="f1108-127">Значение</span><span class="sxs-lookup"><span data-stu-id="f1108-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1108-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1108-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f1108-129">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f1108-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f1108-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1108-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f1108-131">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f1108-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f1108-132">Header</span><span class="sxs-lookup"><span data-stu-id="f1108-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1108-133"><dt>Ндаттрибутилс. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1108-133"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1108-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1108-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1108-135">**репаиринфо**</span><span class="sxs-lookup"><span data-stu-id="f1108-135">**RepairInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> </dl>

 

 





