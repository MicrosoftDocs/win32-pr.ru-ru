---
description: 'Метод GetMediaLength2 извлекает длину носителя этого исходного объекта. Этот метод эквивалентен Иамтимелинесрк:: Жетмедиаленгс, но принимает значения РЕФТИМЕ.'
ms.assetid: 96685e00-4e16-4205-a6ad-8b83cf2f8c29
title: 'Метод Иамтимелинесрк:: GetMediaLength2 (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: caee510db9ddeda1923327176a634a9011601e4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685080"
---
# <a name="iamtimelinesrcgetmedialength2-method"></a><span data-ttu-id="8fbe1-104">Метод Иамтимелинесрк:: GetMediaLength2</span><span class="sxs-lookup"><span data-stu-id="8fbe1-104">IAMTimelineSrc::GetMediaLength2 method</span></span>

> [!Note]  
> <span data-ttu-id="8fbe1-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="8fbe1-105">\[Deprecated.</span></span> <span data-ttu-id="8fbe1-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8fbe1-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8fbe1-107">`GetMediaLength2`Метод получает длину носителя этого исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="8fbe1-107">The `GetMediaLength2` method retrieves the media length of this source object.</span></span> <span data-ttu-id="8fbe1-108">Этот метод эквивалентен [**иамтимелинесрк:: жетмедиаленгс**](iamtimelinesrc-getmedialength.md), но принимает значения [**рефтиме**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="8fbe1-108">This method is equivalent to [**IAMTimelineSrc::GetMediaLength**](iamtimelinesrc-getmedialength.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fbe1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fbe1-109">Syntax</span></span>


```C++
HRESULT GetMediaLength2(
   REFTIME *pLength
);
```



## <a name="parameters"></a><span data-ttu-id="8fbe1-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="8fbe1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fbe1-111">*пленгс*</span><span class="sxs-lookup"><span data-stu-id="8fbe1-111">*pLength*</span></span> 
</dt> <dd>

<span data-ttu-id="8fbe1-112">Получает длину носителя в секундах.</span><span class="sxs-lookup"><span data-stu-id="8fbe1-112">Receives the media length in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fbe1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8fbe1-113">Return value</span></span>

<span data-ttu-id="8fbe1-114">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="8fbe1-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="8fbe1-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8fbe1-115">Return code</span></span>                                                                                     | <span data-ttu-id="8fbe1-116">Описание</span><span class="sxs-lookup"><span data-stu-id="8fbe1-116">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="8fbe1-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="8fbe1-117"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="8fbe1-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="8fbe1-118">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="8fbe1-119"><dt>**E \_ нотдетерминед**</dt></span><span class="sxs-lookup"><span data-stu-id="8fbe1-119"><dt>**E\_NOTDETERMINED**</dt></span></span> </dl> | <span data-ttu-id="8fbe1-120">Для этого объекта не заданы значения времени носителя.</span><span class="sxs-lookup"><span data-stu-id="8fbe1-120">Media times are not set on this object.</span></span><br/> |
| <dl> <span data-ttu-id="8fbe1-121"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="8fbe1-121"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="8fbe1-122">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="8fbe1-122">**NULL** pointer argument.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="8fbe1-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8fbe1-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8fbe1-124">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="8fbe1-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8fbe1-125">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8fbe1-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8fbe1-126">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="8fbe1-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8fbe1-127">Требования</span><span class="sxs-lookup"><span data-stu-id="8fbe1-127">Requirements</span></span>



| <span data-ttu-id="8fbe1-128">Требование</span><span class="sxs-lookup"><span data-stu-id="8fbe1-128">Requirement</span></span> | <span data-ttu-id="8fbe1-129">Значение</span><span class="sxs-lookup"><span data-stu-id="8fbe1-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fbe1-130">Header</span><span class="sxs-lookup"><span data-stu-id="8fbe1-130">Header</span></span><br/>  | <dl> <span data-ttu-id="8fbe1-131"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fbe1-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8fbe1-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8fbe1-132">Library</span></span><br/> | <dl> <span data-ttu-id="8fbe1-133"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8fbe1-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fbe1-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8fbe1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fbe1-135">**Интерфейс Иамтимелинесрк**</span><span class="sxs-lookup"><span data-stu-id="8fbe1-135">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="8fbe1-136">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="8fbe1-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




