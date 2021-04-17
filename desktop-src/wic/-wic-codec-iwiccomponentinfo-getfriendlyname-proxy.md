---
description: Функция-посредник для метода Жетфриендлинаме.
ms.assetid: 8ac8f954-c2b9-47a2-88fe-b56710b5630c
title: Функция IWICComponentInfo_GetFriendlyName_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetFriendlyName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 667571169818169cb7c7ea5a1f4d3d7eb6e1635e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702589"
---
# <a name="iwiccomponentinfo_getfriendlyname_proxy-function"></a><span data-ttu-id="28435-103">Ивиккомпонентинфо \_ жетфриендлинаме \_ -функция</span><span class="sxs-lookup"><span data-stu-id="28435-103">IWICComponentInfo\_GetFriendlyName\_Proxy function</span></span>

<span data-ttu-id="28435-104">Функция-посредник для метода [**жетфриендлинаме**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname) .</span><span class="sxs-lookup"><span data-stu-id="28435-104">Proxy function for the [**GetFriendlyName**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="28435-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28435-105">Syntax</span></span>


```C++
HRESULT IWICComponentInfo_GetFriendlyName_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchFriendlyName,
  _Inout_ WCHAR             *wzFriendlyName,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="28435-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="28435-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28435-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="28435-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28435-108">Тип: \**[**ивиккомпонентинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="28435-108">Type: \**[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\** _</span></span>

<span data-ttu-id="28435-109">Указатель на этот объект [_ *ивиккомпонентинфо* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="28435-109">Pointer to this [_ *IWICComponentInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="28435-110">*кчфриендлинаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="28435-110">*cchFriendlyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28435-111">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="28435-111">Type: **UINT**</span></span>

<span data-ttu-id="28435-112">Размер буфера *взфриендлинаме* .</span><span class="sxs-lookup"><span data-stu-id="28435-112">The size of the *wzFriendlyName* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="28435-113">*взфриендлинаме* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="28435-113">*wzFriendlyName* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="28435-114">Тип: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="28435-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="28435-115">Указатель, получающий понятное имя компонента.</span><span class="sxs-lookup"><span data-stu-id="28435-115">A pointer that receives the friendly name of the component.</span></span>

<span data-ttu-id="28435-116">Возвращаемая строка зависит от языкового стандарта, 1033 по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="28435-116">The string returned is locale specific, 1033 by default.</span></span>

</dd> <dt>

<span data-ttu-id="28435-117">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="28435-117">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28435-118">Тип: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="28435-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="28435-119">Указатель, получающий фактическую длину понятного имени компонента.</span><span class="sxs-lookup"><span data-stu-id="28435-119">A pointer that receives the actual length of the component's friendly name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28435-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28435-120">Return value</span></span>

<span data-ttu-id="28435-121">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="28435-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="28435-122">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="28435-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="28435-123">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="28435-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="28435-124">Remarks</span><span class="sxs-lookup"><span data-stu-id="28435-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="28435-125">Требования</span><span class="sxs-lookup"><span data-stu-id="28435-125">Requirements</span></span>



| <span data-ttu-id="28435-126">Требование</span><span class="sxs-lookup"><span data-stu-id="28435-126">Requirement</span></span> | <span data-ttu-id="28435-127">Значение</span><span class="sxs-lookup"><span data-stu-id="28435-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28435-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28435-128">Minimum supported client</span></span><br/> | <span data-ttu-id="28435-129">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28435-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="28435-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28435-130">Minimum supported server</span></span><br/> | <span data-ttu-id="28435-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="28435-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="28435-132">DLL</span><span class="sxs-lookup"><span data-stu-id="28435-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28435-133"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28435-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




