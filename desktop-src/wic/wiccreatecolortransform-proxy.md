---
description: Создает объект преобразования цвета, реализующий Ивикколортрансформ. Этот COM-объект поддерживает объектную модель свободной потоковой модели.
ms.assetid: 43DCC3FB-B687-45F0-AAC6-DED76214716C
title: Функция WICCreateColorTransform_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorTransform_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 451b549aa44e785e406f50ccf4eb7a8317edf6b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704173"
---
# <a name="wiccreatecolortransform_proxy-function"></a><span data-ttu-id="6082a-104">Виккреатеколортрансформ \_ -функция прокси</span><span class="sxs-lookup"><span data-stu-id="6082a-104">WICCreateColorTransform\_Proxy function</span></span>

<span data-ttu-id="6082a-105">Создает объект преобразования цвета, реализующий [**ивикколортрансформ**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform).</span><span class="sxs-lookup"><span data-stu-id="6082a-105">Creates an color transform object that implements [**IWICColorTransform**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform).</span></span> <span data-ttu-id="6082a-106">Этот COM-объект поддерживает объектную модель свободной потоковой модели.</span><span class="sxs-lookup"><span data-stu-id="6082a-106">This COM object supports the free-threaded object model.</span></span>

## <a name="syntax"></a><span data-ttu-id="6082a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6082a-107">Syntax</span></span>


```C++
HRESULT WINAPI WICCreateColorTransform_Proxy(
  _Out_  **ppIColorTransform
);
```



## <a name="parameters"></a><span data-ttu-id="6082a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6082a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6082a-109">*ппиколортрансформ* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6082a-109">*ppIColorTransform* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6082a-110">Созданное преобразование цвета.</span><span class="sxs-lookup"><span data-stu-id="6082a-110">The color transform created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6082a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6082a-111">Return value</span></span>

<span data-ttu-id="6082a-112">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="6082a-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6082a-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6082a-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6082a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="6082a-114">Requirements</span></span>



| <span data-ttu-id="6082a-115">Требование</span><span class="sxs-lookup"><span data-stu-id="6082a-115">Requirement</span></span> | <span data-ttu-id="6082a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6082a-116">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6082a-117">DLL</span><span class="sxs-lookup"><span data-stu-id="6082a-117">DLL</span></span><br/> | <dl> <span data-ttu-id="6082a-118"><dt>WindowsCodecsExt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6082a-118"><dt>WindowsCodecsExt.dll</dt></span></span> </dl> |



 

 
