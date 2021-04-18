---
description: Метод Жетконнектедмедиатипе Извлекает тип носителя для соединения по входному закрепления образца захвата.
ms.assetid: 65f5603a-1151-4ffd-a662-84e265663b04
title: 'Метод Исамплеграббер:: Жетконнектедмедиатипе (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetConnectedMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 85e30820afdca865f438ac40521a9be540fd4a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674972"
---
# <a name="isamplegrabbergetconnectedmediatype-method"></a><span data-ttu-id="682cb-103">Метод Исамплеграббер:: Жетконнектедмедиатипе</span><span class="sxs-lookup"><span data-stu-id="682cb-103">ISampleGrabber::GetConnectedMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="682cb-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="682cb-104">\[Deprecated.</span></span> <span data-ttu-id="682cb-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="682cb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="682cb-106">`GetConnectedMediaType`Метод извлекает тип носителя для соединения по входному закрепления образца захвата.</span><span class="sxs-lookup"><span data-stu-id="682cb-106">The `GetConnectedMediaType` method retrieves the media type for the connection on the input pin of the Sample Grabber.</span></span>

## <a name="syntax"></a><span data-ttu-id="682cb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="682cb-107">Syntax</span></span>


```C++
HRESULT GetConnectedMediaType(
   AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a><span data-ttu-id="682cb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="682cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="682cb-109">*птипе*</span><span class="sxs-lookup"><span data-stu-id="682cb-109">*pType*</span></span> 
</dt> <dd>

<span data-ttu-id="682cb-110">Указатель на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) , выделенную вызывающей стороной.</span><span class="sxs-lookup"><span data-stu-id="682cb-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure allocated by the caller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="682cb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="682cb-111">Return value</span></span>

<span data-ttu-id="682cb-112">Возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="682cb-112">Returns one of the following values.</span></span>



| <span data-ttu-id="682cb-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="682cb-113">Return code</span></span>                                                                                           | <span data-ttu-id="682cb-114">Описание</span><span class="sxs-lookup"><span data-stu-id="682cb-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="682cb-115"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="682cb-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="682cb-116">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="682cb-116">**NULL** pointer argument.</span></span><br/>   |
| <dl> <span data-ttu-id="682cb-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="682cb-117"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="682cb-118">Успешно.</span><span class="sxs-lookup"><span data-stu-id="682cb-118">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="682cb-119"><dt>**VFW \_ E \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="682cb-119"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="682cb-120">Фильтр не подключен.</span><span class="sxs-lookup"><span data-stu-id="682cb-120">The filter is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="682cb-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="682cb-121">Remarks</span></span>

<span data-ttu-id="682cb-122">Этот метод копирует тип носителя в структуру **AM \_ Media \_ Type** , заданную параметром *птипе*.</span><span class="sxs-lookup"><span data-stu-id="682cb-122">This method copies the media type into the **AM\_MEDIA\_TYPE** structure specified by *pType*.</span></span> <span data-ttu-id="682cb-123">Вызывающий объект должен освободить блок формата типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="682cb-123">The caller must free the format block of the media type.</span></span> <span data-ttu-id="682cb-124">Можно использовать функцию **CoTaskMemFree** или функцию [**фримедиатипе**](freemediatype.md) в библиотеке базового класса.</span><span class="sxs-lookup"><span data-stu-id="682cb-124">You can use the **CoTaskMemFree** function, or the [**FreeMediaType**](freemediatype.md) function in the base-class library.</span></span>

> [!Note]  
> <span data-ttu-id="682cb-125">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="682cb-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="682cb-126">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="682cb-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="682cb-127">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="682cb-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="682cb-128">Требования</span><span class="sxs-lookup"><span data-stu-id="682cb-128">Requirements</span></span>



| <span data-ttu-id="682cb-129">Требование</span><span class="sxs-lookup"><span data-stu-id="682cb-129">Requirement</span></span> | <span data-ttu-id="682cb-130">Значение</span><span class="sxs-lookup"><span data-stu-id="682cb-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="682cb-131">Header</span><span class="sxs-lookup"><span data-stu-id="682cb-131">Header</span></span><br/>  | <dl> <span data-ttu-id="682cb-132"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="682cb-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="682cb-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="682cb-133">Library</span></span><br/> | <dl> <span data-ttu-id="682cb-134"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="682cb-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="682cb-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="682cb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="682cb-136">Использование образца захвата</span><span class="sxs-lookup"><span data-stu-id="682cb-136">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="682cb-137">**Интерфейс Исамплеграббер**</span><span class="sxs-lookup"><span data-stu-id="682cb-137">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




