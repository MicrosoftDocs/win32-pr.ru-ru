---
description: Функция-посредник для метода Сетресолутион.
ms.assetid: c4e3927c-6f9d-401d-acd7-711674cdbb53
title: Функция IWICBitmap_SetResolution_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: eef599147a67986c6b9853f7a67e53a15be68e00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710976"
---
# <a name="iwicbitmap_setresolution_proxy-function"></a><span data-ttu-id="8e378-103">Ивикбитмап \_ сетресолутион \_ -функция</span><span class="sxs-lookup"><span data-stu-id="8e378-103">IWICBitmap\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="8e378-104">Функция-посредник для метода [**сетресолутион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) .</span><span class="sxs-lookup"><span data-stu-id="8e378-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e378-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e378-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetResolution_Proxy(
  _In_ IWICBitmap *THIS_PTR,
  _In_ double     dpiX,
  _In_ double     dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="8e378-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e378-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e378-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="8e378-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e378-108">Тип: \**[**ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _</span><span class="sxs-lookup"><span data-stu-id="8e378-108">Type: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\** _</span></span>

<span data-ttu-id="8e378-109">Указатель на этот объект [_ *ивикбитмап* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="8e378-109">Pointer to this [_ *IWICBitmap*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="8e378-110">*дпикс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8e378-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e378-111">Тип: **Double**</span><span class="sxs-lookup"><span data-stu-id="8e378-111">Type: **double**</span></span>

<span data-ttu-id="8e378-112">Разрешение по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="8e378-112">The horizontal resolution.</span></span>

</dd> <dt>

<span data-ttu-id="8e378-113">*дпий* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8e378-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e378-114">Тип: **Double**</span><span class="sxs-lookup"><span data-stu-id="8e378-114">Type: **double**</span></span>

<span data-ttu-id="8e378-115">Разрешение по вертикали.</span><span class="sxs-lookup"><span data-stu-id="8e378-115">The vertical resolution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e378-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e378-116">Return value</span></span>

<span data-ttu-id="8e378-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8e378-117">Type: **HRESULT**</span></span>

<span data-ttu-id="8e378-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="8e378-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8e378-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8e378-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e378-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="8e378-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8e378-121">Требования</span><span class="sxs-lookup"><span data-stu-id="8e378-121">Requirements</span></span>



| <span data-ttu-id="8e378-122">Требование</span><span class="sxs-lookup"><span data-stu-id="8e378-122">Requirement</span></span> | <span data-ttu-id="8e378-123">Значение</span><span class="sxs-lookup"><span data-stu-id="8e378-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e378-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e378-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8e378-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e378-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8e378-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e378-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8e378-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8e378-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8e378-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8e378-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e378-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e378-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




