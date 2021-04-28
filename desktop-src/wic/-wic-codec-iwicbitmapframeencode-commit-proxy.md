---
description: IWICBitmapFrameEncode_Commit_Proxy функция-прокси для метода Commit.
ms.assetid: 605801e5-00f8-4e4f-87d3-ad34d3568ee5
title: Функция IWICBitmapFrameEncode_Commit_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0f8ab87860c77cf58f73491a1fb5fc1b658ed67f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091122"
---
# <a name="iwicbitmapframeencode_commit_proxy-function"></a><span data-ttu-id="75e0d-103">Ивикбитмапфраминкоде \_ фиксация \_ прокси-функции</span><span class="sxs-lookup"><span data-stu-id="75e0d-103">IWICBitmapFrameEncode\_Commit\_Proxy function</span></span>

<span data-ttu-id="75e0d-104">Функция-посредник для метода [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) .</span><span class="sxs-lookup"><span data-stu-id="75e0d-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="75e0d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75e0d-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Commit_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="75e0d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="75e0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75e0d-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="75e0d-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75e0d-108">Тип: **[ **ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="75e0d-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="75e0d-109">Указатель на этот объект [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="75e0d-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75e0d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75e0d-110">Return value</span></span>

<span data-ttu-id="75e0d-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="75e0d-111">Type: **HRESULT**</span></span>

<span data-ttu-id="75e0d-112">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="75e0d-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="75e0d-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="75e0d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="75e0d-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="75e0d-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="75e0d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="75e0d-115">Requirements</span></span>



| <span data-ttu-id="75e0d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="75e0d-116">Requirement</span></span> | <span data-ttu-id="75e0d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="75e0d-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75e0d-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="75e0d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="75e0d-119">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75e0d-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="75e0d-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="75e0d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="75e0d-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="75e0d-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="75e0d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="75e0d-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75e0d-123"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75e0d-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




