---
title: Функция Вмдрмкреатепротектедпровидер (Вмдрмсдк. h)
description: Функция Вмдрмкреатепротектедпровидер создает фабрику класса, которая может создавать другие объекты расширенных API-интерфейсов клиента DRM Windows Media.
ms.assetid: 0882062f-48a2-43bc-8853-a8a3d6bc2f52
keywords:
- Вмдрмкреатепротектедпровидер функция Windows Media Format
topic_type:
- apiref
api_name:
- WMDRMCreateProtectedProvider
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f046de906c7753fa200de5075cf2064721940b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694554"
---
# <a name="wmdrmcreateprotectedprovider-function"></a><span data-ttu-id="92b39-104">Функция Вмдрмкреатепротектедпровидер</span><span class="sxs-lookup"><span data-stu-id="92b39-104">WMDRMCreateProtectedProvider function</span></span>

<span data-ttu-id="92b39-105">Функция **вмдрмкреатепротектедпровидер** создает фабрику класса, которая может создавать другие объекты расширенных API-интерфейсов клиента DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="92b39-105">The **WMDRMCreateProtectedProvider** function creates a class factory that can create the other objects of the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="92b39-106">Эта функция требует наличия библиотеки-заглушки от корпорации Майкрософт и создает объекты, поддерживающие защищенные функции DRM.</span><span class="sxs-lookup"><span data-stu-id="92b39-106">This function requires a stub library from Microsoft and creates objects that support the protected DRM features.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b39-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92b39-107">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProtectedProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a><span data-ttu-id="92b39-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="92b39-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92b39-109">*ппдрмпровидер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="92b39-109">*ppDRMProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92b39-110">Получает указатель на интерфейс [**ивмдрмпровидер**](iwmdrmprovider.md) только что созданного объекта.</span><span class="sxs-lookup"><span data-stu-id="92b39-110">Receives a pointer to the [**IWMDRMProvider**](iwmdrmprovider.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92b39-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92b39-111">Return value</span></span>

<span data-ttu-id="92b39-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="92b39-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="92b39-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="92b39-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="92b39-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="92b39-114">Return code</span></span>                                                                          | <span data-ttu-id="92b39-115">Описание</span><span class="sxs-lookup"><span data-stu-id="92b39-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="92b39-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="92b39-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="92b39-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="92b39-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="92b39-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92b39-118">Remarks</span></span>

<span data-ttu-id="92b39-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="92b39-119">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="92b39-120">Требования</span><span class="sxs-lookup"><span data-stu-id="92b39-120">Requirements</span></span>



| <span data-ttu-id="92b39-121">Требование</span><span class="sxs-lookup"><span data-stu-id="92b39-121">Requirement</span></span> | <span data-ttu-id="92b39-122">Значение</span><span class="sxs-lookup"><span data-stu-id="92b39-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92b39-123">Header</span><span class="sxs-lookup"><span data-stu-id="92b39-123">Header</span></span><br/> | <dl> <span data-ttu-id="92b39-124"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="92b39-124"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92b39-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92b39-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b39-126">**Функции**</span><span class="sxs-lookup"><span data-stu-id="92b39-126">**Functions**</span></span>](drm-functions.md)
</dt> <dt>

[<span data-ttu-id="92b39-127">**вмдрмкреатепровидер**</span><span class="sxs-lookup"><span data-stu-id="92b39-127">**WMDRMCreateProvider**</span></span>](wmdrmcreateprovider.md)
</dt> </dl>

 

 





