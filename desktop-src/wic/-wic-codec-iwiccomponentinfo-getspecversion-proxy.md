---
description: Функция-посредник для метода Жетспекверсион.
ms.assetid: 363e55c2-d6e8-4ddc-a063-c5be08232a67
title: Функция IWICComponentInfo_GetSpecVersion_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetSpecVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7b9b0a44eb5fd8404eecc3ad355ec280583d690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713121"
---
# <a name="iwiccomponentinfo_getspecversion_proxy-function"></a><span data-ttu-id="39fa9-103">Ивиккомпонентинфо \_ жетспекверсион \_ -функция</span><span class="sxs-lookup"><span data-stu-id="39fa9-103">IWICComponentInfo\_GetSpecVersion\_Proxy function</span></span>

<span data-ttu-id="39fa9-104">Функция-посредник для метода [**жетспекверсион**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion) .</span><span class="sxs-lookup"><span data-stu-id="39fa9-104">Proxy function for the [**GetSpecVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="39fa9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39fa9-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetSpecVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchSpecVersion,
  _Inout_ WCHAR             *wzSpecVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="39fa9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="39fa9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39fa9-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="39fa9-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39fa9-108">Тип: \**[**ивиккомпонентинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="39fa9-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="39fa9-109">Указатель на этот объект [_ *ивиккомпонентинфо* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="39fa9-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="39fa9-110">*кчспекверсион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="39fa9-110">*cchSpecVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39fa9-111">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="39fa9-111">Type: **UINT**</span></span>

<span data-ttu-id="39fa9-112">Размер буфера *взспекверсион* .</span><span class="sxs-lookup"><span data-stu-id="39fa9-112">The size of the *wzSpecVersion* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="39fa9-113">*взспекверсион* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="39fa9-113">*wzSpecVersion* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="39fa9-114">Тип: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="39fa9-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="39fa9-115">При возврате из этого метода содержит язык и региональные параметры, инвариент строку версии спецификации компонента.</span><span class="sxs-lookup"><span data-stu-id="39fa9-115">When this method returns, contain a culture invarient string of the component's specification version.</span></span> <span data-ttu-id="39fa9-116">Формат версии — NN. NN. NN. NN.</span><span class="sxs-lookup"><span data-stu-id="39fa9-116">The version form is NN.NN.NN.NN.</span></span>

</dd> <dt>

<span data-ttu-id="39fa9-117">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="39fa9-117">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39fa9-118">Тип: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="39fa9-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="39fa9-119">Указатель, получающий фактическую длину версии спецификации компонента.</span><span class="sxs-lookup"><span data-stu-id="39fa9-119">A pointer that receives the actual length of the component's specification version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39fa9-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39fa9-120">Return value</span></span>

<span data-ttu-id="39fa9-121">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="39fa9-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="39fa9-122">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="39fa9-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="39fa9-123">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="39fa9-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="39fa9-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="39fa9-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="39fa9-125">Требования</span><span class="sxs-lookup"><span data-stu-id="39fa9-125">Requirements</span></span>



| <span data-ttu-id="39fa9-126">Требование</span><span class="sxs-lookup"><span data-stu-id="39fa9-126">Requirement</span></span> | <span data-ttu-id="39fa9-127">Значение</span><span class="sxs-lookup"><span data-stu-id="39fa9-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39fa9-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39fa9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="39fa9-129">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39fa9-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="39fa9-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39fa9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="39fa9-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="39fa9-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="39fa9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="39fa9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39fa9-133"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39fa9-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




