---
description: Функция-посредник для метода Жетколоркаунт.
ms.assetid: 2ad87383-4d30-4df0-b43a-95fdad1d59f9
title: Функция IWICPalette_GetColorCount_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColorCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9518878dd05c6b89152b91863c8996f96b8e6e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911384"
---
# <a name="iwicpalette_getcolorcount_proxy-function"></a><span data-ttu-id="ea79b-103">Ивикпалетте \_ жетколоркаунт \_ -функция</span><span class="sxs-lookup"><span data-stu-id="ea79b-103">IWICPalette\_GetColorCount\_Proxy function</span></span>

<span data-ttu-id="ea79b-104">Функция-посредник для метода [**жетколоркаунт**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolorcount) .</span><span class="sxs-lookup"><span data-stu-id="ea79b-104">Proxy function for the [**GetColorCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolorcount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea79b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ea79b-105">Syntax</span></span>


```C++
HRESULT IWICPalette_GetColorCount_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _Out_ UINT        *pcCount
);
```



## <a name="parameters"></a><span data-ttu-id="ea79b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea79b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea79b-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="ea79b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea79b-108">Тип: \**[**ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="ea79b-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="ea79b-109">Указатель на этот объект [_ *ивикпалетте* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) .</span><span class="sxs-lookup"><span data-stu-id="ea79b-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="ea79b-110">*пккаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ea79b-110">*pcCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea79b-111">Тип: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="ea79b-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="ea79b-112">Указатель, получающий количество цветов в таблице цветов.</span><span class="sxs-lookup"><span data-stu-id="ea79b-112">Pointer that receives the number of colors in the color table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea79b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea79b-113">Return value</span></span>

<span data-ttu-id="ea79b-114">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="ea79b-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="ea79b-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="ea79b-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ea79b-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ea79b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea79b-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="ea79b-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ea79b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ea79b-118">Requirements</span></span>



| <span data-ttu-id="ea79b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ea79b-119">Requirement</span></span> | <span data-ttu-id="ea79b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ea79b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea79b-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea79b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ea79b-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea79b-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ea79b-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea79b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ea79b-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ea79b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ea79b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ea79b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea79b-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea79b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




