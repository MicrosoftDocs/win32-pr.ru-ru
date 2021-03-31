---
title: Функция Копируткаусеинфо (Ндаттрибутилс. h)
description: Создает копию структуры Руткаусеинфо.
ms.assetid: 6bcd1341-657a-40c1-bebd-1c0f780ae337
keywords:
- Копируткаусеинфо функция NDF
topic_type:
- apiref
api_name:
- CopyRootCauseInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5093d7af6458668a763aa206cacd22a0526aa521
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988437"
---
# <a name="copyrootcauseinfo-function"></a><span data-ttu-id="3e52c-104">Функция Копируткаусеинфо</span><span class="sxs-lookup"><span data-stu-id="3e52c-104">CopyRootCauseInfo function</span></span>

<span data-ttu-id="3e52c-105">Функция **копируткаусеинфо** создает копию структуры [**руткаусеинфо**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) .</span><span class="sxs-lookup"><span data-stu-id="3e52c-105">The **CopyRootCauseInfo** function creates a copy of a [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e52c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e52c-106">Syntax</span></span>


```C++
HRESULT CopyRootCauseInfo(
  _Out_       RootCauseInfo *Dest,
  _In_  const RootCauseInfo *Source
);
```



## <a name="parameters"></a><span data-ttu-id="3e52c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e52c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e52c-108">*Конечный адрес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3e52c-108">*Dest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e52c-109">Тип: \**[**руткаусеинфо**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="3e52c-109">Type: \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\** _</span></span>

<span data-ttu-id="3e52c-110">Обновляемая структура.</span><span class="sxs-lookup"><span data-stu-id="3e52c-110">The structure to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="3e52c-111">_Source \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="3e52c-111">_Source\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e52c-112">Тип: \**const [**руткаусеинфо**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="3e52c-112">Type: \**const [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\** _</span></span>

<span data-ttu-id="3e52c-113">Существующая копируемая структура.</span><span class="sxs-lookup"><span data-stu-id="3e52c-113">The existing structure to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e52c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e52c-114">Return value</span></span>

<span data-ttu-id="3e52c-115">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="3e52c-115">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="3e52c-116">Возможные возвращаемые значения включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="3e52c-116">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="3e52c-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3e52c-117">Return code</span></span>                                                                                   | <span data-ttu-id="3e52c-118">Описание</span><span class="sxs-lookup"><span data-stu-id="3e52c-118">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3e52c-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3e52c-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3e52c-120">Операция успешно выполнена.</span><span class="sxs-lookup"><span data-stu-id="3e52c-120">The operation succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="3e52c-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3e52c-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3e52c-122">Один или несколько параметров указаны неправильно.</span><span class="sxs-lookup"><span data-stu-id="3e52c-122">One or more parameters has not been provided correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="3e52c-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3e52c-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3e52c-124">Недостаточно памяти для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="3e52c-124">There is not enough memory available to complete this operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3e52c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="3e52c-125">Requirements</span></span>



| <span data-ttu-id="3e52c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="3e52c-126">Requirement</span></span> | <span data-ttu-id="3e52c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="3e52c-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e52c-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e52c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3e52c-129">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3e52c-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3e52c-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e52c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3e52c-131">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3e52c-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3e52c-132">Header</span><span class="sxs-lookup"><span data-stu-id="3e52c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e52c-133"><dt>Ндаттрибутилс. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e52c-133"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e52c-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e52c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e52c-135">**руткаусеинфо**</span><span class="sxs-lookup"><span data-stu-id="3e52c-135">**RootCauseInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> </dl>

 

 





