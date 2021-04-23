---
description: Функция-посредник для метода Креатебитмапскалер.
ms.assetid: 27fcb17e-bdcd-44cc-9fe6-f93816589b50
title: Функция IWICImagingFactory_CreateBitmapScaler_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapScaler_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ac831427901de481d313833e4ca8459ccd333384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999255"
---
# <a name="iwicimagingfactory_createbitmapscaler_proxy-function"></a><span data-ttu-id="ee51a-103">IWICImagingFactory \_ креатебитмапскалер \_ -функция</span><span class="sxs-lookup"><span data-stu-id="ee51a-103">IWICImagingFactory\_CreateBitmapScaler\_Proxy function</span></span>

<span data-ttu-id="ee51a-104">Функция-посредник для метода [**креатебитмапскалер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapscaler) .</span><span class="sxs-lookup"><span data-stu-id="ee51a-104">Proxy function for the [**CreateBitmapScaler**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapscaler) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee51a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee51a-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapScaler_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICBitmapScaler   **ppIBitmapScaler
);
```



## <a name="parameters"></a><span data-ttu-id="ee51a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee51a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee51a-107">*пфактори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee51a-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee51a-108">Тип: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="ee51a-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="ee51a-109">_ppIBitmapScaler \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ee51a-109">_ppIBitmapScaler\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee51a-110">Тип: **[ **ивикбитмапскалер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\*\***</span><span class="sxs-lookup"><span data-stu-id="ee51a-110">Type: **[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\*\***</span></span>

<span data-ttu-id="ee51a-111">Указатель, получающий указатель на новый [**ивикбитмапскалер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler).</span><span class="sxs-lookup"><span data-stu-id="ee51a-111">A pointer that receives a pointer to a new [**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee51a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee51a-112">Return value</span></span>

<span data-ttu-id="ee51a-113">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ee51a-113">Type: **HRESULT**</span></span>

<span data-ttu-id="ee51a-114">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="ee51a-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ee51a-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ee51a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee51a-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="ee51a-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ee51a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ee51a-117">Requirements</span></span>



| <span data-ttu-id="ee51a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ee51a-118">Requirement</span></span> | <span data-ttu-id="ee51a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ee51a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee51a-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee51a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ee51a-121">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ee51a-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ee51a-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ee51a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ee51a-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ee51a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ee51a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ee51a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee51a-125"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee51a-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




