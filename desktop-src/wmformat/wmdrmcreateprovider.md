---
title: Функция Вмдрмкреатепровидер (Вмдрмсдк. h)
description: Функция Вмдрмкреатепровидер создает фабрику класса, которая может создавать другие объекты расширенных API-интерфейсов клиента DRM Windows Media.
ms.assetid: 25ec2fbf-136a-4f40-b2d3-f35b42178c60
keywords:
- Вмдрмкреатепровидер функция Windows Media Format
topic_type:
- apiref
api_name:
- WMDRMCreateProvider
api_location:
- Wmdrmsdk.dll
- Ext-MS-Win-mm-wmdrmsdk-l1-1-0.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cdf7a102d969ce916f8a5692d994c183305409a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717821"
---
# <a name="wmdrmcreateprovider-function"></a><span data-ttu-id="c9910-104">Функция Вмдрмкреатепровидер</span><span class="sxs-lookup"><span data-stu-id="c9910-104">WMDRMCreateProvider function</span></span>

<span data-ttu-id="c9910-105">Функция **вмдрмкреатепровидер** создает фабрику класса, которая может создавать другие объекты расширенных API-интерфейсов клиента DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c9910-105">The **WMDRMCreateProvider** function creates a class factory that can create the other objects of the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="c9910-106">Эта функция не требует наличия библиотеки-заглушки от корпорации Майкрософт и создает объекты, которые не поддерживают защищенные функции DRM.</span><span class="sxs-lookup"><span data-stu-id="c9910-106">This function does not require a stub library from Microsoft and creates objects that do not support the protected DRM features.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9910-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9910-107">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a><span data-ttu-id="c9910-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9910-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9910-109">*ппдрмпровидер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c9910-109">*ppDRMProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9910-110">Получает указатель на интерфейс [**ивмдрмпровидер**](iwmdrmprovider.md) только что созданного объекта.</span><span class="sxs-lookup"><span data-stu-id="c9910-110">Receives a pointer to the [**IWMDRMProvider**](iwmdrmprovider.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9910-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9910-111">Return value</span></span>

<span data-ttu-id="c9910-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c9910-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c9910-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c9910-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c9910-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c9910-114">Return code</span></span>                                                                          | <span data-ttu-id="c9910-115">Описание</span><span class="sxs-lookup"><span data-stu-id="c9910-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c9910-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c9910-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c9910-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="c9910-117">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c9910-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c9910-118">Requirements</span></span>



| <span data-ttu-id="c9910-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c9910-119">Requirement</span></span> | <span data-ttu-id="c9910-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c9910-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9910-121">Header</span><span class="sxs-lookup"><span data-stu-id="c9910-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c9910-122"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9910-122"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9910-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c9910-123">Library</span></span><br/> | <dl> <span data-ttu-id="c9910-124"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9910-124"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |
| <span data-ttu-id="c9910-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c9910-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="c9910-126"><dt>Wmdrmsdk.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9910-126"><dt>Wmdrmsdk.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9910-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9910-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9910-128">**Функции**</span><span class="sxs-lookup"><span data-stu-id="c9910-128">**Functions**</span></span>](drm-functions.md)
</dt> <dt>

[<span data-ttu-id="c9910-129">**вмдрмкреатепротектедпровидер**</span><span class="sxs-lookup"><span data-stu-id="c9910-129">**WMDRMCreateProtectedProvider**</span></span>](wmdrmcreateprotectedprovider.md)
</dt> </dl>

 

 





