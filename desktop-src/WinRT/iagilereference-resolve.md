---
description: Возвращает идентификатор интерфейса гибкой ссылки на объект.
ms.assetid: 627A7EE4-CFEF-47F6-BA99-51BEB78C5D55
title: 'Метод Иагилереференце:: Resolve'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAgileReference.Resolve
api_type:
- COM
api_location:
- objidl.h
ms.openlocfilehash: 1c3ac95802a44f4305abb24566744ad98c67b174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701575"
---
# <a name="iagilereferenceresolve-method"></a><span data-ttu-id="9e3d0-103">Метод Иагилереференце:: Resolve</span><span class="sxs-lookup"><span data-stu-id="9e3d0-103">IAgileReference::Resolve method</span></span>

<span data-ttu-id="9e3d0-104">Возвращает идентификатор интерфейса гибкой ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-104">Gets the interface ID of an agile reference to an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e3d0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9e3d0-105">Syntax</span></span>


```C++
HRESULT Resolve(
  [in]          REFIID riid,
  [out, retval] void   **ppvObjectReference
);
```



## <a name="parameters"></a><span data-ttu-id="9e3d0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e3d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e3d0-107">*riid* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9e3d0-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e3d0-108">Идентификатор интерфейса для извлечения из ссылки Agile.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-108">The interface ID of the interface to be retrieved from the agile reference.</span></span> <span data-ttu-id="9e3d0-109">Он не обязательно должен совпадать с зарегистрированным интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-109">It is not required to be the same as the registered interface.</span></span>

</dd> <dt>

<span data-ttu-id="9e3d0-110">*ппвобжектреференце* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="9e3d0-110">*ppvObjectReference* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9e3d0-111">При успешном завершении \* *ппвобжектреференце* является указателем на интерфейс, заданный параметром *riid*.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-111">On successful completion, \**ppvObjectReference* is a pointer to the interface specified by *riid*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e3d0-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e3d0-112">Return value</span></span>

<span data-ttu-id="9e3d0-113">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-113">This method can return one of these values.</span></span>



| <span data-ttu-id="9e3d0-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e3d0-114">Return value</span></span>                                                                              | <span data-ttu-id="9e3d0-115">Описание</span><span class="sxs-lookup"><span data-stu-id="9e3d0-115">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9e3d0-116"><dt>\_ОК</dt></span><span class="sxs-lookup"><span data-stu-id="9e3d0-116"><dt>S\_OK</dt></span></span> </dl>          | <span data-ttu-id="9e3d0-117">Метод завершился успешно.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-117">The method completed successfully.</span></span><br/>                                  |
| <dl> <span data-ttu-id="9e3d0-118"><dt>\_интерфейс E</dt></span><span class="sxs-lookup"><span data-stu-id="9e3d0-118"><dt>E\_NOINTERFACE</dt></span></span> </dl> | <span data-ttu-id="9e3d0-119">Запрошенный интерфейс не реализован в зарегистрированном объекте.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-119">The requested interface isn't implemented on the registered object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9e3d0-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e3d0-120">Remarks</span></span>

<span data-ttu-id="9e3d0-121">Вызовите функцию [**рожетагилереференце**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) , чтобы создать динамическую ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="9e3d0-121">Call the [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) function to create an agile reference to an object.</span></span> <span data-ttu-id="9e3d0-122">Вызовите метод **Resolve** для локализации объекта в апартамент, в котором вызывается **разрешение Resolve** .</span><span class="sxs-lookup"><span data-stu-id="9e3d0-122">Call the **Resolve** method to localize the object into the apartment in which **Resolve** is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e3d0-123">Требования</span><span class="sxs-lookup"><span data-stu-id="9e3d0-123">Requirements</span></span>



| <span data-ttu-id="9e3d0-124">Требование</span><span class="sxs-lookup"><span data-stu-id="9e3d0-124">Requirement</span></span> | <span data-ttu-id="9e3d0-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9e3d0-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9e3d0-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9e3d0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9e3d0-127">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="9e3d0-127">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>            |
| <span data-ttu-id="9e3d0-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9e3d0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9e3d0-129">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="9e3d0-129">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e3d0-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e3d0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e3d0-131">**иагилереференце**</span><span class="sxs-lookup"><span data-stu-id="9e3d0-131">**IAgileReference**</span></span>](/windows/desktop/api/objidl/nn-objidl-iagilereference)
</dt> <dt>

[<span data-ttu-id="9e3d0-132">**рожетагилереференце**</span><span class="sxs-lookup"><span data-stu-id="9e3d0-132">**RoGetAgileReference**</span></span>](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference)
</dt> </dl>

 

 




