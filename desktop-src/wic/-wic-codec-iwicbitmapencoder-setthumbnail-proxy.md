---
description: Функция-посредник для метода Сетсумбнаил.
ms.assetid: 6c062eaf-27a4-4d48-8315-be9bf168f999
title: Функция IWICBitmapEncoder_SetThumbnail_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_SetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d2670dae0d8ba9eeda7ca1d6dce5d3957dc59b7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497325"
---
# <a name="iwicbitmapencoder_setthumbnail_proxy-function"></a><span data-ttu-id="7ffa0-103">Ивикбитмапенкодер \_ сетсумбнаил \_ -функция</span><span class="sxs-lookup"><span data-stu-id="7ffa0-103">IWICBitmapEncoder\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="7ffa0-104">Функция-посредник для метода [**сетсумбнаил**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="7ffa0-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ffa0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ffa0-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_SetThumbnail_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR,
  _In_ IWICBitmapSource  *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="7ffa0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ffa0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ffa0-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="7ffa0-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ffa0-108">Тип: \**[**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="7ffa0-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="7ffa0-109">Указатель на этот объект [_ *ивикбитмапенкодер* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="7ffa0-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="7ffa0-110">*писумбнаил* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7ffa0-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ffa0-111">Тип: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="7ffa0-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="7ffa0-112">Значение [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) для задания в качестве глобального эскиза.</span><span class="sxs-lookup"><span data-stu-id="7ffa0-112">The [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to set as the global thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ffa0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ffa0-113">Return value</span></span>

<span data-ttu-id="7ffa0-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7ffa0-114">Type: **HRESULT**</span></span>

<span data-ttu-id="7ffa0-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7ffa0-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7ffa0-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7ffa0-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ffa0-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="7ffa0-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7ffa0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7ffa0-118">Requirements</span></span>



| <span data-ttu-id="7ffa0-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7ffa0-119">Requirement</span></span> | <span data-ttu-id="7ffa0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7ffa0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ffa0-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7ffa0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7ffa0-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ffa0-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="7ffa0-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7ffa0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7ffa0-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7ffa0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="7ffa0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7ffa0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ffa0-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ffa0-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




