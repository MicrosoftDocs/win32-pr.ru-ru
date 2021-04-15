---
description: Метод Жетмедиаленгс извлекает длину носителя этого исходного объекта.
ms.assetid: 70298d8f-67e7-4774-a7ae-f0b48e4afda7
title: 'Метод Иамтимелинесрк:: Жетмедиаленгс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5cd896ed0890a199f85838a01c4c6ebec6d0895d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675732"
---
# <a name="iamtimelinesrcgetmedialength-method"></a><span data-ttu-id="85202-103">Метод Иамтимелинесрк:: Жетмедиаленгс</span><span class="sxs-lookup"><span data-stu-id="85202-103">IAMTimelineSrc::GetMediaLength method</span></span>

> [!Note]  
> <span data-ttu-id="85202-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="85202-104">\[Deprecated.</span></span> <span data-ttu-id="85202-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="85202-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="85202-106">`GetMediaLength`Метод получает длину носителя этого исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="85202-106">The `GetMediaLength` method retrieves the media length of this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="85202-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85202-107">Syntax</span></span>


```C++
HRESULT GetMediaLength(
   REFERENCE_TIME *pLength
);
```



## <a name="parameters"></a><span data-ttu-id="85202-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="85202-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85202-109">*пленгс*</span><span class="sxs-lookup"><span data-stu-id="85202-109">*pLength*</span></span> 
</dt> <dd>

<span data-ttu-id="85202-110">Получает длину носителя в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="85202-110">Receives the media length in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85202-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85202-111">Return value</span></span>

<span data-ttu-id="85202-112">Возвращает одно из следующих значений **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="85202-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="85202-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="85202-113">Return code</span></span>                                                                                     | <span data-ttu-id="85202-114">Описание</span><span class="sxs-lookup"><span data-stu-id="85202-114">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="85202-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="85202-115"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="85202-116">Успешно.</span><span class="sxs-lookup"><span data-stu-id="85202-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="85202-117"><dt>**E \_ нотдетерминед**</dt></span><span class="sxs-lookup"><span data-stu-id="85202-117"><dt>**E\_NOTDETERMINED**</dt></span></span> </dl> | <span data-ttu-id="85202-118">Для этого объекта не заданы значения времени носителя.</span><span class="sxs-lookup"><span data-stu-id="85202-118">Media times are not set on this object.</span></span><br/> |
| <dl> <span data-ttu-id="85202-119"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="85202-119"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="85202-120">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="85202-120">**NULL** pointer argument.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="85202-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85202-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="85202-122">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="85202-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="85202-123">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="85202-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="85202-124">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="85202-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="85202-125">Требования</span><span class="sxs-lookup"><span data-stu-id="85202-125">Requirements</span></span>



| <span data-ttu-id="85202-126">Требование</span><span class="sxs-lookup"><span data-stu-id="85202-126">Requirement</span></span> | <span data-ttu-id="85202-127">Значение</span><span class="sxs-lookup"><span data-stu-id="85202-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85202-128">Header</span><span class="sxs-lookup"><span data-stu-id="85202-128">Header</span></span><br/>  | <dl> <span data-ttu-id="85202-129"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="85202-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="85202-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="85202-130">Library</span></span><br/> | <dl> <span data-ttu-id="85202-131"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85202-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85202-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85202-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85202-133">**Интерфейс Иамтимелинесрк**</span><span class="sxs-lookup"><span data-stu-id="85202-133">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="85202-134">**Иамтимелинесрк:: Сетмедиаленгс**</span><span class="sxs-lookup"><span data-stu-id="85202-134">**IAMTimelineSrc::SetMediaLength**</span></span>](iamtimelinesrc-setmedialength.md)
</dt> <dt>

[<span data-ttu-id="85202-135">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="85202-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




