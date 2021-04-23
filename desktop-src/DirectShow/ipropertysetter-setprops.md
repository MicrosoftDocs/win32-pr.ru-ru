---
description: Метод Сетпропс задает для свойств целевого объекта соответствующее состояние в течение указанного времени.
ms.assetid: 65e701c9-d3a1-4396-9cba-a7830757701f
title: 'Метод Ипропертисеттер:: Сетпропс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6a36b1735ea5b8261c37bee66ac90b9a186a55f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675804"
---
# <a name="ipropertysettersetprops-method"></a><span data-ttu-id="0d53c-103">Метод Ипропертисеттер:: Сетпропс</span><span class="sxs-lookup"><span data-stu-id="0d53c-103">IPropertySetter::SetProps method</span></span>

> [!Note]  
> <span data-ttu-id="0d53c-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="0d53c-104">\[Deprecated.</span></span> <span data-ttu-id="0d53c-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0d53c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0d53c-106">`SetProps`Метод задает для свойств целевого объекта соответствующее состояние в течение указанного времени.</span><span class="sxs-lookup"><span data-stu-id="0d53c-106">The `SetProps` method sets the properties of the target object to the appropriate state for the specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d53c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d53c-107">Syntax</span></span>


```C++
HRESULT SetProps(
  [in] IUnknown       *pTarget,
  [in] REFERENCE_TIME rtNow
);
```



## <a name="parameters"></a><span data-ttu-id="0d53c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d53c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d53c-109">*птаржет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d53c-109">*pTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d53c-110">Указатель на целевой объект, для которого необходимо задать свойства.</span><span class="sxs-lookup"><span data-stu-id="0d53c-110">Pointer to the target object for which to set the properties.</span></span>

</dd> <dt>

<span data-ttu-id="0d53c-111">*ртнов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d53c-111">*rtNow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d53c-112">Время, когда необходимо задать свойства, в единицах измерения 100-наносекундных или – 1, чтобы задать статические свойства (которые не меняются со временем).</span><span class="sxs-lookup"><span data-stu-id="0d53c-112">Time at which to set the properties, in 100-nanosecond units, or –1 to set static properties (those that do not vary over time).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d53c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d53c-113">Return value</span></span>

<span data-ttu-id="0d53c-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="0d53c-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0d53c-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0d53c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d53c-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d53c-116">Remarks</span></span>

<span data-ttu-id="0d53c-117">Этот метод вызывается DES для задания свойств перехода или воздействия.</span><span class="sxs-lookup"><span data-stu-id="0d53c-117">This method is called by DES to set the properties on a transition or effect.</span></span> <span data-ttu-id="0d53c-118">Приложение не будет вызывать этот метод обычным образом.</span><span class="sxs-lookup"><span data-stu-id="0d53c-118">An application will not normally call this method.</span></span>

<span data-ttu-id="0d53c-119">Объект, указанный параметром *птаржет* , должен реализовывать интерфейс **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="0d53c-119">The object specified by *pTarget* must implement the **IDispatch** interface.</span></span>

> [!Note]  
> <span data-ttu-id="0d53c-120">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="0d53c-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0d53c-121">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0d53c-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0d53c-122">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="0d53c-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0d53c-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0d53c-123">Requirements</span></span>



| <span data-ttu-id="0d53c-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0d53c-124">Requirement</span></span> | <span data-ttu-id="0d53c-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0d53c-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d53c-126">Header</span><span class="sxs-lookup"><span data-stu-id="0d53c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0d53c-127"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d53c-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0d53c-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0d53c-128">Library</span></span><br/> | <dl> <span data-ttu-id="0d53c-129"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d53c-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d53c-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d53c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d53c-131">**Интерфейс Ипропертисеттер**</span><span class="sxs-lookup"><span data-stu-id="0d53c-131">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="0d53c-132">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="0d53c-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




