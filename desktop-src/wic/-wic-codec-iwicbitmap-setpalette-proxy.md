---
description: IWICBitmap_SetPalette_Proxy функция-прокси для метода Сетпалетте.
ms.assetid: 3fd60833-7f21-4654-883a-2dd88c403bc8
title: Функция IWICBitmap_SetPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fc8d6181cf9fe9313755fd52d54319f266f4cae6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086412"
---
# <a name="iwicbitmap_setpalette_proxy-function"></a><span data-ttu-id="dd049-103">Ивикбитмап \_ сетпалетте \_ -функция</span><span class="sxs-lookup"><span data-stu-id="dd049-103">IWICBitmap\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="dd049-104">Функция-посредник для метода [**сетпалетте**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="dd049-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd049-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd049-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetPalette_Proxy(
  _In_ IWICBitmap  *THIS_PTR,
  _In_ IWICPalette *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="dd049-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd049-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd049-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="dd049-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd049-108">Тип: **[ **ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span><span class="sxs-lookup"><span data-stu-id="dd049-108">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span></span>

<span data-ttu-id="dd049-109">Указатель на этот объект [**ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="dd049-109">Pointer to this [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="dd049-110">*пипалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dd049-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd049-111">Тип: **[ **ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="dd049-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="dd049-112">Палитра, используемая для преобразования.</span><span class="sxs-lookup"><span data-stu-id="dd049-112">The palette to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd049-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd049-113">Return value</span></span>

<span data-ttu-id="dd049-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dd049-114">Type: **HRESULT**</span></span>

<span data-ttu-id="dd049-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="dd049-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dd049-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dd049-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd049-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="dd049-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="dd049-118">Требования</span><span class="sxs-lookup"><span data-stu-id="dd049-118">Requirements</span></span>



| <span data-ttu-id="dd049-119">Требование</span><span class="sxs-lookup"><span data-stu-id="dd049-119">Requirement</span></span> | <span data-ttu-id="dd049-120">Значение</span><span class="sxs-lookup"><span data-stu-id="dd049-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd049-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd049-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dd049-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dd049-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="dd049-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd049-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dd049-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dd049-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="dd049-125">DLL</span><span class="sxs-lookup"><span data-stu-id="dd049-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd049-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd049-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




