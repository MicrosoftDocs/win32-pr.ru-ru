---
description: Функция-посредник для метода Commit.
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
ms.openlocfilehash: c0cd3cfbe5e1c80d82cd90303d26f2da33cf467d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072715"
---
# <a name="iwicbitmapencoder_commit_proxy-function"></a><span data-ttu-id="30a6f-103">Ивикбитмапенкодер \_ фиксация \_ прокси-функции</span><span class="sxs-lookup"><span data-stu-id="30a6f-103">IWICBitmapEncoder\_Commit\_Proxy function</span></span>

<span data-ttu-id="30a6f-104">Функция-посредник для метода [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) .</span><span class="sxs-lookup"><span data-stu-id="30a6f-104">Proxy function for the [**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="30a6f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30a6f-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_Commit_Proxy(
  _In_ IWICBitmapEncoder *THIS_PTR
);
```



## <a name="parameters"></a><span data-ttu-id="30a6f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="30a6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30a6f-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="30a6f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30a6f-108">Тип: \**[**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="30a6f-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="30a6f-109">Указатель на этот объект [_ *ивикбитмапенкодер* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="30a6f-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30a6f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30a6f-110">Return value</span></span>

<span data-ttu-id="30a6f-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="30a6f-111">Type: **HRESULT**</span></span>

<span data-ttu-id="30a6f-112">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="30a6f-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="30a6f-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="30a6f-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="30a6f-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="30a6f-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="30a6f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="30a6f-115">Requirements</span></span>



| <span data-ttu-id="30a6f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="30a6f-116">Requirement</span></span> | <span data-ttu-id="30a6f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="30a6f-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30a6f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30a6f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="30a6f-119">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="30a6f-119">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="30a6f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30a6f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="30a6f-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="30a6f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="30a6f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="30a6f-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30a6f-123"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30a6f-123"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




