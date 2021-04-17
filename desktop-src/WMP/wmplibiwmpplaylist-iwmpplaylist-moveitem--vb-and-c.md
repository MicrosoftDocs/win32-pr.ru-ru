---
title: Ивмпплайлист Мовеитем, метод
description: Метод Мовеитем изменяет расположение элемента мультимедиа в списке воспроизведения.
ms.assetid: e82c820f-4640-4289-88c1-79a92e520f00
keywords:
- Мовеитем метод Windows Media Player
- Мовеитем метод проигрывателя Windows Media Player, интерфейс Ивмпплайлист
- Интерфейс Ивмпплайлист Windows Media Player, метод Мовеитем
topic_type:
- apiref
api_name:
- IWMPPlaylist.moveItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c2d5be745fc3dcf799eb7203e607e493b284b4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708399"
---
# <a name="iwmpplaylistmoveitem-method"></a><span data-ttu-id="01da3-106">Метод Ивмпплайлист:: Мовеитем</span><span class="sxs-lookup"><span data-stu-id="01da3-106">IWMPPlaylist::moveItem method</span></span>

<span data-ttu-id="01da3-107">Метод **мовеитем** изменяет расположение элемента мультимедиа в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="01da3-107">The **moveItem** method changes the location of a media item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="01da3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01da3-108">Syntax</span></span>


```CSharp
public void moveItem(
  System.Int32 lIndexOld,
  System.Int32 lIndexNew
);
```


```VB

Public Sub moveItem( _
  ByVal lIndexOld As System.Int32, _
  ByVal lIndexNew As System.Int32 _
)
Implements IWMPPlaylist.moveItem
```





## <a name="parameters"></a><span data-ttu-id="01da3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="01da3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01da3-110">*линдексолд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01da3-110">*lIndexOld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01da3-111">Объект **System. Int32** , являющийся исходным индексом.</span><span class="sxs-lookup"><span data-stu-id="01da3-111">A **System.Int32** that is the original index.</span></span>

</dd> <dt>

<span data-ttu-id="01da3-112">*линдекснев* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01da3-112">*lIndexNew* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01da3-113">Объект **System. Int32** , который является новым индексом.</span><span class="sxs-lookup"><span data-stu-id="01da3-113">A **System.Int32** that is the new index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01da3-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01da3-114">Return value</span></span>

<span data-ttu-id="01da3-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="01da3-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="01da3-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01da3-116">Remarks</span></span>

<span data-ttu-id="01da3-117">Номера индексов всех элементов после вставленного элемента будут увеличены на единицу.</span><span class="sxs-lookup"><span data-stu-id="01da3-117">All items after the inserted item will have their index numbers increased by one.</span></span>

<span data-ttu-id="01da3-118">Перед вызовом этого метода необходимо иметь полный доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="01da3-118">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="01da3-119">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="01da3-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="01da3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="01da3-120">Requirements</span></span>



| <span data-ttu-id="01da3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="01da3-121">Requirement</span></span> | <span data-ttu-id="01da3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="01da3-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01da3-123">Версия</span><span class="sxs-lookup"><span data-stu-id="01da3-123">Version</span></span><br/>   | <span data-ttu-id="01da3-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="01da3-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="01da3-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="01da3-125">Namespace</span></span><br/> | <span data-ttu-id="01da3-126">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="01da3-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="01da3-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="01da3-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="01da3-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="01da3-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01da3-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01da3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01da3-130">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="01da3-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="01da3-131">**IWMPSettings2. Медиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="01da3-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="01da3-132">**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="01da3-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





