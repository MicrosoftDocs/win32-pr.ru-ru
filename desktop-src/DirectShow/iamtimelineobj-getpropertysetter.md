---
description: Метод Жетпропертисеттер извлекает свойство метода задания свойства объекта. При подготовке к просмотру объекта сведения о свойствах, содержащиеся в методе задания свойств, применяются к объекту.
ms.assetid: 7a9c5ee4-2df6-4eaa-a583-5efea0cf7bde
title: 'Метод Иамтимелинеобж:: Жетпропертисеттер (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4410a0b63a0228d9e8e403ef1f0403d1968ad639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689181"
---
# <a name="iamtimelineobjgetpropertysetter-method"></a><span data-ttu-id="1afec-104">Метод Иамтимелинеобж:: Жетпропертисеттер</span><span class="sxs-lookup"><span data-stu-id="1afec-104">IAMTimelineObj::GetPropertySetter method</span></span>

> [!Note]  
> <span data-ttu-id="1afec-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="1afec-105">\[Deprecated.</span></span> <span data-ttu-id="1afec-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1afec-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1afec-107">`GetPropertySetter`Метод получает свойство задания свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="1afec-107">The `GetPropertySetter` method retrieves the object's property setter.</span></span> <span data-ttu-id="1afec-108">При подготовке к просмотру объекта сведения о свойствах, содержащиеся в методе задания свойств, применяются к объекту.</span><span class="sxs-lookup"><span data-stu-id="1afec-108">When the object is rendered, the property information contained in the property setter is applied to the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1afec-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1afec-109">Syntax</span></span>


```C++
HRESULT GetPropertySetter(
  [out, retval] IPropertySetter **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="1afec-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="1afec-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1afec-111">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1afec-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1afec-112">Получает указатель на интерфейс [**ипропертисеттер**](ipropertysetter.md) метода задания свойства.</span><span class="sxs-lookup"><span data-stu-id="1afec-112">Receives a pointer to the property setter's [**IPropertySetter**](ipropertysetter.md) interface.</span></span> <span data-ttu-id="1afec-113">Если объект не имеет метода задания свойства, ему присваивается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="1afec-113">If the object does not have a property setter, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1afec-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1afec-114">Return value</span></span>

<span data-ttu-id="1afec-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="1afec-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1afec-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1afec-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1afec-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1afec-117">Remarks</span></span>

<span data-ttu-id="1afec-118">Если значение, возвращаемое в *Pval* , не равно **null**, то интерфейс **ипропертисеттер** имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="1afec-118">If the value returned in *pVal* is not **NULL**, the **IPropertySetter** interface has an outstanding reference count.</span></span> <span data-ttu-id="1afec-119">Не забудьте освободить интерфейс по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="1afec-119">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="1afec-120">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="1afec-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1afec-121">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1afec-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1afec-122">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="1afec-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1afec-123">Требования</span><span class="sxs-lookup"><span data-stu-id="1afec-123">Requirements</span></span>



| <span data-ttu-id="1afec-124">Требование</span><span class="sxs-lookup"><span data-stu-id="1afec-124">Requirement</span></span> | <span data-ttu-id="1afec-125">Значение</span><span class="sxs-lookup"><span data-stu-id="1afec-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1afec-126">Header</span><span class="sxs-lookup"><span data-stu-id="1afec-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1afec-127"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="1afec-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1afec-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1afec-128">Library</span></span><br/> | <dl> <span data-ttu-id="1afec-129"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1afec-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1afec-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1afec-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1afec-131">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="1afec-131">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="1afec-132">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="1afec-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




