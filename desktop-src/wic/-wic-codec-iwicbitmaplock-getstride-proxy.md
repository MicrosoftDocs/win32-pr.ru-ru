---
description: Функция-посредник для метода STRIDE.
ms.assetid: 243439f3-2267-4632-b312-75c5ae5eddaa
title: Функция IWICBitmapLock_GetStride_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapLock_GetStride_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 70e42e233235b8616cf9191189ecc9e9ff01e85f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702859"
---
# <a name="iwicbitmaplock_getstride_proxy-function"></a><span data-ttu-id="922fa-103">Ивикбитмаплокк \_ \_ -функция класса STRIDE</span><span class="sxs-lookup"><span data-stu-id="922fa-103">IWICBitmapLock\_GetStride\_Proxy function</span></span>

<span data-ttu-id="922fa-104">Функция-посредник для метода [**stride**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getstride) .</span><span class="sxs-lookup"><span data-stu-id="922fa-104">Proxy function for the [**GetStride**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmaplock-getstride) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="922fa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="922fa-105">Syntax</span></span>


```C++
HRESULT IWICBitmapLock_GetStride_Proxy(
  _In_  IWICBitmapLock *THIS_PTR,
  _Out_ UINT           *pcbStride
);
```



## <a name="parameters"></a><span data-ttu-id="922fa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="922fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="922fa-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="922fa-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="922fa-108">Тип: \**[**ивикбитмаплокк**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) \** _</span><span class="sxs-lookup"><span data-stu-id="922fa-108">Type: \**[**IWICBitmapLock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\** _</span></span>

<span data-ttu-id="922fa-109">Указатель на этот объект [_ *ивикбитмаплокк* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) .</span><span class="sxs-lookup"><span data-stu-id="922fa-109">Pointer to this [_ *IWICBitmapLock*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) object.</span></span>

</dd> <dt>

<span data-ttu-id="922fa-110">*пкбстриде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="922fa-110">*pcbStride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="922fa-111">Тип: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="922fa-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="922fa-112">Шаг точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="922fa-112">The bitmap stride.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="922fa-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="922fa-113">Return value</span></span>

<span data-ttu-id="922fa-114">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="922fa-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="922fa-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="922fa-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="922fa-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="922fa-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="922fa-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="922fa-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="922fa-118">Требования</span><span class="sxs-lookup"><span data-stu-id="922fa-118">Requirements</span></span>



| <span data-ttu-id="922fa-119">Требование</span><span class="sxs-lookup"><span data-stu-id="922fa-119">Requirement</span></span> | <span data-ttu-id="922fa-120">Значение</span><span class="sxs-lookup"><span data-stu-id="922fa-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="922fa-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="922fa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="922fa-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="922fa-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="922fa-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="922fa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="922fa-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="922fa-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="922fa-125">DLL</span><span class="sxs-lookup"><span data-stu-id="922fa-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="922fa-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="922fa-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




