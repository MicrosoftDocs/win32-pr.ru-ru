---
title: Метод Исофткбд Енумсофткэйбоард (Софткбдк. h)
description: Метод Исофткбд Енумсофткэйбоард перечисляет возможные мягкие клавиатуры, поддерживающие указанный язык.
ms.assetid: c71f99e5-c4c2-4b09-a58f-d3f4348d0c5d
keywords:
- Платформа служб текстового ввода метода Енумсофткэйбоард
- Платформа текстовых служб метода Енумсофткэйбоард, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Енумсофткэйбоард
topic_type:
- apiref
api_name:
- ISoftKbd.EnumSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ecdb083684163798a68674628a8b1abc2460268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491892"
---
# <a name="isoftkbdenumsoftkeyboard-method"></a><span data-ttu-id="762e8-106">Метод Исофткбд:: Енумсофткэйбоард</span><span class="sxs-lookup"><span data-stu-id="762e8-106">ISoftKbd::EnumSoftKeyboard method</span></span>

<span data-ttu-id="762e8-107">Метод **исофткбд:: енумсофткэйбоард** перечисляет возможные мягкие клавиатуры, поддерживающие указанный язык.</span><span class="sxs-lookup"><span data-stu-id="762e8-107">The **ISoftKbd::EnumSoftKeyboard** method enumerates the possible soft keyboards that support the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="762e8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="762e8-108">Syntax</span></span>


```C++
HRESULT EnumSoftKeyboard(
  [in]  LANGID langid,
  [out] DWORD  *lpdwKeyboard
);
```



## <a name="parameters"></a><span data-ttu-id="762e8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="762e8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="762e8-110">*LangID* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="762e8-110">*langid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="762e8-111">Идентификатор языка.</span><span class="sxs-lookup"><span data-stu-id="762e8-111">Language identifier.</span></span>

</dd> <dt>

<span data-ttu-id="762e8-112">*лпдвкэйбоард* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="762e8-112">*lpdwKeyboard* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="762e8-113">Указатель на буфер, в котором этот метод получает идентификаторы доступных мягких клавиатур.</span><span class="sxs-lookup"><span data-stu-id="762e8-113">Pointer to a buffer in which this method retrieves identifiers of the available soft keyboards.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="762e8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="762e8-114">Return value</span></span>

<span data-ttu-id="762e8-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="762e8-115">This method can return one of these values.</span></span>



| <span data-ttu-id="762e8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="762e8-116">Value</span></span>                                                                                        | <span data-ttu-id="762e8-117">Описание</span><span class="sxs-lookup"><span data-stu-id="762e8-117">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="762e8-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="762e8-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="762e8-119">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="762e8-119">The method was successful.</span></span><br/>         |
| <dl> <span data-ttu-id="762e8-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="762e8-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="762e8-121">Недопустимый параметр *LangID* .</span><span class="sxs-lookup"><span data-stu-id="762e8-121">The *langid* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="762e8-122">Требования</span><span class="sxs-lookup"><span data-stu-id="762e8-122">Requirements</span></span>



| <span data-ttu-id="762e8-123">Требование</span><span class="sxs-lookup"><span data-stu-id="762e8-123">Requirement</span></span> | <span data-ttu-id="762e8-124">Значение</span><span class="sxs-lookup"><span data-stu-id="762e8-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="762e8-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="762e8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="762e8-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="762e8-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="762e8-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="762e8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="762e8-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="762e8-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="762e8-129">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="762e8-129">Redistributable</span></span><br/>          | <span data-ttu-id="762e8-130">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="762e8-130">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="762e8-131">Header</span><span class="sxs-lookup"><span data-stu-id="762e8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="762e8-132"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="762e8-132"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="762e8-133">IDL</span><span class="sxs-lookup"><span data-stu-id="762e8-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="762e8-134"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="762e8-134"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="762e8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="762e8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="762e8-136"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="762e8-136"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="762e8-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="762e8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="762e8-138">**исофткбд**</span><span class="sxs-lookup"><span data-stu-id="762e8-138">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





