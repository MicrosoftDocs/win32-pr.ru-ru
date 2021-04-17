---
description: Функция-посредник для метода Копипалетте.
ms.assetid: 7dfe2367-036c-450a-ad2f-f862b77545a2
title: Функция IWICBitmapSource_CopyPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 792738a6be3966e898527c357c99a8cd6c5cfdb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703273"
---
# <a name="iwicbitmapsource_copypalette_proxy-function"></a><span data-ttu-id="66451-103">IWICBitmapSource \_ копипалетте \_ -функция</span><span class="sxs-lookup"><span data-stu-id="66451-103">IWICBitmapSource\_CopyPalette\_Proxy function</span></span>

<span data-ttu-id="66451-104">Функция-посредник для метода [**копипалетте**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) .</span><span class="sxs-lookup"><span data-stu-id="66451-104">Proxy function for the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="66451-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66451-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_CopyPalette_Proxy(
  _In_ IWICBitmapSource *THIS_PTR,
  _In_ IWICPalette      *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="66451-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="66451-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66451-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="66451-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66451-108">Тип: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="66451-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="66451-109">Указатель на этот объект [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .</span><span class="sxs-lookup"><span data-stu-id="66451-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="66451-110">*пипалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="66451-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66451-111">Тип: \**[**ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="66451-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="66451-112">Палитра.</span><span class="sxs-lookup"><span data-stu-id="66451-112">The palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66451-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="66451-113">Return value</span></span>

<span data-ttu-id="66451-114">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="66451-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="66451-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="66451-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="66451-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="66451-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="66451-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="66451-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="66451-118">Требования</span><span class="sxs-lookup"><span data-stu-id="66451-118">Requirements</span></span>



| <span data-ttu-id="66451-119">Требование</span><span class="sxs-lookup"><span data-stu-id="66451-119">Requirement</span></span> | <span data-ttu-id="66451-120">Значение</span><span class="sxs-lookup"><span data-stu-id="66451-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66451-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66451-121">Minimum supported client</span></span><br/> | <span data-ttu-id="66451-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="66451-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="66451-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66451-123">Minimum supported server</span></span><br/> | <span data-ttu-id="66451-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="66451-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="66451-125">DLL</span><span class="sxs-lookup"><span data-stu-id="66451-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66451-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66451-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




