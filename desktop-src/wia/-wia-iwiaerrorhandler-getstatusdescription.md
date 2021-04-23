---
description: Возвращает строку, описывающую код состояния.
ms.assetid: d3007f3e-46e1-4ab6-8ce3-c4e38f87ce61
title: 'Метод Ивиаеррорхандлер:: Жетстатусдескриптион (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.GetStatusDescription
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: da23e413ee238f43ae577a51b18a542dc1b0768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692522"
---
# <a name="iwiaerrorhandlergetstatusdescription-method"></a><span data-ttu-id="747ae-103">Метод Ивиаеррорхандлер:: Жетстатусдескриптион</span><span class="sxs-lookup"><span data-stu-id="747ae-103">IWiaErrorHandler::GetStatusDescription method</span></span>

<span data-ttu-id="747ae-104">Возвращает строку, описывающую код состояния.</span><span class="sxs-lookup"><span data-stu-id="747ae-104">Returns a string that describes the status code.</span></span>

## <a name="syntax"></a><span data-ttu-id="747ae-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="747ae-105">Syntax</span></span>


```C++
HRESULT GetStatusDescription(
  [in]  IUnknown *punkItem,
  [in]  HRESULT  hrStatus,
  [in]  LONG     cbResLength,
  [in]  BYTE     *pbData,
  [out] BSTR     *pbstrDescription
);
```



## <a name="parameters"></a><span data-ttu-id="747ae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="747ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="747ae-107">*пункитем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="747ae-107">*punkItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="747ae-108">Тип: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="747ae-108">Type: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="747ae-109">Указатель на [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) передаваемого элемента.</span><span class="sxs-lookup"><span data-stu-id="747ae-109">Pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) of the item being transferred.</span></span> <span data-ttu-id="747ae-110">Этот объект минимальное реализует [_ *IWiaItem2* \*](-wia-iwiaitem2.md) и [**ивиадататрансфер**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span><span class="sxs-lookup"><span data-stu-id="747ae-110">This object minimally implements [_ *IWiaItem2*\*](-wia-iwiaitem2.md) and [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span></span>

</dd> <dt>

<span data-ttu-id="747ae-111">*хрстатус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="747ae-111">*hrStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="747ae-112">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="747ae-112">Type: **HRESULT**</span></span>

<span data-ttu-id="747ae-113">**Значение HRESULT** , которое является кодом состояния, полученным [**бандеддатакаллбакк**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="747ae-113">**HRESULT** that is the status code received by [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> <dt>

<span data-ttu-id="747ae-114">*кбресленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="747ae-114">*cbResLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="747ae-115">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="747ae-115">Type: **LONG**</span></span>

<span data-ttu-id="747ae-116">Значение **типа Long** , равное размеру данных, на которые ссылается *pbData*.</span><span class="sxs-lookup"><span data-stu-id="747ae-116">**LONG** that is the size of the data referred to by *pbData*.</span></span>

</dd> <dt>

<span data-ttu-id="747ae-117">*pbData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="747ae-117">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="747ae-118">Тип: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="747ae-118">Type: \**BYTE\** _</span></span>

<span data-ttu-id="747ae-119">Указатель на буфер данных, полученный с помощью [_ *бандеддатакаллбакк* \*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="747ae-119">Pointer to the data buffer as received by [_ *BandedDataCallback*\*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> <dt>

<span data-ttu-id="747ae-120">*пбстрдескриптион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="747ae-120">*pbstrDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="747ae-121">Тип: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="747ae-121">Type: \**BSTR\** _</span></span>

<span data-ttu-id="747ae-122">_ \*BSTR\*\*, которая получает описание состояния или ошибки, возникшей во время передачи данных.</span><span class="sxs-lookup"><span data-stu-id="747ae-122">_ *BSTR*\* that receives a description of the status or error encountered during the data transfer.</span></span> <span data-ttu-id="747ae-123">Этот параметр не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="747ae-123">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="747ae-124">Вызывающий объект должен освободить строку с помощью [сисфристринг](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring), и разработчик должен выделить строку с помощью [сисаллокстринг](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).</span><span class="sxs-lookup"><span data-stu-id="747ae-124">The caller must free the string using [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring), and the implementor must allocate the string using [SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="747ae-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="747ae-125">Return value</span></span>

<span data-ttu-id="747ae-126">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="747ae-126">Type: **HRESULT**</span></span>

<span data-ttu-id="747ae-127">Возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="747ae-127">Returns one of the following values.</span></span>



| <span data-ttu-id="747ae-128">Код возврата</span><span class="sxs-lookup"><span data-stu-id="747ae-128">Return code</span></span>                                                                             | <span data-ttu-id="747ae-129">Описание</span><span class="sxs-lookup"><span data-stu-id="747ae-129">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="747ae-130"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="747ae-130"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="747ae-131">*пбстрдескриптион* содержит допустимый указатель **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="747ae-131">*pbstrDescription* contains a valid **BSTR** pointer.</span></span> <br/>  |
| <dl> <span data-ttu-id="747ae-132"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="747ae-132"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="747ae-133">*хрстатус* неизвестен, и описание недоступно.</span><span class="sxs-lookup"><span data-stu-id="747ae-133">*hrStatus* is unknown and no description is available.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="747ae-134">Требования</span><span class="sxs-lookup"><span data-stu-id="747ae-134">Requirements</span></span>



| <span data-ttu-id="747ae-135">Требование</span><span class="sxs-lookup"><span data-stu-id="747ae-135">Requirement</span></span> | <span data-ttu-id="747ae-136">Значение</span><span class="sxs-lookup"><span data-stu-id="747ae-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="747ae-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="747ae-137">Minimum supported client</span></span><br/> | <span data-ttu-id="747ae-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="747ae-138">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="747ae-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="747ae-139">Minimum supported server</span></span><br/> | <span data-ttu-id="747ae-140">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="747ae-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="747ae-141">Header</span><span class="sxs-lookup"><span data-stu-id="747ae-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="747ae-142"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="747ae-142"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="747ae-143">IDL</span><span class="sxs-lookup"><span data-stu-id="747ae-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="747ae-144"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="747ae-144"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="747ae-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="747ae-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="747ae-146"><dt>Виагуид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="747ae-146"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
