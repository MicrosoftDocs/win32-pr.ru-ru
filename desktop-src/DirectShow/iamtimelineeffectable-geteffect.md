---
description: Метод "Effect" получает результат на указанном уровне приоритета.
ms.assetid: 8606c457-1c4d-4a20-b674-aaf82abeb451
title: 'Метод Иамтимелиниффектабле:: Effect (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.GetEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b7a769fca28ea1f8f698b23de7df6b7c15f05234
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680069"
---
# <a name="iamtimelineeffectablegeteffect-method"></a><span data-ttu-id="2f135-103">Метод Иамтимелиниффектабле:: Effect</span><span class="sxs-lookup"><span data-stu-id="2f135-103">IAMTimelineEffectable::GetEffect method</span></span>

> [!Note]  
> <span data-ttu-id="2f135-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="2f135-104">\[Deprecated.</span></span> <span data-ttu-id="2f135-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2f135-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2f135-106">Метод " **Effect** " получает результат на указанном уровне приоритета.</span><span class="sxs-lookup"><span data-stu-id="2f135-106">The **GetEffect** method retrieves the effect at the specified priority level.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f135-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f135-107">Syntax</span></span>


```C++
HRESULT GetEffect(
  [out] IAMTimelineObj **ppFX,
        long           Which
);
```



## <a name="parameters"></a><span data-ttu-id="2f135-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f135-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f135-109">*ппфкс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2f135-109">*ppFX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f135-110">Получает интерфейс [**иамтимелинеобж**](iamtimelineobj.md) воздействия.</span><span class="sxs-lookup"><span data-stu-id="2f135-110">Receives the effect's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="2f135-111">*Какую*</span><span class="sxs-lookup"><span data-stu-id="2f135-111">*Which*</span></span> 
</dt> <dd>

<span data-ttu-id="2f135-112">Уровень приоритета получаемого результата.</span><span class="sxs-lookup"><span data-stu-id="2f135-112">Priority level of the effect to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f135-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f135-113">Return value</span></span>

<span data-ttu-id="2f135-114">Возвращает значение HRESULT.</span><span class="sxs-lookup"><span data-stu-id="2f135-114">Returns an HRESULT value.</span></span> <span data-ttu-id="2f135-115">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="2f135-115">Possible values include the following:</span></span>



| <span data-ttu-id="2f135-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2f135-116">Return code</span></span>                                                                               | <span data-ttu-id="2f135-117">Описание</span><span class="sxs-lookup"><span data-stu-id="2f135-117">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="2f135-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="2f135-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="2f135-119">Не влияет на заданный приоритет,</span><span class="sxs-lookup"><span data-stu-id="2f135-119">No effect at the specified priority,</span></span><br/> |
| <dl> <span data-ttu-id="2f135-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2f135-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="2f135-121">Успешно.</span><span class="sxs-lookup"><span data-stu-id="2f135-121">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="2f135-122"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="2f135-122"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="2f135-123">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="2f135-123">**NULL** pointer argument.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="2f135-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f135-124">Remarks</span></span>

<span data-ttu-id="2f135-125">Если метод возвращает значение " \_ ОК", возвращаемый им интерфейс **иамтимелинеобж** имеет необработанный счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="2f135-125">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="2f135-126">Не забудьте освободить интерфейс по завершении его использования.</span><span class="sxs-lookup"><span data-stu-id="2f135-126">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="2f135-127">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="2f135-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2f135-128">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2f135-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2f135-129">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2f135-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2f135-130">Требования</span><span class="sxs-lookup"><span data-stu-id="2f135-130">Requirements</span></span>



| <span data-ttu-id="2f135-131">Требование</span><span class="sxs-lookup"><span data-stu-id="2f135-131">Requirement</span></span> | <span data-ttu-id="2f135-132">Значение</span><span class="sxs-lookup"><span data-stu-id="2f135-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f135-133">Header</span><span class="sxs-lookup"><span data-stu-id="2f135-133">Header</span></span><br/>  | <dl> <span data-ttu-id="2f135-134"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f135-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2f135-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2f135-135">Library</span></span><br/> | <dl> <span data-ttu-id="2f135-136"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f135-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f135-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f135-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f135-138">**Интерфейс Иамтимелиниффектабле**</span><span class="sxs-lookup"><span data-stu-id="2f135-138">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="2f135-139">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="2f135-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




