---
description: Метод Жетвтракк извлекает виртуальную дорожку по указанному приоритету.
ms.assetid: e866064b-a511-4f0c-8cb1-62e4f1c42347
title: 'Метод Иамтимелинекомп:: Жетвтракк (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 06c205f700cbdb98fdc5f45bdd2ca7727e2456f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679787"
---
# <a name="iamtimelinecompgetvtrack-method"></a><span data-ttu-id="a2b75-103">Метод Иамтимелинекомп:: Жетвтракк</span><span class="sxs-lookup"><span data-stu-id="a2b75-103">IAMTimelineComp::GetVTrack method</span></span>

> [!Note]  
> <span data-ttu-id="a2b75-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="a2b75-104">\[Deprecated.</span></span> <span data-ttu-id="a2b75-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a2b75-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a2b75-106">`GetVTrack`Метод извлекает виртуальную дорожку по указанному приоритету.</span><span class="sxs-lookup"><span data-stu-id="a2b75-106">The `GetVTrack` method retrieves the virtual track at the specified priority.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2b75-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2b75-107">Syntax</span></span>


```C++
HRESULT GetVTrack(
  [out] IAMTimelineObj **ppVirtualTrack,
        long           Which
);
```



## <a name="parameters"></a><span data-ttu-id="a2b75-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2b75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2b75-109">*ппвиртуалтракк* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a2b75-109">*ppVirtualTrack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2b75-110">Получает интерфейс [**иамтимелинеобж**](iamtimelineobj.md) виртуальной записи.</span><span class="sxs-lookup"><span data-stu-id="a2b75-110">Receives the virtual track's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="a2b75-111">*Какую*</span><span class="sxs-lookup"><span data-stu-id="a2b75-111">*Which*</span></span> 
</dt> <dd>

<span data-ttu-id="a2b75-112">Приоритет извлекаемой виртуальной записи.</span><span class="sxs-lookup"><span data-stu-id="a2b75-112">Priority of the virtual track to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2b75-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2b75-113">Return value</span></span>

<span data-ttu-id="a2b75-114">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="a2b75-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="a2b75-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a2b75-115">Return code</span></span>                                                                                  | <span data-ttu-id="a2b75-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a2b75-116">Description</span></span>                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="a2b75-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a2b75-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a2b75-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="a2b75-118">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="a2b75-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a2b75-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a2b75-120">Отсутствует виртуальная дорожка с указанным приоритетом.</span><span class="sxs-lookup"><span data-stu-id="a2b75-120">No virtual track with the specified priority.</span></span><br/> |
| <dl> <span data-ttu-id="a2b75-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="a2b75-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="a2b75-122">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="a2b75-122">**NULL** pointer argument.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="a2b75-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2b75-123">Remarks</span></span>

<span data-ttu-id="a2b75-124">Если метод завершается успешно, интерфейс **иамтимелинеобж** , который он возвращает, имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="a2b75-124">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="a2b75-125">Не забудьте освободить интерфейс по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="a2b75-125">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="a2b75-126">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="a2b75-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a2b75-127">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a2b75-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a2b75-128">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="a2b75-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a2b75-129">Требования</span><span class="sxs-lookup"><span data-stu-id="a2b75-129">Requirements</span></span>



| <span data-ttu-id="a2b75-130">Требование</span><span class="sxs-lookup"><span data-stu-id="a2b75-130">Requirement</span></span> | <span data-ttu-id="a2b75-131">Значение</span><span class="sxs-lookup"><span data-stu-id="a2b75-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2b75-132">Header</span><span class="sxs-lookup"><span data-stu-id="a2b75-132">Header</span></span><br/>  | <dl> <span data-ttu-id="a2b75-133"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2b75-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a2b75-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a2b75-134">Library</span></span><br/> | <dl> <span data-ttu-id="a2b75-135"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2b75-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2b75-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2b75-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2b75-137">**Интерфейс Иамтимелинекомп**</span><span class="sxs-lookup"><span data-stu-id="a2b75-137">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="a2b75-138">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="a2b75-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




