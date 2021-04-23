---
description: Возвращает значение указанных дочерних свойств в элементе <Properties> элемент профиля сканирования.
ms.assetid: 528b51f5-51e0-4639-965d-ee318eb2187b
title: Метод Исканпрофиле::-Property (Сканпрофиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 48137e61d88d580ac556220b4e47b949d9e2c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719380"
---
# <a name="iscanprofilegetproperty-method"></a><span data-ttu-id="2da2c-104">Исканпрофиле:: метод Property</span><span class="sxs-lookup"><span data-stu-id="2da2c-104">IScanProfile::GetProperty method</span></span>

<span data-ttu-id="2da2c-105">Возвращает значение указанных дочерних свойств в `<Properties>` элементе профиля сканирования.</span><span class="sxs-lookup"><span data-stu-id="2da2c-105">Gets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="2da2c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2da2c-106">Syntax</span></span>


```C++
HRESULT GetProperty(
  [in]  ULONG       num,
  [in]  PROPID      *pid,
  [out] PROPVARIANT *pvar
);
```



## <a name="parameters"></a><span data-ttu-id="2da2c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2da2c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2da2c-108">*число* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2da2c-108">*num* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2da2c-109">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="2da2c-109">Type: **ULONG**</span></span>

<span data-ttu-id="2da2c-110">Количество записей в массивах, на которые указывает *PID* и *ПВАР*.</span><span class="sxs-lookup"><span data-stu-id="2da2c-110">The number of entries in the arrays that are pointed to by *pid* and *pvar*.</span></span>

</dd> <dt>

<span data-ttu-id="2da2c-111">*идентификатор процесса* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2da2c-111">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2da2c-112">Тип: \**PropID \** _</span><span class="sxs-lookup"><span data-stu-id="2da2c-112">Type: \**PROPID\** _</span></span>

<span data-ttu-id="2da2c-113">Указатель на массив идентификационных номеров заданных свойств.</span><span class="sxs-lookup"><span data-stu-id="2da2c-113">A pointer to an array of the identification numbers of the properties to be set.</span></span> <span data-ttu-id="2da2c-114">Каждое значение в массиве является [константами свойства WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2da2c-114">Each value in the array is a [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="2da2c-115">_pvar \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2da2c-115">_pvar\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2da2c-116">Тип: \**[пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="2da2c-116">Type: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="2da2c-117">Указатель на массив значений.</span><span class="sxs-lookup"><span data-stu-id="2da2c-117">A pointer to an array of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2da2c-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2da2c-118">Return value</span></span>

<span data-ttu-id="2da2c-119">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="2da2c-119">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="2da2c-120">Возвращает \_ значение false, если какое-либо из значений свойств недоступно; в противном случае возвращает s \_ OK или стандартный код ошибки COM.</span><span class="sxs-lookup"><span data-stu-id="2da2c-120">Returns S\_FALSE if any of the property values is not available; otherwise, returns S\_OK or a standard COM error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2da2c-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2da2c-121">Remarks</span></span>

<span data-ttu-id="2da2c-122">Тип каждого значения должен быть того же типа, который был задан при вызове [**исканпрофиле:: SetProperty**](-wia-iscanprofile-setproperty.md).</span><span class="sxs-lookup"><span data-stu-id="2da2c-122">The type of each value must be the same type that was set with the call to [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).</span></span>

<span data-ttu-id="2da2c-123">Каждое значение в массиве, на которое указывает *PID* , является одной из [констант свойства WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2da2c-123">Each value in the array that *pid* points to is one of the [WIA Property Constants](-wia-wia-property-constants.md).</span></span> <span data-ttu-id="2da2c-124">Эту систему идентификации можно расширить.</span><span class="sxs-lookup"><span data-stu-id="2da2c-124">You can extend this identification system.</span></span> <span data-ttu-id="2da2c-125">См. раздел [Определение пользовательских свойств](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="2da2c-125">See [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2da2c-126">Требования</span><span class="sxs-lookup"><span data-stu-id="2da2c-126">Requirements</span></span>



| <span data-ttu-id="2da2c-127">Требование</span><span class="sxs-lookup"><span data-stu-id="2da2c-127">Requirement</span></span> | <span data-ttu-id="2da2c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="2da2c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2da2c-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2da2c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2da2c-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2da2c-130">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="2da2c-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2da2c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2da2c-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2da2c-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2da2c-133">Header</span><span class="sxs-lookup"><span data-stu-id="2da2c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2da2c-134"><dt>Сканпрофиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="2da2c-134"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="2da2c-135">IDL</span><span class="sxs-lookup"><span data-stu-id="2da2c-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2da2c-136"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2da2c-136"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2da2c-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2da2c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2da2c-138">**исканпрофиле**</span><span class="sxs-lookup"><span data-stu-id="2da2c-138">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

<span data-ttu-id="2da2c-139">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="2da2c-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2da2c-140">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="2da2c-140">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> <dt>

[<span data-ttu-id="2da2c-141">Константы свойств WIA</span><span class="sxs-lookup"><span data-stu-id="2da2c-141">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="2da2c-142">Определение пользовательских свойств</span><span class="sxs-lookup"><span data-stu-id="2da2c-142">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
