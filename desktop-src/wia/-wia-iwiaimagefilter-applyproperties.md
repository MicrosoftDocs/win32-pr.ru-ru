---
description: Включает фильтр обработки изображений для записи свойств обратно в драйвер (и на устройство).
ms.assetid: b9bb8d81-2945-46ba-a0a2-7009000574aa
title: 'Метод Ивиаимажефилтер:: Апплипропертиес (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.ApplyProperties
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3c20527ee587b975adea34e7c480349836620015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711956"
---
# <a name="iwiaimagefilterapplyproperties-method"></a><span data-ttu-id="828d6-103">Метод Ивиаимажефилтер:: Апплипропертиес</span><span class="sxs-lookup"><span data-stu-id="828d6-103">IWiaImageFilter::ApplyProperties method</span></span>

<span data-ttu-id="828d6-104">Включает фильтр обработки изображений для записи свойств обратно в драйвер (и на устройство).</span><span class="sxs-lookup"><span data-stu-id="828d6-104">Enables the image processing filter to write properties back to the driver (and device).</span></span>

## <a name="syntax"></a><span data-ttu-id="828d6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="828d6-105">Syntax</span></span>


```C++
HRESULT ApplyProperties(
  [in] IWiaPropertyStorage *pWiaPropertyStorage
);
```



## <a name="parameters"></a><span data-ttu-id="828d6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="828d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="828d6-107">*пвиапропертистораже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="828d6-107">*pWiaPropertyStorage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="828d6-108">Тип: \**[**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) \** _</span><span class="sxs-lookup"><span data-stu-id="828d6-108">Type: \**[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)\** _</span></span>

<span data-ttu-id="828d6-109">Указывает указатель на [_ *ивиапропертистораже* \*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) для применяемых свойств.</span><span class="sxs-lookup"><span data-stu-id="828d6-109">Specifies a pointer to the [_ *IWiaPropertyStorage*\*](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) for the properties to be applied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="828d6-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="828d6-110">Return value</span></span>

<span data-ttu-id="828d6-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="828d6-111">Type: **HRESULT**</span></span>

<span data-ttu-id="828d6-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="828d6-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="828d6-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="828d6-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="828d6-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="828d6-114">Remarks</span></span>

<span data-ttu-id="828d6-115">Не вызывайте этот метод непосредственно из приложения.</span><span class="sxs-lookup"><span data-stu-id="828d6-115">Do not call this method directly from your application.</span></span> <span data-ttu-id="828d6-116">Он вызывается функцией получения образа Windows (WIA) 2,0 после того, как фильтр обработки образов обработал необработанные данные.</span><span class="sxs-lookup"><span data-stu-id="828d6-116">It is called by Windows Image Acquisition (WIA) 2.0 after the image processing filter has processed the raw data.</span></span>

<span data-ttu-id="828d6-117">*пвиапропертистораже* — это интерфейс [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) , в который фильтр обработки изображений должен записывать свойства.</span><span class="sxs-lookup"><span data-stu-id="828d6-117">*pWiaPropertyStorage* is the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface into which the image processing filter should write properties.</span></span> <span data-ttu-id="828d6-118">Фильтр обработки изображений должен использовать только метод [ипропертистораже:: вритемултипле](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) для записи свойств.</span><span class="sxs-lookup"><span data-stu-id="828d6-118">An image processing filter should use only the [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) method to write properties.</span></span>

<span data-ttu-id="828d6-119">Этот метод позволяет фильтру обработки изображений записывать свойства обратно в драйвер (и на устройство).</span><span class="sxs-lookup"><span data-stu-id="828d6-119">This method allows the image processing filter to write properties back to the driver (and device).</span></span> <span data-ttu-id="828d6-120">Это может потребоваться для фильтров, которые реализуют такие функции, как автоматическая раскрытие во время сканирования пленки.</span><span class="sxs-lookup"><span data-stu-id="828d6-120">This may be necessary for filters that implement features such as auto-exposure during film scanning.</span></span>

## <a name="requirements"></a><span data-ttu-id="828d6-121">Требования</span><span class="sxs-lookup"><span data-stu-id="828d6-121">Requirements</span></span>



| <span data-ttu-id="828d6-122">Требование</span><span class="sxs-lookup"><span data-stu-id="828d6-122">Requirement</span></span> | <span data-ttu-id="828d6-123">Значение</span><span class="sxs-lookup"><span data-stu-id="828d6-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="828d6-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="828d6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="828d6-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="828d6-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="828d6-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="828d6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="828d6-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="828d6-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="828d6-128">Header</span><span class="sxs-lookup"><span data-stu-id="828d6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="828d6-129"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="828d6-129"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="828d6-130">IDL</span><span class="sxs-lookup"><span data-stu-id="828d6-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="828d6-131"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="828d6-131"><dt>Wia.idl</dt></span></span> </dl> |



 

 
