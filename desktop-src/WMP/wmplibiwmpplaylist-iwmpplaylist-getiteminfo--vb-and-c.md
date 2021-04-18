---
title: Ивмпплайлист getItemInfo, метод
description: Метод getItemInfo возвращает значение атрибута списка воспроизведения, указанного по имени.
ms.assetid: 62e882d6-66bb-450c-9700-b99d30dd42fa
keywords:
- getItemInfo метод Windows Media Player
- getItemInfo метод проигрывателя Windows Media Player, интерфейс Ивмпплайлист
- Интерфейс Ивмпплайлист Windows Media Player, метод getItemInfo
topic_type:
- apiref
api_name:
- IWMPPlaylist.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced433b13f5af2d1df8c12dba023b7fbb55c5f7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708401"
---
# <a name="iwmpplaylistgetiteminfo-method"></a><span data-ttu-id="135eb-106">Метод Ивмпплайлист:: getItemInfo</span><span class="sxs-lookup"><span data-stu-id="135eb-106">IWMPPlaylist::getItemInfo method</span></span>

<span data-ttu-id="135eb-107">Метод **getItemInfo** возвращает значение атрибута списка воспроизведения, указанного по имени.</span><span class="sxs-lookup"><span data-stu-id="135eb-107">The **getItemInfo** method returns the value of a playlist attribute specified by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="135eb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="135eb-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.String bstrName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrName As System.String _
) As System.String
Implements IWMPPlaylist.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="135eb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="135eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="135eb-110">*bstrName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="135eb-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="135eb-111">**Строка System. String** , которая является именем атрибута списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="135eb-111">A **System.String** that is the name of the playlist attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="135eb-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="135eb-112">Return value</span></span>

<span data-ttu-id="135eb-113">**Строка System. String** , которая является значением атрибута списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="135eb-113">A **System.String** that is the value of the playlist attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="135eb-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="135eb-114">Remarks</span></span>

<span data-ttu-id="135eb-115">Перед использованием этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="135eb-115">Before using this method, you must have read access to the library.</span></span> <span data-ttu-id="135eb-116">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="135eb-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="135eb-117">Пример кода, в котором используется это свойство, см. в свойстве [аттрибутекаунт](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) .</span><span class="sxs-lookup"><span data-stu-id="135eb-117">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="135eb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="135eb-118">Requirements</span></span>



| <span data-ttu-id="135eb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="135eb-119">Requirement</span></span> | <span data-ttu-id="135eb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="135eb-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="135eb-121">Версия</span><span class="sxs-lookup"><span data-stu-id="135eb-121">Version</span></span><br/>   | <span data-ttu-id="135eb-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="135eb-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="135eb-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="135eb-123">Namespace</span></span><br/> | <span data-ttu-id="135eb-124">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="135eb-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="135eb-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="135eb-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="135eb-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="135eb-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="135eb-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="135eb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="135eb-128">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="135eb-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="135eb-129">**Ивмпплайлист. Сетитеминфо (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="135eb-129">**IWMPPlaylist.setItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





