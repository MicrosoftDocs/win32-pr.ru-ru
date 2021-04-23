---
title: Функция Копихелператтрибуте (Ндаттрибутилс. h)
description: Создает копию структуры ВСПОМОГАТЕЛЬного \_ атрибута.
ms.assetid: ff49be29-4cd8-4730-929f-c66a7325704f
keywords:
- Копихелператтрибуте функция NDF
topic_type:
- apiref
api_name:
- CopyHelperAttribute
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59fac3449ee48659980681c836d24406c4db7e2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672601"
---
# <a name="copyhelperattribute-function"></a><span data-ttu-id="6021b-104">Функция Копихелператтрибуте</span><span class="sxs-lookup"><span data-stu-id="6021b-104">CopyHelperAttribute function</span></span>

<span data-ttu-id="6021b-105">Функция **копихелператтрибуте** создает копию структуры [**вспомогательного \_ атрибута**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) .</span><span class="sxs-lookup"><span data-stu-id="6021b-105">The **CopyHelperAttribute** function creates a copy of a [**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6021b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6021b-106">Syntax</span></span>


```C++
HRESULT CopyHelperAttribute(
  _Out_       HELPER_ATTRIBUTE *Dest,
  _In_  const HELPER_ATTRIBUTE *Source
);
```



## <a name="parameters"></a><span data-ttu-id="6021b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6021b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6021b-108">*Конечный адрес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6021b-108">*Dest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6021b-109">Тип: \**[**вспомогательный \_ атрибут**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) \** _</span><span class="sxs-lookup"><span data-stu-id="6021b-109">Type: \**[**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\** _</span></span>

<span data-ttu-id="6021b-110">Обновляемая структура.</span><span class="sxs-lookup"><span data-stu-id="6021b-110">The structure to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="6021b-111">_Source \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="6021b-111">_Source\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6021b-112">Тип: \**\* const [**\_ атрибут вспомогательной**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)* функции _</span><span class="sxs-lookup"><span data-stu-id="6021b-112">Type: \**const [**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\** _</span></span>

<span data-ttu-id="6021b-113">Существующая копируемая структура.</span><span class="sxs-lookup"><span data-stu-id="6021b-113">The existing structure to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6021b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6021b-114">Return value</span></span>

<span data-ttu-id="6021b-115">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="6021b-115">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="6021b-116">Возможные возвращаемые значения включают, но не ограничиваются следующим.</span><span class="sxs-lookup"><span data-stu-id="6021b-116">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="6021b-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6021b-117">Return code</span></span>                                                                                   | <span data-ttu-id="6021b-118">Описание</span><span class="sxs-lookup"><span data-stu-id="6021b-118">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6021b-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="6021b-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6021b-120">Операция успешно выполнена.</span><span class="sxs-lookup"><span data-stu-id="6021b-120">The operation succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="6021b-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6021b-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6021b-122">Один или несколько параметров указаны неправильно.</span><span class="sxs-lookup"><span data-stu-id="6021b-122">One or more parameters has not been provided correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="6021b-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6021b-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6021b-124">Недостаточно памяти для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="6021b-124">There is not enough memory available to complete this operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6021b-125">Требования</span><span class="sxs-lookup"><span data-stu-id="6021b-125">Requirements</span></span>



| <span data-ttu-id="6021b-126">Требование</span><span class="sxs-lookup"><span data-stu-id="6021b-126">Requirement</span></span> | <span data-ttu-id="6021b-127">Значение</span><span class="sxs-lookup"><span data-stu-id="6021b-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6021b-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6021b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6021b-129">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6021b-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6021b-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6021b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6021b-131">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6021b-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6021b-132">Header</span><span class="sxs-lookup"><span data-stu-id="6021b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6021b-133"><dt>Ндаттрибутилс. h</dt></span><span class="sxs-lookup"><span data-stu-id="6021b-133"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6021b-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6021b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6021b-135">**ВСПОМОГАТЕЛЬный \_ атрибут**</span><span class="sxs-lookup"><span data-stu-id="6021b-135">**HELPER\_ATTRIBUTE**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> </dl>

 

 





