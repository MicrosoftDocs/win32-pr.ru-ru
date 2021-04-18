---
description: Метод Жетсубобжект извлекает подобъект, связанный с этим объектом.
ms.assetid: 478597d6-ae13-4fa9-a928-19893f378f1a
title: 'Метод Иамтимелинеобж:: Жетсубобжект (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 74f14658db5ffbaf100925f26573a08b592f6510
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675506"
---
# <a name="iamtimelineobjgetsubobject-method"></a><span data-ttu-id="6d813-103">Метод Иамтимелинеобж:: Жетсубобжект</span><span class="sxs-lookup"><span data-stu-id="6d813-103">IAMTimelineObj::GetSubObject method</span></span>

> [!Note]  
> <span data-ttu-id="6d813-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="6d813-104">\[Deprecated.</span></span> <span data-ttu-id="6d813-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6d813-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6d813-106">`GetSubObject`Метод извлекает подобъект, связанный с этим объектом.</span><span class="sxs-lookup"><span data-stu-id="6d813-106">The `GetSubObject` method retrieves the subobject associated with this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d813-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d813-107">Syntax</span></span>


```C++
HRESULT GetSubObject(
  [out, retval] IUnknown **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="6d813-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d813-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d813-109">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6d813-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6d813-110">Получает указатель на интерфейс **IUnknown** подобъекта.</span><span class="sxs-lookup"><span data-stu-id="6d813-110">Receives a pointer to the subobject's **IUnknown** interface.</span></span> <span data-ttu-id="6d813-111">Если у объекта нет подобъекта, ему присваивается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="6d813-111">If the object does not have a subobject, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d813-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d813-112">Return value</span></span>

<span data-ttu-id="6d813-113">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="6d813-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6d813-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6d813-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d813-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d813-115">Remarks</span></span>

<span data-ttu-id="6d813-116">Каждый объект временной шкалы может содержать указатель на связанный с ним подобъект.</span><span class="sxs-lookup"><span data-stu-id="6d813-116">Every timeline object can hold a pointer to an associated subobject.</span></span>

<span data-ttu-id="6d813-117">Если значение, возвращаемое в *Pval* , не равно **null**, то интерфейс **IUnknown** имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="6d813-117">If the value returned in *pVal* is not **NULL**, the **IUnknown** interface has an outstanding reference count.</span></span> <span data-ttu-id="6d813-118">Не забудьте освободить интерфейс по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="6d813-118">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="6d813-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="6d813-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6d813-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6d813-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6d813-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="6d813-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6d813-122">Требования</span><span class="sxs-lookup"><span data-stu-id="6d813-122">Requirements</span></span>



| <span data-ttu-id="6d813-123">Требование</span><span class="sxs-lookup"><span data-stu-id="6d813-123">Requirement</span></span> | <span data-ttu-id="6d813-124">Значение</span><span class="sxs-lookup"><span data-stu-id="6d813-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d813-125">Header</span><span class="sxs-lookup"><span data-stu-id="6d813-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6d813-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d813-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6d813-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6d813-127">Library</span></span><br/> | <dl> <span data-ttu-id="6d813-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d813-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d813-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d813-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d813-130">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="6d813-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="6d813-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="6d813-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




