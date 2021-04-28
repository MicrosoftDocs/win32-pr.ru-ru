---
description: IWICBitmapEncoder_Commit_Proxy функция-прокси для метода Commit.
ms.assetid: f7f1be43-fe44-47eb-a5ba-3446c0db22a6
title: Функция IWICBitmapEncoder_Commit_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Commit_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 934b2e21097a671c2b52ea77ab07caf25ab521a3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091192"
---
# <a name="iwicbitmapencoder_commit_proxy-function"></a><span data-ttu-id="fffa2-103">Ивикбитмапенкодер \_ фиксация \_ прокси-функции</span><span class="sxs-lookup"><span data-stu-id="fffa2-103">IWICBitmapEncoder\_Commit\_Proxy function</span></span>

<span data-ttu-id="fffa2-104">Функция-посредник для метода [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) .</span><span class="sxs-lookup"><span data-stu-id="fffa2-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fffa2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fffa2-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_Commit_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="fffa2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fffa2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fffa2-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="fffa2-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fffa2-108">Тип: **[ **ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span><span class="sxs-lookup"><span data-stu-id="fffa2-108">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***</span></span>

<span data-ttu-id="fffa2-109">Указатель на этот объект [**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="fffa2-109">Pointer to this [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fffa2-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fffa2-110">Return value</span></span>

<span data-ttu-id="fffa2-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fffa2-111">Type: **HRESULT**</span></span>

<span data-ttu-id="fffa2-112">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="fffa2-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fffa2-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fffa2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fffa2-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="fffa2-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="fffa2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="fffa2-115">Requirements</span></span>



| <span data-ttu-id="fffa2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="fffa2-116">Requirement</span></span> | <span data-ttu-id="fffa2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fffa2-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fffa2-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fffa2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fffa2-119">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fffa2-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="fffa2-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fffa2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fffa2-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fffa2-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="fffa2-122">DLL</span><span class="sxs-lookup"><span data-stu-id="fffa2-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fffa2-123"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fffa2-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




