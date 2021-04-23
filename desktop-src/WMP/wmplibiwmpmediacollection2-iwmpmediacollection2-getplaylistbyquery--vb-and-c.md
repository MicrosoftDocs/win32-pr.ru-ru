---
title: IWMPMediaCollection2 Жетплайлистбикуери, метод
description: Метод Жетплайлистбикуери возвращает интерфейс Ивмпплайлист, который предоставляет доступ к элементам мультимедиа, соответствующим условиям запроса.
ms.assetid: ebbb631f-1faa-4c89-8c1d-cc2b128126b8
keywords:
- Жетплайлистбикуери метод Windows Media Player
- Жетплайлистбикуери метод проигрывателя Windows Media Player, интерфейс IWMPMediaCollection2
- Интерфейс IWMPMediaCollection2 Windows Media Player, метод Жетплайлистбикуери
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getPlaylistByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109f6e49e77d1cfa8c6d3b45bef1d011faf21a8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648797"
---
# <a name="iwmpmediacollection2getplaylistbyquery-method"></a><span data-ttu-id="46405-106">Метод IWMPMediaCollection2:: Жетплайлистбикуери</span><span class="sxs-lookup"><span data-stu-id="46405-106">IWMPMediaCollection2::getPlaylistByQuery method</span></span>

<span data-ttu-id="46405-107">`getPlaylistByQuery`Метод возвращает интерфейс **ивмпплайлист** , который предоставляет доступ к элементам мультимедиа, соответствующим условиям запроса.</span><span class="sxs-lookup"><span data-stu-id="46405-107">The `getPlaylistByQuery` method returns an **IWMPPlaylist** interface that provides access to media items that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="46405-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46405-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getPlaylistByQuery(
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getPlaylistByQuery( _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getPlaylistByQuery
```





## <a name="parameters"></a><span data-ttu-id="46405-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="46405-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46405-110">*пкуери* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46405-110">*pQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46405-111">Интерфейс **вмплиб. ивмпкуери** , представляющий запрос.</span><span class="sxs-lookup"><span data-stu-id="46405-111">The **WMPLib.IWMPQuery** interface that represents the query.</span></span>

</dd> <dt>

<span data-ttu-id="46405-112">*бстрмедиатипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46405-112">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46405-113">**Строка System. String** , которая является типом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="46405-113">The **System.String** that is the media type.</span></span> <span data-ttu-id="46405-114">Должно содержать одно из следующих значений: "аудио", "видео", "Фото", "список воспроизведения" или "другое".</span><span class="sxs-lookup"><span data-stu-id="46405-114">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="46405-115">*бстрсортаттрибуте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46405-115">*bstrSortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46405-116">**Строка System. String** , которая является именем атрибута, используемого для сортировки.</span><span class="sxs-lookup"><span data-stu-id="46405-116">The **System.String** that is the attribute name used for sorting.</span></span> <span data-ttu-id="46405-117">Строка нулевой длины ("") означает, что сортировка не применяется.</span><span class="sxs-lookup"><span data-stu-id="46405-117">A zero-length string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="46405-118">*фсортасцендинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46405-118">*fSortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46405-119">Значение **System. Boolean** , указывающее, должен ли список воспроизведения быть отсортирован в возрастающем порядке.</span><span class="sxs-lookup"><span data-stu-id="46405-119">The **System.Boolean** value that indicates whether the playlist must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46405-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46405-120">Return value</span></span>

<span data-ttu-id="46405-121">Интерфейс **вмплиб. ивмпплайлист** для полученного списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="46405-121">A **WMPLib.IWMPPlaylist** interface for the retrieved playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="46405-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46405-122">Remarks</span></span>

<span data-ttu-id="46405-123">В составных запросах, использующих **ивмпкуери** , регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="46405-123">Compound queries using **IWMPQuery** are not case sensitive.</span></span>

<span data-ttu-id="46405-124">Если составной запрос, заданный параметром *пкуери* , содержит условие, построенное на атрибуте **mediaType** , это условие игнорируется.</span><span class="sxs-lookup"><span data-stu-id="46405-124">When the compound query specified by the *pQuery* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="46405-125">Значение параметра *бстрмедиатипе* всегда используется.</span><span class="sxs-lookup"><span data-stu-id="46405-125">The value for the *bstrMediaType* parameter is always used.</span></span> <span data-ttu-id="46405-126">Например, если составной запрос содержит условие «MediaType равно Audio», а значение параметра *бстрмедиатипе* — «Video», то итоговый список будет содержать только элементы видео.</span><span class="sxs-lookup"><span data-stu-id="46405-126">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *bstrMediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="46405-127">Требования</span><span class="sxs-lookup"><span data-stu-id="46405-127">Requirements</span></span>



| <span data-ttu-id="46405-128">Требование</span><span class="sxs-lookup"><span data-stu-id="46405-128">Requirement</span></span> | <span data-ttu-id="46405-129">Значение</span><span class="sxs-lookup"><span data-stu-id="46405-129">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46405-130">Версия</span><span class="sxs-lookup"><span data-stu-id="46405-130">Version</span></span><br/>   | <span data-ttu-id="46405-131">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="46405-131">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="46405-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="46405-132">Namespace</span></span><br/> | <span data-ttu-id="46405-133">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="46405-133">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="46405-134">Сборка</span><span class="sxs-lookup"><span data-stu-id="46405-134">Assembly</span></span><br/>  | <dl> <span data-ttu-id="46405-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="46405-135"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46405-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46405-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46405-137">**Интерфейс IWMPMediaCollection2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="46405-137">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="46405-138">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="46405-138">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="46405-139">**Интерфейс Ивмпкуери (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="46405-139">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="46405-140">**Атрибут MediaType**</span><span class="sxs-lookup"><span data-stu-id="46405-140">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> </dl>

 

 





