---
description: Инициализирует фильтр. Вызывается функцией получения образа Windows (WIA) 2,0 перед загрузкой каждого образа.
ms.assetid: 0487900d-2103-4314-b18d-58ff97d6f524
title: 'Метод Ивиаимажефилтер:: Инитиализефилтер (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.InitializeFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a113c9493128a634ce61ccf7c0362bf7a9767f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711957"
---
# <a name="iwiaimagefilterinitializefilter-method"></a><span data-ttu-id="a132e-104">Метод Ивиаимажефилтер:: Инитиализефилтер</span><span class="sxs-lookup"><span data-stu-id="a132e-104">IWiaImageFilter::InitializeFilter method</span></span>

<span data-ttu-id="a132e-105">Инициализирует фильтр.</span><span class="sxs-lookup"><span data-stu-id="a132e-105">Initializes the filter.</span></span> <span data-ttu-id="a132e-106">Вызывается функцией получения образа Windows (WIA) 2,0 перед загрузкой каждого образа.</span><span class="sxs-lookup"><span data-stu-id="a132e-106">Called by Windows Image Acquisition (WIA) 2.0 before each image download.</span></span>

## <a name="syntax"></a><span data-ttu-id="a132e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a132e-107">Syntax</span></span>


```C++
HRESULT InitializeFilter(
  [in] IWiaItem2            *pWiaItem2,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="a132e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a132e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a132e-109">*pWiaItem2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a132e-109">*pWiaItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a132e-110">Тип: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="a132e-110">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="a132e-111">Указывает указатель на элемент [_ *IWiaItem2* \*](-wia-iwiaitem2.md) , представляющий изображение для предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="a132e-111">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item that represents the preview image.</span></span>

</dd> <dt>

<span data-ttu-id="a132e-112">*пвиатрансферкаллбакк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a132e-112">*pWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a132e-113">Тип: \**[**ивиатрансферкаллбакк**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="a132e-113">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="a132e-114">Указывает указатель на интерфейс [_ *ивиатрансферкаллбакк* \*](-wia-iwiatransfercallback.md) приложения.</span><span class="sxs-lookup"><span data-stu-id="a132e-114">Specifies a pointer to the application's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a132e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a132e-115">Return value</span></span>

<span data-ttu-id="a132e-116">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a132e-116">Type: **HRESULT**</span></span>

<span data-ttu-id="a132e-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a132e-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a132e-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a132e-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a132e-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a132e-119">Remarks</span></span>

<span data-ttu-id="a132e-120">Этот метод вызывается, когда приложение вызывает [**загрузку**](-wia-iwiatransfer-download.md) и когда приложение вызывает функцию компонента предварительной версии WIA 2,0 `GetNewPreview` .</span><span class="sxs-lookup"><span data-stu-id="a132e-120">This method is called when an application calls [**Download**](-wia-iwiatransfer-download.md) and when an application calls the WIA 2.0 Preview Component's `GetNewPreview` function.</span></span> <span data-ttu-id="a132e-121">**Ивиаимажефилтер:: инитиализефилтер** сохраняет ссылки на *pWiaItem2* и *пвиатрансферкаллбакк* для передачи в эти функции.</span><span class="sxs-lookup"><span data-stu-id="a132e-121">**IWiaImageFilter::InitializeFilter** stores the references to *pWiaItem2* and *pWiaTransferCallback* to pass into these functions.</span></span> <span data-ttu-id="a132e-122">Эти два указателя интерфейса должны храниться как переменные члена, и [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) следует вызывать для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="a132e-122">These two interface pointers should be stored as member variables and [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) should be called for each.</span></span> <span data-ttu-id="a132e-123">Указатели интерфейса также необходимы в реализации фильтра [**трансферкаллбакк**](-wia-iwiatransfercallback-transfercallback.md) и [**жетнекстстреам**](-wia-iwiatransfercallback-getnextstream.md) во время получения образа.</span><span class="sxs-lookup"><span data-stu-id="a132e-123">The interface pointers are also needed in the filter's implementation of [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) and [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) during image acquisition.</span></span>

## <a name="requirements"></a><span data-ttu-id="a132e-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a132e-124">Requirements</span></span>



| <span data-ttu-id="a132e-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a132e-125">Requirement</span></span> | <span data-ttu-id="a132e-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a132e-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a132e-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a132e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a132e-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a132e-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a132e-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a132e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a132e-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a132e-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a132e-131">Header</span><span class="sxs-lookup"><span data-stu-id="a132e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a132e-132"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="a132e-132"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="a132e-133">IDL</span><span class="sxs-lookup"><span data-stu-id="a132e-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a132e-134"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a132e-134"><dt>Wia.idl</dt></span></span> </dl> |



 

 
