---
description: Функция-посредник для метода Креатеформатконвертер.
ms.assetid: 1013720a-d00e-4381-af5d-747806546692
title: Функция IWICImagingFactory_CreateFormatConverter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFormatConverter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 91e0d87a57326e413e725e056bd5f44aff152934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266143"
---
# <a name="iwicimagingfactory_createformatconverter_proxy-function"></a><span data-ttu-id="a114b-103">IWICImagingFactory \_ креатеформатконвертер \_ -функция</span><span class="sxs-lookup"><span data-stu-id="a114b-103">IWICImagingFactory\_CreateFormatConverter\_Proxy function</span></span>

<span data-ttu-id="a114b-104">Функция-посредник для метода [**креатеформатконвертер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) .</span><span class="sxs-lookup"><span data-stu-id="a114b-104">Proxy function for the [**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a114b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a114b-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateFormatConverter_Proxy(
  _In_  IWICImagingFactory  *pFactory,
  _Out_ IWICFormatConverter **ppIFormatConverter
);
```



## <a name="parameters"></a><span data-ttu-id="a114b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a114b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a114b-107">*пфактори* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a114b-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a114b-108">Тип: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="a114b-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="a114b-109">_ppIFormatConverter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a114b-109">_ppIFormatConverter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a114b-110">Тип: **[ **ивикформатконвертер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\*\***</span><span class="sxs-lookup"><span data-stu-id="a114b-110">Type: **[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\*\***</span></span>

<span data-ttu-id="a114b-111">Указатель, получающий указатель на новый [**ивикформатконвертер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter).</span><span class="sxs-lookup"><span data-stu-id="a114b-111">A pointer that receives a pointer to a new [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a114b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a114b-112">Return value</span></span>

<span data-ttu-id="a114b-113">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a114b-113">Type: **HRESULT**</span></span>

<span data-ttu-id="a114b-114">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a114b-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a114b-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a114b-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a114b-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="a114b-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a114b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a114b-117">Requirements</span></span>



| <span data-ttu-id="a114b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a114b-118">Requirement</span></span> | <span data-ttu-id="a114b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a114b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a114b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a114b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a114b-121">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a114b-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a114b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a114b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a114b-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a114b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a114b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a114b-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a114b-125"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a114b-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




