---
title: Функция фабрики D2D1CreateFactory (D2D1_FACTORY_TYPE, Factory) (D2d1. h)
description: Создает объект фабрики, который можно использовать для создания ресурсов Direct2D. | Функция фабрики D2D1CreateFactory (D2D1_FACTORY_TYPE, Factory) (D2d1. h)
ms.assetid: c1c25d51-15ea-4075-a896-bd6501bf68c1
keywords:
- Фабрика D2D1CreateFactory (D2D1_FACTORY_TYPE, Factory), функция Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03400cec8c838ba561a7eb504674e074d7b3199
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105647799"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typefactory-function"></a><span data-ttu-id="5b80a-105"><Factory>Функция D2D1CreateFactory ( \_ Тип фабрики D2D1 \_ , фабрика \* \* )</span><span class="sxs-lookup"><span data-stu-id="5b80a-105">D2D1CreateFactory<Factory>(D2D1\_FACTORY\_TYPE,Factory\*\*) Function</span></span>

<span data-ttu-id="5b80a-106">Создает объект фабрики, который можно использовать для создания ресурсов Direct2D.</span><span class="sxs-lookup"><span data-stu-id="5b80a-106">Creates a factory object that can be used to create Direct2D resources.</span></span>

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __out Factory **factory
);
```

## <a name="template-parameters"></a><span data-ttu-id="5b80a-107">Параметры шаблона</span><span class="sxs-lookup"><span data-stu-id="5b80a-107">Template Parameters</span></span>



| <span data-ttu-id="5b80a-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="5b80a-108">Parameter</span></span> | <span data-ttu-id="5b80a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5b80a-109">Description</span></span>                                                 |
|-----------|-------------------------------------------------------------|
| <span data-ttu-id="5b80a-110">*Установлен*</span><span class="sxs-lookup"><span data-stu-id="5b80a-110">*Factory*</span></span> | <span data-ttu-id="5b80a-111">Тип создаваемого [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) .</span><span class="sxs-lookup"><span data-stu-id="5b80a-111">The type of [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) to create.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="5b80a-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="5b80a-112">Parameters</span></span>



| <span data-ttu-id="5b80a-113">Параметр</span><span class="sxs-lookup"><span data-stu-id="5b80a-113">Parameter</span></span>     | <span data-ttu-id="5b80a-114">Описание</span><span class="sxs-lookup"><span data-stu-id="5b80a-114">Description</span></span>                                                                     |
|---------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="5b80a-115">*factoryType*</span><span class="sxs-lookup"><span data-stu-id="5b80a-115">*factoryType*</span></span> | <span data-ttu-id="5b80a-116">Потоковая модель фабрики и создаваемые ею ресурсы.</span><span class="sxs-lookup"><span data-stu-id="5b80a-116">The threading model of the factory and the resources it creates.</span></span>                |
| <span data-ttu-id="5b80a-117">*фабрика*</span><span class="sxs-lookup"><span data-stu-id="5b80a-117">*factory*</span></span>     | <span data-ttu-id="5b80a-118">При возврате из этого метода содержит адрес указателя на новую фабрику.</span><span class="sxs-lookup"><span data-stu-id="5b80a-118">When this method returns, contains the address of a pointer to the new factory.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="5b80a-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5b80a-119">Return Value</span></span>

<span data-ttu-id="5b80a-120">Если метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="5b80a-120">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5b80a-121">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5b80a-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="examples"></a><span data-ttu-id="5b80a-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="5b80a-122">Examples</span></span>

<span data-ttu-id="5b80a-123">В следующем примере создается фабрика.</span><span class="sxs-lookup"><span data-stu-id="5b80a-123">The following example creates a factory.</span></span>


```C++
HRESULT DemoApp::CreateDeviceIndependentResources()
{
    HRESULT hr = S_OK;

    // Create a Direct2D factory.
    hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="5b80a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="5b80a-124">Requirements</span></span>



| <span data-ttu-id="5b80a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="5b80a-125">Requirement</span></span> | <span data-ttu-id="5b80a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="5b80a-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b80a-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5b80a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5b80a-128">Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для \[ классических приложений Windows Vista \| приложения UWP\]</span><span class="sxs-lookup"><span data-stu-id="5b80a-128">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="5b80a-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5b80a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5b80a-130">Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 классические \[ приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5b80a-130">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="5b80a-131">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="5b80a-131">Minimum supported phone</span></span><br/>  | <span data-ttu-id="5b80a-132">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="5b80a-132">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="5b80a-133">Header</span><span class="sxs-lookup"><span data-stu-id="5b80a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b80a-134"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b80a-134"><dt>D2d1.h</dt></span></span> </dl>                                                        |
| <span data-ttu-id="5b80a-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5b80a-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="5b80a-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b80a-136"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="5b80a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="5b80a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b80a-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b80a-138"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

