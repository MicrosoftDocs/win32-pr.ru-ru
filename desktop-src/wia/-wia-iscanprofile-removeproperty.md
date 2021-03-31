---
description: Удаляет указанный список дочерних свойств в элементе <Properties> элемент профиля сканирования.
ms.assetid: 512ccfec-0c95-4abb-98b6-d309e432151b
title: 'Метод Исканпрофиле:: RemoveProperty (Сканпрофиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.RemoveProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 1ac1d713ab36da5c35ea7a0d7c523699e7c85b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154871"
---
# <a name="iscanprofileremoveproperty-method"></a><span data-ttu-id="94934-104">Метод Исканпрофиле:: RemoveProperty</span><span class="sxs-lookup"><span data-stu-id="94934-104">IScanProfile::RemoveProperty method</span></span>

<span data-ttu-id="94934-105">Удаляет указанный список дочерних свойств `<Properties>` элемента профиля сканирования.</span><span class="sxs-lookup"><span data-stu-id="94934-105">Removes a specified list of child properties in the `<Properties>` element of a scan profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="94934-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94934-106">Syntax</span></span>


```C++
HRESULT RemoveProperty(
  [in] ULONG  num,
  [in] PROPID *pid
);
```



## <a name="parameters"></a><span data-ttu-id="94934-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="94934-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94934-108">*число* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94934-108">*num* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94934-109">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="94934-109">Type: **ULONG**</span></span>

<span data-ttu-id="94934-110">Количество записей в массиве, на которое указывает *PID* .</span><span class="sxs-lookup"><span data-stu-id="94934-110">The number of entries in the array that *pid* points to.</span></span>

</dd> <dt>

<span data-ttu-id="94934-111">*идентификатор процесса* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94934-111">*pid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94934-112">Тип: \**PropID \** _</span><span class="sxs-lookup"><span data-stu-id="94934-112">Type: \**PROPID\** _</span></span>

<span data-ttu-id="94934-113">Указатель на массив идентификационных номеров удаляемых свойств.</span><span class="sxs-lookup"><span data-stu-id="94934-113">A pointer to an array of identification numbers of the properties to be deleted.</span></span> <span data-ttu-id="94934-114">Каждая из них является [константами свойства WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="94934-114">Each is a [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94934-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94934-115">Return value</span></span>

<span data-ttu-id="94934-116">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="94934-116">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="94934-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="94934-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="94934-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="94934-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="94934-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94934-119">Remarks</span></span>

<span data-ttu-id="94934-120">Каждое значение в массиве, на которое указывает *PID* , является одной из [констант свойства WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="94934-120">Each value in the array that *pid* points to is one of the [WIA Property Constants](-wia-wia-property-constants.md).</span></span> <span data-ttu-id="94934-121">Эту систему идентификации можно расширить.</span><span class="sxs-lookup"><span data-stu-id="94934-121">You can extend this identification system.</span></span> <span data-ttu-id="94934-122">См. раздел [Определение пользовательских свойств](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="94934-122">See [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

<span data-ttu-id="94934-123">Изменения в профиле не сохраняются на диск, пока приложение не вызовет метод [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) .</span><span class="sxs-lookup"><span data-stu-id="94934-123">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="94934-124">Если два приложения создают объекты профиля сканирования из одного и того же XML-файла и каждое приложение записывает изменения в свой объект, только изменения, внесенные приложением, которое вызывает [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) Last, сохраняются на диске.</span><span class="sxs-lookup"><span data-stu-id="94934-124">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="94934-125">Требования</span><span class="sxs-lookup"><span data-stu-id="94934-125">Requirements</span></span>



| <span data-ttu-id="94934-126">Требование</span><span class="sxs-lookup"><span data-stu-id="94934-126">Requirement</span></span> | <span data-ttu-id="94934-127">Значение</span><span class="sxs-lookup"><span data-stu-id="94934-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="94934-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94934-128">Minimum supported client</span></span><br/> | <span data-ttu-id="94934-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="94934-129">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="94934-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94934-130">Minimum supported server</span></span><br/> | <span data-ttu-id="94934-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="94934-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="94934-132">Header</span><span class="sxs-lookup"><span data-stu-id="94934-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="94934-133"><dt>Сканпрофиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="94934-133"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="94934-134">IDL</span><span class="sxs-lookup"><span data-stu-id="94934-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="94934-135"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="94934-135"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94934-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94934-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94934-137">**исканпрофиле**</span><span class="sxs-lookup"><span data-stu-id="94934-137">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

<span data-ttu-id="94934-138">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="94934-138">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="94934-139">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="94934-139">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> <dt>

[<span data-ttu-id="94934-140">Константы свойств WIA</span><span class="sxs-lookup"><span data-stu-id="94934-140">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="94934-141">Определение пользовательских свойств</span><span class="sxs-lookup"><span data-stu-id="94934-141">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 




