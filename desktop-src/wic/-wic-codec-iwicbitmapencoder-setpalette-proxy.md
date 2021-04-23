---
description: Функция-посредник для метода Сетпалетте.
ms.assetid: d8e2c36e-6886-4959-b2a2-469bebfe1cdc
title: Функция IWICBitmapEncoder_SetPalette_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 128953cd56c3bea17ec9761a2acf2b8bc89cacfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541263"
---
# <a name="iwicbitmapencoder_setpalette_proxy-function"></a><span data-ttu-id="35e06-103">Ивикбитмапенкодер \_ сетпалетте \_ -функция</span><span class="sxs-lookup"><span data-stu-id="35e06-103">IWICBitmapEncoder\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="35e06-104">Функция-посредник для метода [**сетпалетте**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="35e06-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="35e06-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35e06-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetPalette_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICPalette       *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="35e06-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="35e06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35e06-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="35e06-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e06-108">Тип: \**[**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="35e06-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="35e06-109">Указатель на этот объект [_ *ивикбитмапенкодер* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="35e06-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="35e06-110">*пипалетте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="35e06-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e06-111">Тип: \**[**ивикпалетте**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="35e06-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="35e06-112">Значение [_ *ивикпалетте* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) для использования в качестве глобальной палитры.</span><span class="sxs-lookup"><span data-stu-id="35e06-112">The [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) to use as the global palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35e06-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35e06-113">Return value</span></span>

<span data-ttu-id="35e06-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="35e06-114">Type: **HRESULT**</span></span>

<span data-ttu-id="35e06-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="35e06-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="35e06-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="35e06-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="35e06-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="35e06-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="35e06-118">Требования</span><span class="sxs-lookup"><span data-stu-id="35e06-118">Requirements</span></span>



| <span data-ttu-id="35e06-119">Требование</span><span class="sxs-lookup"><span data-stu-id="35e06-119">Requirement</span></span> | <span data-ttu-id="35e06-120">Значение</span><span class="sxs-lookup"><span data-stu-id="35e06-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35e06-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35e06-121">Minimum supported client</span></span><br/> | <span data-ttu-id="35e06-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35e06-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="35e06-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35e06-123">Minimum supported server</span></span><br/> | <span data-ttu-id="35e06-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35e06-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="35e06-125">DLL</span><span class="sxs-lookup"><span data-stu-id="35e06-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35e06-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35e06-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




