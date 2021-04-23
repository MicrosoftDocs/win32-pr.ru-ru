---
description: Статическая функция Creator, которая может создать Ксамлуипресентер для поверхности рендеринга в классическом приложении.
ms.assetid: 3160E4C2-39D3-8FF5-ED37-78E645D1AC2E
title: Функция Креатексамлуипресентер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateXamlUIPresenter
api_type:
- DllExport
api_location:
- Windows.UI.Xaml.dll
ms.openlocfilehash: f9561a179ec4501406e26cb2bbc38ea69b64b979
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718172"
---
# <a name="createxamluipresenter-function"></a><span data-ttu-id="cdf2b-103">Функция Креатексамлуипресентер</span><span class="sxs-lookup"><span data-stu-id="cdf2b-103">CreateXamlUIPresenter function</span></span>

<span data-ttu-id="cdf2b-104">Статическая функция Creator, которая может создать [**ксамлуипресентер**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) для поверхности рендеринга в классическом приложении.</span><span class="sxs-lookup"><span data-stu-id="cdf2b-104">A static creator function that can create a [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) for a render surface in a desktop app.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdf2b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cdf2b-105">Syntax</span></span>


```C++
 static HRESULT WINAPI CreateXamlUIPresenter(
  _In_  IViewObjectPresentNotifySite                 *pPresentSite,
  _Out_ Windows::UI::Xaml::Hosting::IXamlUIPresenter **ppPresenter
);
```



## <a name="parameters"></a><span data-ttu-id="cdf2b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cdf2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdf2b-107">*ппресентсите* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cdf2b-107">*pPresentSite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf2b-108">Существующий интерфейс размещения.</span><span class="sxs-lookup"><span data-stu-id="cdf2b-108">An existing hosting interface.</span></span> <span data-ttu-id="cdf2b-109">См. раздел **ивиевобжектпресентнотифисите** в документации по Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="cdf2b-109">See **IViewObjectPresentNotifySite** in Internet Explorer documentation.</span></span>

</dd> <dt>

<span data-ttu-id="cdf2b-110">*пппресентер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cdf2b-110">*ppPresenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf2b-111">Интерфейс **\[ Ексклусивето \]** для [**ксамлуипресентер**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041).</span><span class="sxs-lookup"><span data-stu-id="cdf2b-111">The **\[exclusiveto\]** interface for a [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdf2b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cdf2b-112">Return value</span></span>

<span data-ttu-id="cdf2b-113">Стандартное **значение HRESULT**, **\_ ОК** — успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="cdf2b-113">A standard **HResult**, **S\_OK** for success.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdf2b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cdf2b-114">Remarks</span></span>

<span data-ttu-id="cdf2b-115">Для вызова этого метода требуется атрибут **DllImport** от Windows.UI.Xaml.dll.</span><span class="sxs-lookup"><span data-stu-id="cdf2b-115">Calling this method requires a **DllImport** from Windows.UI.Xaml.dll.</span></span>

<span data-ttu-id="cdf2b-116">Этот метод нельзя вызвать из приложения Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="cdf2b-116">You cannot call this method from a Windows Store app.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdf2b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="cdf2b-117">Requirements</span></span>



| <span data-ttu-id="cdf2b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="cdf2b-118">Requirement</span></span> | <span data-ttu-id="cdf2b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="cdf2b-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdf2b-120">Header</span><span class="sxs-lookup"><span data-stu-id="cdf2b-120">Header</span></span><br/> | <dl> <span data-ttu-id="cdf2b-121"><dt>Windows. UI. ксамл-коретипес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cdf2b-121"><dt>Windows.ui.xaml-coretypes.idl</dt></span></span> </dl> |
| <span data-ttu-id="cdf2b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="cdf2b-122">DLL</span></span><br/>    | <dl> <span data-ttu-id="cdf2b-123"><dt>Windows.UI.Xaml.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdf2b-123"><dt>Windows.UI.Xaml.dll</dt></span></span> </dl>           |



## <a name="see-also"></a><span data-ttu-id="cdf2b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cdf2b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdf2b-125">**ксамлуипресентер**</span><span class="sxs-lookup"><span data-stu-id="cdf2b-125">**XamlUIPresenter**</span></span>](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)
</dt> </dl>

 

 
