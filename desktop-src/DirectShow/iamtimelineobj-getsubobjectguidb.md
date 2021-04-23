---
description: 'Метод Жетсубобжектгуидб извлекает идентификатор GUID для подобъекта, связанного с этим объектом временной шкалы. Этот метод эквивалентен Иамтимелинеобж:: Жетсубобжектгуид, но получает значение BSTR.'
ms.assetid: 693cafda-78c8-4ba4-90d7-23fedcd1fc52
title: 'Метод Иамтимелинеобж:: Жетсубобжектгуидб (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 903c6638eececd635af2facd964adabe26f0c106
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675236"
---
# <a name="iamtimelineobjgetsubobjectguidb-method"></a><span data-ttu-id="4df54-104">Метод Иамтимелинеобж:: Жетсубобжектгуидб</span><span class="sxs-lookup"><span data-stu-id="4df54-104">IAMTimelineObj::GetSubObjectGUIDB method</span></span>

> [!Note]  
> <span data-ttu-id="4df54-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="4df54-105">\[Deprecated.</span></span> <span data-ttu-id="4df54-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4df54-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4df54-107">`GetSubObjectGUIDB`Метод получает идентификатор GUID подобъекта, связанного с этим объектом временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="4df54-107">The `GetSubObjectGUIDB` method retrieves the GUID of the subobject associated with this timeline object.</span></span> <span data-ttu-id="4df54-108">Этот метод эквивалентен [**иамтимелинеобж:: жетсубобжектгуид**](iamtimelineobj-getsubobjectguid.md), но получает значение **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="4df54-108">This method is equivalent to [**IAMTimelineObj::GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md), but receives a **BSTR** value.</span></span>

## <a name="syntax"></a><span data-ttu-id="4df54-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4df54-109">Syntax</span></span>


```C++
HRESULT GetSubObjectGUIDB(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="4df54-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4df54-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4df54-111">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4df54-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4df54-112">Получает строку, представляющую GUID подобъекта.</span><span class="sxs-lookup"><span data-stu-id="4df54-112">Receives a string representing the subobject GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4df54-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4df54-113">Return value</span></span>

<span data-ttu-id="4df54-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4df54-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4df54-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4df54-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4df54-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4df54-116">Remarks</span></span>

<span data-ttu-id="4df54-117">Метод выделяет память для строки.</span><span class="sxs-lookup"><span data-stu-id="4df54-117">The method allocates memory for the string.</span></span> <span data-ttu-id="4df54-118">Приложение должно вызвать **сисфристринг** для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="4df54-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="4df54-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="4df54-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4df54-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4df54-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4df54-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="4df54-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4df54-122">Требования</span><span class="sxs-lookup"><span data-stu-id="4df54-122">Requirements</span></span>



| <span data-ttu-id="4df54-123">Требование</span><span class="sxs-lookup"><span data-stu-id="4df54-123">Requirement</span></span> | <span data-ttu-id="4df54-124">Значение</span><span class="sxs-lookup"><span data-stu-id="4df54-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4df54-125">Header</span><span class="sxs-lookup"><span data-stu-id="4df54-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4df54-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="4df54-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4df54-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="4df54-127">Library</span></span><br/> | <dl> <span data-ttu-id="4df54-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4df54-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4df54-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4df54-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4df54-130">**Интерфейс Иамтимелинеобж**</span><span class="sxs-lookup"><span data-stu-id="4df54-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="4df54-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="4df54-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




