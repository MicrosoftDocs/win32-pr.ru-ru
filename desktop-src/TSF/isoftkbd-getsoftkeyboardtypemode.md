---
title: Метод Исофткбд Жетсофткэйбоардтипемоде (Софткбдк. h)
description: Метод Исофткбд Жетсофткэйбоардтипемоде извлекает режим типа для экранной клавиатуры.
ms.assetid: 77294652-b82e-4b69-bb55-5ebebc3c97c7
keywords:
- Платформа служб текстового ввода метода Жетсофткэйбоардтипемоде
- Платформа текстовых служб метода Жетсофткэйбоардтипемоде, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Жетсофткэйбоардтипемоде
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6aad6d60c50ee0050cf418018dd6db1c7a33efc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414700"
---
# <a name="isoftkbdgetsoftkeyboardtypemode-method"></a><span data-ttu-id="80316-106">Метод Исофткбд:: Жетсофткэйбоардтипемоде</span><span class="sxs-lookup"><span data-stu-id="80316-106">ISoftKbd::GetSoftKeyboardTypeMode method</span></span>

<span data-ttu-id="80316-107">Метод **исофткбд:: жетсофткэйбоардтипемоде** получает режим типа для экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="80316-107">The **ISoftKbd::GetSoftKeyboardTypeMode** method retrieves the type mode for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="80316-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80316-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardTypeMode(
  [out] TYPEMODE *lpTypeMode
);
```



## <a name="parameters"></a><span data-ttu-id="80316-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="80316-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80316-110">*лптипемоде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="80316-110">*lpTypeMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80316-111">Указатель на буфер, в котором этот метод извлекает режим типа.</span><span class="sxs-lookup"><span data-stu-id="80316-111">Pointer to a buffer in which this method retrieves the type mode.</span></span> <span data-ttu-id="80316-112">Для перечисления [**типемоде**](typemode.md) определены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="80316-112">Possible values are defined for the [**TYPEMODE**](typemode.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80316-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80316-113">Return value</span></span>

<span data-ttu-id="80316-114">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="80316-114">This method can return one of these values.</span></span>



| <span data-ttu-id="80316-115">Значение</span><span class="sxs-lookup"><span data-stu-id="80316-115">Value</span></span>                                                                                        | <span data-ttu-id="80316-116">Описание</span><span class="sxs-lookup"><span data-stu-id="80316-116">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="80316-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="80316-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="80316-118">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="80316-118">The method was successful.</span></span><br/>             |
| <dl> <span data-ttu-id="80316-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="80316-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="80316-120">Недопустимый параметр *лптипемоде* .</span><span class="sxs-lookup"><span data-stu-id="80316-120">The *lpTypeMode* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="80316-121">Требования</span><span class="sxs-lookup"><span data-stu-id="80316-121">Requirements</span></span>



| <span data-ttu-id="80316-122">Требование</span><span class="sxs-lookup"><span data-stu-id="80316-122">Requirement</span></span> | <span data-ttu-id="80316-123">Значение</span><span class="sxs-lookup"><span data-stu-id="80316-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80316-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80316-124">Minimum supported client</span></span><br/> | <span data-ttu-id="80316-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="80316-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="80316-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80316-126">Minimum supported server</span></span><br/> | <span data-ttu-id="80316-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="80316-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="80316-128">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="80316-128">Redistributable</span></span><br/>          | <span data-ttu-id="80316-129">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="80316-129">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="80316-130">Header</span><span class="sxs-lookup"><span data-stu-id="80316-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="80316-131"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="80316-131"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="80316-132">IDL</span><span class="sxs-lookup"><span data-stu-id="80316-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="80316-133"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="80316-133"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="80316-134">DLL</span><span class="sxs-lookup"><span data-stu-id="80316-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80316-135"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80316-135"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80316-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80316-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80316-137">**исофткбд**</span><span class="sxs-lookup"><span data-stu-id="80316-137">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="80316-138">**Исофткбд:: Сетсофткэйбоардтипемоде**</span><span class="sxs-lookup"><span data-stu-id="80316-138">**ISoftKbd::SetSoftKeyboardTypeMode**</span></span>](isoftkbd-setsoftkeyboardtypemode.md)
</dt> <dt>

[<span data-ttu-id="80316-139">**типемоде**</span><span class="sxs-lookup"><span data-stu-id="80316-139">**TYPEMODE**</span></span>](typemode.md)
</dt> </dl>

 

 





