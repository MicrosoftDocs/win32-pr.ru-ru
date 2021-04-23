---
description: Метод размещения \_ фильтра задает фильтр источника для использования средством обнаружения мультимедиа.
ms.assetid: 59382cb0-c472-48b8-9cc5-52f9dbc61a07
title: 'Имедиадет: метод ut_Filter:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd07ee3e2a18dcceae752e3923fd5fbdc88c0313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675438"
---
# <a name="imediadetput_filter-method"></a><span data-ttu-id="5dad2-103">Имедиадет: \_ метод фильтрации:p UT</span><span class="sxs-lookup"><span data-stu-id="5dad2-103">IMediaDet::put\_Filter method</span></span>

> [!Note]  
> <span data-ttu-id="5dad2-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="5dad2-104">\[Deprecated.</span></span> <span data-ttu-id="5dad2-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5dad2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5dad2-106">`put_Filter`Метод задает фильтр источника для использования средством обнаружения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="5dad2-106">The `put_Filter` method specifies a source filter for the media detector to use.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5dad2-107">Не добавляйте фильтр источника к диаграмме фильтра или используйте фильтр, который уже находится в графе фильтра.</span><span class="sxs-lookup"><span data-stu-id="5dad2-107">Do not add the source filter to your own filter graph, or use a filter that is already in a filter graph.</span></span> <span data-ttu-id="5dad2-108">Объект детектора мультимедиа автоматически создает внутренний граф фильтра, и размещение фильтра на другом графе может привести к непредвиденным результатам.</span><span class="sxs-lookup"><span data-stu-id="5dad2-108">The media detector object automatically builds an internal filter graph, and putting the filter in another graph can cause unexpected results.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5dad2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5dad2-109">Syntax</span></span>


```C++
HRESULT put_Filter(
  [in] IUnknown *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="5dad2-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5dad2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dad2-111">*неввал* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5dad2-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5dad2-112">Указатель на интерфейс **IUnknown** исходного фильтра.</span><span class="sxs-lookup"><span data-stu-id="5dad2-112">Pointer to the source filter's **IUnknown** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dad2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5dad2-113">Return value</span></span>

<span data-ttu-id="5dad2-114">Возвращает значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5dad2-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5dad2-115">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="5dad2-115">Possible values include the following:</span></span>



| <span data-ttu-id="5dad2-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5dad2-116">Return code</span></span>                                                                                   | <span data-ttu-id="5dad2-117">Описание</span><span class="sxs-lookup"><span data-stu-id="5dad2-117">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="5dad2-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5dad2-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5dad2-119">Успешно.</span><span class="sxs-lookup"><span data-stu-id="5dad2-119">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="5dad2-120"><dt>**\_интерфейс E**</dt></span><span class="sxs-lookup"><span data-stu-id="5dad2-120"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="5dad2-121">*неввал* не указывает на фильтр.</span><span class="sxs-lookup"><span data-stu-id="5dad2-121">*newVal* does not point to a filter.</span></span><br/> |
| <dl> <span data-ttu-id="5dad2-122"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="5dad2-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5dad2-123">**Пустой** аргумент указателя.</span><span class="sxs-lookup"><span data-stu-id="5dad2-123">**NULL** pointer argument.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="5dad2-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5dad2-124">Remarks</span></span>

<span data-ttu-id="5dad2-125">Для большинства приложений проще вызывать метод [**имедиадет::p UT \_ filename**](imediadet-put-filename.md) с именем исходного файла.</span><span class="sxs-lookup"><span data-stu-id="5dad2-125">For most applications, it is simpler to call the [**IMediaDet::put\_Filename**](imediadet-put-filename.md) method with the name of a source file.</span></span>

> [!Note]  
> <span data-ttu-id="5dad2-126">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="5dad2-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5dad2-127">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5dad2-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5dad2-128">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="5dad2-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5dad2-129">Требования</span><span class="sxs-lookup"><span data-stu-id="5dad2-129">Requirements</span></span>



| <span data-ttu-id="5dad2-130">Требование</span><span class="sxs-lookup"><span data-stu-id="5dad2-130">Requirement</span></span> | <span data-ttu-id="5dad2-131">Значение</span><span class="sxs-lookup"><span data-stu-id="5dad2-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5dad2-132">Header</span><span class="sxs-lookup"><span data-stu-id="5dad2-132">Header</span></span><br/>  | <dl> <span data-ttu-id="5dad2-133"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dad2-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5dad2-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5dad2-134">Library</span></span><br/> | <dl> <span data-ttu-id="5dad2-135"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5dad2-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dad2-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5dad2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dad2-137">**Интерфейс Имедиадет**</span><span class="sxs-lookup"><span data-stu-id="5dad2-137">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="5dad2-138">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="5dad2-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




