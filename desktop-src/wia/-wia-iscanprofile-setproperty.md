---
description: Задает значение указанных дочерних свойств в элементе <Properties> элемент профиля сканирования.
ms.assetid: 3cf7b723-4004-49e5-b3bd-49a84432ede3
title: 'Метод Исканпрофиле:: SetProperty (Сканпрофиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: f8f21891ae0cc5fa8e64fafd4acb9e61334a7279
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810792"
---
# <a name="iscanprofilesetproperty-method"></a><span data-ttu-id="efdef-104">Метод Исканпрофиле:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="efdef-104">IScanProfile::SetProperty method</span></span>

<span data-ttu-id="efdef-105">Задает значение указанных дочерних свойств в `<Properties>` элементе профиля сканирования.</span><span class="sxs-lookup"><span data-stu-id="efdef-105">Sets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="efdef-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="efdef-106">Syntax</span></span>


```C++
HRESULT SetProperty(
  [in] ULONG       num,
  [in] PROPID      *pid,
  [in] PROPVARIANT *pvar
);
```



## <a name="parameters"></a><span data-ttu-id="efdef-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="efdef-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efdef-108">*число* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="efdef-108">*num* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efdef-109">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="efdef-109">Type: **ULONG**</span></span>

<span data-ttu-id="efdef-110">Количество записей в массивах, на которые указывает *PID* и *ПВАР*.</span><span class="sxs-lookup"><span data-stu-id="efdef-110">The number of entries in the arrays that are pointed to by *pid* and *pvar*.</span></span>

</dd> <dt>

<span data-ttu-id="efdef-111">*идентификатор процесса* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="efdef-111">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efdef-112">Тип: \**PropID \** _</span><span class="sxs-lookup"><span data-stu-id="efdef-112">Type: \**PROPID\** _</span></span>

<span data-ttu-id="efdef-113">Указатель на массив идентификационных номеров заданных свойств.</span><span class="sxs-lookup"><span data-stu-id="efdef-113">A pointer to an array of identification numbers of the properties to be set.</span></span> <span data-ttu-id="efdef-114">Каждое значение в массиве является [константами свойства WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="efdef-114">Each value in the array is a [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="efdef-115">_pvar \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="efdef-115">_pvar\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efdef-116">Тип: \**[пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="efdef-116">Type: \**[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="efdef-117">Указатель на массив значений, присваиваемый свойствам.</span><span class="sxs-lookup"><span data-stu-id="efdef-117">A pointer to an array of values to be assigned to the properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efdef-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="efdef-118">Return value</span></span>

<span data-ttu-id="efdef-119">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="efdef-119">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="efdef-120">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="efdef-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="efdef-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="efdef-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="efdef-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="efdef-122">Remarks</span></span>

<span data-ttu-id="efdef-123">Каждое значение в массиве, на которое указывает *PID* , является одной из [констант свойства WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="efdef-123">Each value in the array that *pid* points to is one of the [WIA Property Constants](-wia-wia-property-constants.md).</span></span> <span data-ttu-id="efdef-124">Эту систему идентификации можно расширить.</span><span class="sxs-lookup"><span data-stu-id="efdef-124">You can extend this identification system.</span></span> <span data-ttu-id="efdef-125">См. раздел [Определение пользовательских свойств](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="efdef-125">See [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

<span data-ttu-id="efdef-126">Изменения в профиле не сохраняются на диск, пока приложение не вызовет метод [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) .</span><span class="sxs-lookup"><span data-stu-id="efdef-126">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="efdef-127">Если два приложения создают объекты профиля сканирования из одного и того же XML-файла и каждое приложение записывает изменения в свой объект, только изменения, внесенные приложением, которое вызывает [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) Last, сохраняются на диске.</span><span class="sxs-lookup"><span data-stu-id="efdef-127">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="efdef-128">Требования</span><span class="sxs-lookup"><span data-stu-id="efdef-128">Requirements</span></span>



| <span data-ttu-id="efdef-129">Требование</span><span class="sxs-lookup"><span data-stu-id="efdef-129">Requirement</span></span> | <span data-ttu-id="efdef-130">Значение</span><span class="sxs-lookup"><span data-stu-id="efdef-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="efdef-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="efdef-131">Minimum supported client</span></span><br/> | <span data-ttu-id="efdef-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="efdef-132">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="efdef-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="efdef-133">Minimum supported server</span></span><br/> | <span data-ttu-id="efdef-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="efdef-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="efdef-135">Header</span><span class="sxs-lookup"><span data-stu-id="efdef-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="efdef-136"><dt>Сканпрофиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="efdef-136"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="efdef-137">IDL</span><span class="sxs-lookup"><span data-stu-id="efdef-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="efdef-138"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="efdef-138"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efdef-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="efdef-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efdef-140">**исканпрофиле**</span><span class="sxs-lookup"><span data-stu-id="efdef-140">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

<span data-ttu-id="efdef-141">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="efdef-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="efdef-142">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="efdef-142">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> <dt>

[<span data-ttu-id="efdef-143">Константы свойств WIA</span><span class="sxs-lookup"><span data-stu-id="efdef-143">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="efdef-144">Определение пользовательских свойств</span><span class="sxs-lookup"><span data-stu-id="efdef-144">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 
