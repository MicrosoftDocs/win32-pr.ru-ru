---
description: IWICBitmapCodecInfo_GetContainerFormat_Proxy функция-прокси для метода Жетконтаинерформат.
ms.assetid: d8a2387a-fb75-4812-b046-51359071281d
title: Функция IWICBitmapCodecInfo_GetContainerFormat_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 729b4e2fe0f21fd1e96082e53194fd49bbc39ae1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086372"
---
# <a name="iwicbitmapcodecinfo_getcontainerformat_proxy-function"></a><span data-ttu-id="d010e-103">ИвикбитмапкодеЦинфо \_ жетконтаинерформат \_ -функция</span><span class="sxs-lookup"><span data-stu-id="d010e-103">IWICBitmapCodecInfo\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="d010e-104">Функция-посредник для метода [**жетконтаинерформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) .</span><span class="sxs-lookup"><span data-stu-id="d010e-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d010e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d010e-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetContainerFormat_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ GUID                *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="d010e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d010e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d010e-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="d010e-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d010e-108">Тип: **[ **ивикбитмапкодеЦинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***</span><span class="sxs-lookup"><span data-stu-id="d010e-108">Type: **[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***</span></span>

<span data-ttu-id="d010e-109">Указатель на этот объект [**ивикбитмапкодеЦинфо**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .</span><span class="sxs-lookup"><span data-stu-id="d010e-109">Pointer to this [**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="d010e-110">*пгуидконтаинерформат* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d010e-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d010e-111">Тип: **GUID \***</span><span class="sxs-lookup"><span data-stu-id="d010e-111">Type: **GUID\***</span></span>

<span data-ttu-id="d010e-112">Указатель, получающий идентификатор GUID контейнера.</span><span class="sxs-lookup"><span data-stu-id="d010e-112">A pointer that receives the container GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d010e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d010e-113">Return value</span></span>

<span data-ttu-id="d010e-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d010e-114">Type: **HRESULT**</span></span>

<span data-ttu-id="d010e-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="d010e-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d010e-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d010e-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d010e-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="d010e-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d010e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d010e-118">Requirements</span></span>



| <span data-ttu-id="d010e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d010e-119">Requirement</span></span> | <span data-ttu-id="d010e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d010e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d010e-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d010e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d010e-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d010e-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d010e-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d010e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d010e-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d010e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d010e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d010e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d010e-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d010e-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




