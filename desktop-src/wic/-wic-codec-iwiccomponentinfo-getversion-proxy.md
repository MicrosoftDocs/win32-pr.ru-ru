---
description: Функция-посредник для метода WebMethod.
ms.assetid: b064b065-bc02-4943-b208-ce5e40c12aa2
title: Функция IWICComponentInfo_GetVersion_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: bad3677068802861bce9c0c7d0c1b03e5d06d0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713120"
---
# <a name="iwiccomponentinfo_getversion_proxy-function"></a><span data-ttu-id="c8adc-103">\_ \_ Функция прокси Ивиккомпонентинфо-версии</span><span class="sxs-lookup"><span data-stu-id="c8adc-103">IWICComponentInfo\_GetVersion\_Proxy function</span></span>

<span data-ttu-id="c8adc-104">Функция-посредник для [**метода WebMethod**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getversion) .</span><span class="sxs-lookup"><span data-stu-id="c8adc-104">Proxy function for the [**GetVersion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getversion) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8adc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8adc-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchVersion,
  _Inout_ WCHAR             *wzVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="c8adc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8adc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8adc-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="c8adc-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8adc-108">Тип: \**[**ивиккомпонентинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="c8adc-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="c8adc-109">Указатель на этот объект [_ *ивиккомпонентинфо* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="c8adc-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="c8adc-110">*кчверсион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c8adc-110">*cchVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8adc-111">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="c8adc-111">Type: **UINT**</span></span>

<span data-ttu-id="c8adc-112">Размер буфера *взверсион* .</span><span class="sxs-lookup"><span data-stu-id="c8adc-112">The size of the *wzVersion* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c8adc-113">*взверсион* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c8adc-113">*wzVersion* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8adc-114">Тип: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="c8adc-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="c8adc-115">Указатель, который получает неизменяемую строку языка и региональных параметров для версии компонента.</span><span class="sxs-lookup"><span data-stu-id="c8adc-115">A pointer that receives a culture invariant string of the component's version.</span></span>

</dd> <dt>

<span data-ttu-id="c8adc-116">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c8adc-116">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8adc-117">Тип: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="c8adc-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="c8adc-118">Указатель, получающий фактическую длину версии компонента.</span><span class="sxs-lookup"><span data-stu-id="c8adc-118">A pointer that receives the actual length of the component's version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8adc-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8adc-119">Return value</span></span>

<span data-ttu-id="c8adc-120">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="c8adc-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="c8adc-121">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c8adc-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c8adc-122">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c8adc-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8adc-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="c8adc-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c8adc-124">Требования</span><span class="sxs-lookup"><span data-stu-id="c8adc-124">Requirements</span></span>



| <span data-ttu-id="c8adc-125">Требование</span><span class="sxs-lookup"><span data-stu-id="c8adc-125">Requirement</span></span> | <span data-ttu-id="c8adc-126">Значение</span><span class="sxs-lookup"><span data-stu-id="c8adc-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8adc-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8adc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c8adc-128">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c8adc-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c8adc-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8adc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c8adc-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c8adc-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c8adc-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c8adc-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8adc-132"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8adc-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




