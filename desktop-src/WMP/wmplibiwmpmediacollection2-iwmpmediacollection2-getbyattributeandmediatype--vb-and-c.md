---
title: IWMPMediaCollection2 Жетбяттрибутеандмедиатипе, метод
description: Метод Жетбяттрибутеандмедиатипе возвращает интерфейс Ивмпплайлист, предоставляющий доступ к элементам мультимедиа с указанным атрибутом и типом мультимедиа.
ms.assetid: dce9cef4-1d12-4bee-a75d-42274556c5bc
keywords:
- Жетбяттрибутеандмедиатипе метод Windows Media Player
- Жетбяттрибутеандмедиатипе метод проигрывателя Windows Media Player, интерфейс IWMPMediaCollection2
- Интерфейс IWMPMediaCollection2 Windows Media Player, метод Жетбяттрибутеандмедиатипе
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getByAttributeAndMediaType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb1ee4e9421b4546cdc8ace6173dacab5034b905
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699193"
---
# <a name="iwmpmediacollection2getbyattributeandmediatype-method"></a><span data-ttu-id="4212a-106">Метод IWMPMediaCollection2:: Жетбяттрибутеандмедиатипе</span><span class="sxs-lookup"><span data-stu-id="4212a-106">IWMPMediaCollection2::getByAttributeAndMediaType method</span></span>

<span data-ttu-id="4212a-107">`getByAttributeAndMediaType`Метод возвращает интерфейс **ивмпплайлист** , предоставляющий доступ к элементам мультимедиа с указанным атрибутом и типом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4212a-107">The `getByAttributeAndMediaType` method returns an **IWMPPlaylist** interface that provides access to media items that have a specified attribute and media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="4212a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4212a-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAttributeAndMediaType(
  System.String bstrAttribute,
  System.String bstrValue,
  System.String bstrMediaType
);
```


```VB

Public Function getByAttributeAndMediaType( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getByAttributeAndMediaType
```





## <a name="parameters"></a><span data-ttu-id="4212a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4212a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4212a-110">*бстраттрибуте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4212a-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4212a-111">**Строка System. String** , которая является указанным атрибутом.</span><span class="sxs-lookup"><span data-stu-id="4212a-111">The **System.String** that is the specified attribute.</span></span>

</dd> <dt>

<span data-ttu-id="4212a-112">*бстрвалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4212a-112">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4212a-113">**Строка System. String** , которая является заданным значением для атрибута, указанного в *бстраттрибуте*.</span><span class="sxs-lookup"><span data-stu-id="4212a-113">The **System.String** that is the specified value for the attribute that is specified in *bstrAttribute*.</span></span>

</dd> <dt>

<span data-ttu-id="4212a-114">*бстрмедиатипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4212a-114">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4212a-115">**Строка System. String** , которая является указанным типом носителя.</span><span class="sxs-lookup"><span data-stu-id="4212a-115">The **System.String** that is the specified media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4212a-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4212a-116">Return value</span></span>

<span data-ttu-id="4212a-117">Интерфейс **вмплиб. ивмпплайлист** для полученного списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="4212a-117">A **WMPLib.IWMPPlaylist** interface for the retrieved playlist.</span></span>

## <a name="requirements"></a><span data-ttu-id="4212a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="4212a-118">Requirements</span></span>



| <span data-ttu-id="4212a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="4212a-119">Requirement</span></span> | <span data-ttu-id="4212a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="4212a-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4212a-121">Версия</span><span class="sxs-lookup"><span data-stu-id="4212a-121">Version</span></span><br/>   | <span data-ttu-id="4212a-122">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="4212a-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="4212a-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4212a-123">Namespace</span></span><br/> | <span data-ttu-id="4212a-124">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="4212a-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4212a-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="4212a-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4212a-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4212a-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4212a-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4212a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4212a-128">**Интерфейс IWMPMediaCollection2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4212a-128">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4212a-129">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="4212a-129">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





