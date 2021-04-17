---
title: Метод Исофткбд Шовкэйсфоркэйсканмоде (Софткбдк. h)
description: Метод Исофткбд Шовкэйсфоркэйсканмоде отображает ключи, используемые для режима просмотра ключа для экранной клавиатуры.
ms.assetid: bfa76e5b-6f6e-470a-ba3a-7ecff9f67f7b
keywords:
- Платформа служб текстового ввода метода Шовкэйсфоркэйсканмоде
- Платформа текстовых служб метода Шовкэйсфоркэйсканмоде, интерфейс Исофткбд
- Платформа текстовых служб интерфейса Исофткбд, метод Шовкэйсфоркэйсканмоде
topic_type:
- apiref
api_name:
- ISoftKbd.ShowKeysForKeyScanMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c46fbfc103c0ba40294e4c149d5fd427296765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492096"
---
# <a name="isoftkbdshowkeysforkeyscanmode-method"></a><span data-ttu-id="28751-106">Метод Исофткбд:: Шовкэйсфоркэйсканмоде</span><span class="sxs-lookup"><span data-stu-id="28751-106">ISoftKbd::ShowKeysForKeyScanMode method</span></span>

<span data-ttu-id="28751-107">Метод **исофткбд:: шовкэйсфоркэйсканмоде** отображает ключи, используемые для режима просмотра ключа для экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="28751-107">The **ISoftKbd::ShowKeysForKeyScanMode** method displays the keys used for the key scan mode for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="28751-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28751-108">Syntax</span></span>


```C++
HRESULT ShowKeysForKeyScanMode(
  [in] KEYID *lpKeyID,
  [in] INT   iKeyNum,
  [in] BOOL  fHighL
);
```



## <a name="parameters"></a><span data-ttu-id="28751-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="28751-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28751-110">*лпкэйид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="28751-110">*lpKeyID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28751-111">Указатель на массив элементов KEYID, указывающий идентификаторы ключей для вывода.</span><span class="sxs-lookup"><span data-stu-id="28751-111">Pointer to an array of KEYID elements indicating the identifiers of keys to display.</span></span>

</dd> <dt>

<span data-ttu-id="28751-112">*икэйнум* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="28751-112">*iKeyNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28751-113">Число отображаемых ключей.</span><span class="sxs-lookup"><span data-stu-id="28751-113">The number of keys to display.</span></span>

</dd> <dt>

<span data-ttu-id="28751-114">*фхигхл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="28751-114">*fHighL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28751-115">Значение TRUE, если метод должен выделять ключи, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="28751-115">TRUE if the method is to highlight the keys, and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28751-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28751-116">Return value</span></span>

<span data-ttu-id="28751-117">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="28751-117">This method can return one of these values.</span></span>



| <span data-ttu-id="28751-118">Значение</span><span class="sxs-lookup"><span data-stu-id="28751-118">Value</span></span>                                                                                        | <span data-ttu-id="28751-119">Описание</span><span class="sxs-lookup"><span data-stu-id="28751-119">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="28751-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="28751-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="28751-121">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="28751-121">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="28751-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="28751-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="28751-123">Один из параметров недопустим.</span><span class="sxs-lookup"><span data-stu-id="28751-123">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="28751-124">Требования</span><span class="sxs-lookup"><span data-stu-id="28751-124">Requirements</span></span>



| <span data-ttu-id="28751-125">Требование</span><span class="sxs-lookup"><span data-stu-id="28751-125">Requirement</span></span> | <span data-ttu-id="28751-126">Значение</span><span class="sxs-lookup"><span data-stu-id="28751-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28751-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28751-127">Minimum supported client</span></span><br/> | <span data-ttu-id="28751-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="28751-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="28751-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28751-129">Minimum supported server</span></span><br/> | <span data-ttu-id="28751-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="28751-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="28751-131">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="28751-131">Redistributable</span></span><br/>          | <span data-ttu-id="28751-132">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="28751-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="28751-133">Header</span><span class="sxs-lookup"><span data-stu-id="28751-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="28751-134"><dt>Софткбдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="28751-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="28751-135">IDL</span><span class="sxs-lookup"><span data-stu-id="28751-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="28751-136"><dt>Софткбд. idl</dt></span><span class="sxs-lookup"><span data-stu-id="28751-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="28751-137">DLL</span><span class="sxs-lookup"><span data-stu-id="28751-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28751-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28751-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28751-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28751-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28751-140">**исофткбд**</span><span class="sxs-lookup"><span data-stu-id="28751-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





