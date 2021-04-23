---
description: Задает новый обратный вызов приложения для фильтра обработки изображений, используемого для переадресации вызовов.
ms.assetid: 25b86f1d-96c8-4150-9147-13be9b1dd50c
title: 'Метод Ивиаимажефилтер:: Сетневкаллбакк (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.SetNewCallback
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 16325d854f7b17c62e6fb8254819078de64977f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810774"
---
# <a name="iwiaimagefiltersetnewcallback-method"></a><span data-ttu-id="46cd3-103">Метод Ивиаимажефилтер:: Сетневкаллбакк</span><span class="sxs-lookup"><span data-stu-id="46cd3-103">IWiaImageFilter::SetNewCallback method</span></span>

<span data-ttu-id="46cd3-104">Задает новый обратный вызов приложения для фильтра обработки изображений, используемого для переадресации вызовов.</span><span class="sxs-lookup"><span data-stu-id="46cd3-104">Sets a new application callback for the image processing filter to use for forwarding calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="46cd3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46cd3-105">Syntax</span></span>


```C++
HRESULT SetNewCallback(
  [in] IWiaTransferCallback pWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="46cd3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="46cd3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46cd3-107">*пвиатрансферкаллбакк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46cd3-107">*pWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46cd3-108">Тип: **[ **ивиатрансферкаллбакк**](-wia-iwiatransfercallback.md)**</span><span class="sxs-lookup"><span data-stu-id="46cd3-108">Type: **[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)**</span></span>

<span data-ttu-id="46cd3-109">Указывает указатель на интерфейс [**ивиатрансферкаллбакк**](-wia-iwiatransfercallback.md) приложения.</span><span class="sxs-lookup"><span data-stu-id="46cd3-109">Specifies a pointer to the application's [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46cd3-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46cd3-110">Return value</span></span>

<span data-ttu-id="46cd3-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="46cd3-111">Type: **HRESULT**</span></span>

<span data-ttu-id="46cd3-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="46cd3-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="46cd3-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="46cd3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="46cd3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46cd3-114">Remarks</span></span>

<span data-ttu-id="46cd3-115">Не вызывайте этот метод непосредственно из приложения.</span><span class="sxs-lookup"><span data-stu-id="46cd3-115">Do not call this method directly from your application.</span></span>

<span data-ttu-id="46cd3-116">Фильтр обработки изображений необходим для освобождения ранее сохраненного интерфейса обратного вызова приложения перед установкой нового обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="46cd3-116">The image processing filter is required to release the previously stored application callback interface before setting the new callback.</span></span>

<span data-ttu-id="46cd3-117">Если *пвиатрансферкаллбакк* имеет **значение NULL**, фильтр обработки изображений должен просто освободить Старый обратный вызов приложения и возвратить \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="46cd3-117">If *pWiaTransferCallback* is **NULL**, the image processing filter should simply release the old application callback and return S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="46cd3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="46cd3-118">Requirements</span></span>



| <span data-ttu-id="46cd3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="46cd3-119">Requirement</span></span> | <span data-ttu-id="46cd3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="46cd3-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="46cd3-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46cd3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="46cd3-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46cd3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="46cd3-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46cd3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="46cd3-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="46cd3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="46cd3-125">Header</span><span class="sxs-lookup"><span data-stu-id="46cd3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="46cd3-126"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="46cd3-126"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="46cd3-127">IDL</span><span class="sxs-lookup"><span data-stu-id="46cd3-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="46cd3-128"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="46cd3-128"><dt>Wia.idl</dt></span></span> </dl> |



 

 




