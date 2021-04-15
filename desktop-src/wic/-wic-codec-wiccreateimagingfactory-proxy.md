---
description: Функция-посредник для создания IWICImagingFactory.
ms.assetid: e4f575b0-878f-461e-92e7-9494e505ea6f
title: Функция WICCreateImagingFactory_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateImagingFactory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Windowscodecs.lib
ms.openlocfilehash: 6717764d0c25d64f99ab5d864bd0e77a63b88330
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702390"
---
# <a name="wiccreateimagingfactory_proxy-function"></a><span data-ttu-id="01427-103">Виккреатеимагингфактори \_ -функция прокси</span><span class="sxs-lookup"><span data-stu-id="01427-103">WICCreateImagingFactory\_Proxy function</span></span>

<span data-ttu-id="01427-104">Функция-посредник для создания [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span><span class="sxs-lookup"><span data-stu-id="01427-104">Proxy function for creating the [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span></span>

## <a name="syntax"></a><span data-ttu-id="01427-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01427-105">Syntax</span></span>

```cpp
HRESULT WICCreateImagingFactory_Proxy(
  _In_  UINT               SDKVersion,
  _Out_ IWICImagingFactory **ppIImagingFactory
);
```

## <a name="parameters"></a><span data-ttu-id="01427-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="01427-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01427-107">*Сдкверсион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01427-107">*SDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01427-108">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="01427-108">Type: **UINT**</span></span>

</dd> <dt>

<span data-ttu-id="01427-109">*ппиимагингфактори* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="01427-109">*ppIImagingFactory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01427-110">Тип: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***</span><span class="sxs-lookup"><span data-stu-id="01427-110">Type: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01427-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01427-111">Return value</span></span>

<span data-ttu-id="01427-112">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="01427-112">Type: **HRESULT**</span></span>

<span data-ttu-id="01427-113">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="01427-113">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="01427-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="01427-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="01427-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01427-115">Remarks</span></span>

<span data-ttu-id="01427-116">Эта функция является вспомогательной функцией для создания фабрики WIC для явной компоновки DLL, которая была необходима для Windows XP.</span><span class="sxs-lookup"><span data-stu-id="01427-116">This function is a helper for creating a WIC factory for explicit DLL linking, which was needed for Windows XP.</span></span> <span data-ttu-id="01427-117">В нормальном использовании вместо этого следует использовать [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (см. [фабрики классов API WIC](./-wic-api.md#class-factories)), так как они всегда включаются во все более новые версии Windows.</span><span class="sxs-lookup"><span data-stu-id="01427-117">In normal usage, you would use [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) instead (see [WIC API class factories](./-wic-api.md#class-factories)), since that's always included in all newer versions of Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="01427-118">Требования</span><span class="sxs-lookup"><span data-stu-id="01427-118">Requirements</span></span>



| <span data-ttu-id="01427-119">Требование</span><span class="sxs-lookup"><span data-stu-id="01427-119">Requirement</span></span> | <span data-ttu-id="01427-120">Значение</span><span class="sxs-lookup"><span data-stu-id="01427-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01427-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01427-121">Minimum supported client</span></span><br/> | <span data-ttu-id="01427-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01427-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="01427-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01427-123">Minimum supported server</span></span><br/> | <span data-ttu-id="01427-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="01427-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="01427-125">DLL</span><span class="sxs-lookup"><span data-stu-id="01427-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01427-126"><dt>Windowscodecs.dll; </dt> <dt>виндовскодекс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01427-126"><dt>Windowscodecs.dll; </dt> <dt>windowscodecs.lib</dt></span></span> </dl> |



 

