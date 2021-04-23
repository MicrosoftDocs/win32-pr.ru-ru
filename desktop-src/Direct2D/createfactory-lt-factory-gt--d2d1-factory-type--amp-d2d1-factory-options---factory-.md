---
title: Функция фабрики D2D1CreateFactory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) (D2d1. h)
description: Создает объект фабрики, который можно использовать для создания ресурсов Direct2D. | Функция фабрики D2D1CreateFactory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) (D2d1. h)
ms.assetid: 618d7fbc-3801-4507-8774-4e1f4f36af44
keywords:
- Фабрика D2D1CreateFactory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory), функция Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25e6588ef79b234402742d473982910255f4230
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105656811"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typed2d1_factory_optionsfactory-function"></a><span data-ttu-id="2f12d-105">D2D1CreateFactory <Factory> ( \_ Тип фабрики D2D1 \_ , \_ параметры фабрики D2D1 \_&, Factory \* \* )</span><span class="sxs-lookup"><span data-stu-id="2f12d-105">D2D1CreateFactory<Factory>(D2D1\_FACTORY\_TYPE,D2D1\_FACTORY\_OPTIONS&,Factory\*\*) Function</span></span>

<span data-ttu-id="2f12d-106">Создает объект фабрики, который можно использовать для создания ресурсов Direct2D.</span><span class="sxs-lookup"><span data-stu-id="2f12d-106">Creates a factory object that can be used to create Direct2D resources.</span></span>

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __in CONST D2D1_FACTORY_OPTIONS &factoryOptions,
    __out Factory **factory
);
```

## <a name="template-parameters"></a><span data-ttu-id="2f12d-107">Параметры шаблона</span><span class="sxs-lookup"><span data-stu-id="2f12d-107">Template Parameters</span></span>



| <span data-ttu-id="2f12d-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="2f12d-108">Parameter</span></span> | <span data-ttu-id="2f12d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="2f12d-109">Description</span></span>                                                 |
|-----------|-------------------------------------------------------------|
| <span data-ttu-id="2f12d-110">*Установлен*</span><span class="sxs-lookup"><span data-stu-id="2f12d-110">*Factory*</span></span> | <span data-ttu-id="2f12d-111">Тип создаваемого [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) .</span><span class="sxs-lookup"><span data-stu-id="2f12d-111">The type of [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) to create.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="2f12d-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f12d-112">Parameters</span></span>



| <span data-ttu-id="2f12d-113">Параметр</span><span class="sxs-lookup"><span data-stu-id="2f12d-113">Parameter</span></span>        | <span data-ttu-id="2f12d-114">Описание</span><span class="sxs-lookup"><span data-stu-id="2f12d-114">Description</span></span>                                                                     |
|------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2f12d-115">*factoryType*</span><span class="sxs-lookup"><span data-stu-id="2f12d-115">*factoryType*</span></span>    | <span data-ttu-id="2f12d-116">Потоковая модель фабрики и создаваемые ею ресурсы.</span><span class="sxs-lookup"><span data-stu-id="2f12d-116">The threading model of the factory and the resources it creates.</span></span>                |
| <span data-ttu-id="2f12d-117">*факторйоптионс*</span><span class="sxs-lookup"><span data-stu-id="2f12d-117">*factoryOptions*</span></span> | <span data-ttu-id="2f12d-118">Уровень детализации, предоставляемый слою отладки.</span><span class="sxs-lookup"><span data-stu-id="2f12d-118">The level of detail provided to the debugging layer.</span></span>                            |
| <span data-ttu-id="2f12d-119">*фабрика*</span><span class="sxs-lookup"><span data-stu-id="2f12d-119">*factory*</span></span>        | <span data-ttu-id="2f12d-120">При возврате из этого метода содержит адрес указателя на новую фабрику.</span><span class="sxs-lookup"><span data-stu-id="2f12d-120">When this method returns, contains the address of a pointer to the new factory.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="2f12d-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f12d-121">Return Value</span></span>

<span data-ttu-id="2f12d-122">Если метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="2f12d-122">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2f12d-123">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2f12d-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f12d-124">Требования</span><span class="sxs-lookup"><span data-stu-id="2f12d-124">Requirements</span></span>



| <span data-ttu-id="2f12d-125">Требование</span><span class="sxs-lookup"><span data-stu-id="2f12d-125">Requirement</span></span> | <span data-ttu-id="2f12d-126">Значение</span><span class="sxs-lookup"><span data-stu-id="2f12d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f12d-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f12d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2f12d-128">Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для \[ классических приложений Windows Vista \| приложения UWP\]</span><span class="sxs-lookup"><span data-stu-id="2f12d-128">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="2f12d-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f12d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2f12d-130">Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 классические \[ приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2f12d-130">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="2f12d-131">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="2f12d-131">Minimum supported phone</span></span><br/>  | <span data-ttu-id="2f12d-132">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="2f12d-132">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="2f12d-133">Header</span><span class="sxs-lookup"><span data-stu-id="2f12d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f12d-134"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f12d-134"><dt>D2d1.h</dt></span></span> </dl>                                                        |
| <span data-ttu-id="2f12d-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2f12d-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f12d-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f12d-136"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="2f12d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2f12d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f12d-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f12d-138"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

