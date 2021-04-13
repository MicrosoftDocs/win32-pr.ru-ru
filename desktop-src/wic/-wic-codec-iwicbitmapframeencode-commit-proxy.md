---
description: Функция-посредник для метода Commit.
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
ms.openlocfilehash: 0da0cb95a13148082d8263f622bb4089a7c9bd30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343205"
---
# <a name="iwicbitmapframeencode_commit_proxy-function"></a><span data-ttu-id="3d2df-103">Ивикбитмапфраминкоде \_ фиксация \_ прокси-функции</span><span class="sxs-lookup"><span data-stu-id="3d2df-103">IWICBitmapFrameEncode\_Commit\_Proxy function</span></span>

<span data-ttu-id="3d2df-104">Функция-посредник для метода [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) .</span><span class="sxs-lookup"><span data-stu-id="3d2df-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d2df-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d2df-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Commit_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="3d2df-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d2df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d2df-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="3d2df-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d2df-108">Тип: \**[**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="3d2df-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="3d2df-109">Указатель на этот объект [_ *ивикбитмапфраминкоде* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="3d2df-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d2df-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d2df-110">Return value</span></span>

<span data-ttu-id="3d2df-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3d2df-111">Type: **HRESULT**</span></span>

<span data-ttu-id="3d2df-112">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="3d2df-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3d2df-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3d2df-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d2df-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="3d2df-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="3d2df-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3d2df-115">Requirements</span></span>



| <span data-ttu-id="3d2df-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3d2df-116">Requirement</span></span> | <span data-ttu-id="3d2df-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3d2df-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d2df-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3d2df-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3d2df-119">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3d2df-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="3d2df-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3d2df-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3d2df-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3d2df-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="3d2df-122">DLL</span><span class="sxs-lookup"><span data-stu-id="3d2df-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d2df-123"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d2df-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




