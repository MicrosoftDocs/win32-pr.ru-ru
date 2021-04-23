---
title: Ивмпплайлист Сетитеминфо, метод
description: Метод Сетитеминфо задает значение атрибута текущего списка воспроизведения.
ms.assetid: b3874298-8fbe-47a4-b696-cef0382aec7c
keywords:
- Сетитеминфо метод Windows Media Player
- Сетитеминфо метод проигрывателя Windows Media Player, интерфейс Ивмпплайлист
- Интерфейс Ивмпплайлист Windows Media Player, метод Сетитеминфо
topic_type:
- apiref
api_name:
- IWMPPlaylist.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce882d050f1ce7839fe3589fced3a87d9052fec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708368"
---
# <a name="iwmpplaylistsetiteminfo-method"></a><span data-ttu-id="7a0de-106">Метод Ивмпплайлист:: Сетитеминфо</span><span class="sxs-lookup"><span data-stu-id="7a0de-106">IWMPPlaylist::setItemInfo method</span></span>

<span data-ttu-id="7a0de-107">Метод **сетитеминфо** задает значение атрибута текущего списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="7a0de-107">The **setItemInfo** method sets the value of an attribute of the current playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a0de-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a0de-108">Syntax</span></span>


```CSharp
public void setItemInfo(
  System.String bstrName,
  System.String bstrValue
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrName As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPPlaylist.setItemInfo
```





## <a name="parameters"></a><span data-ttu-id="7a0de-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a0de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a0de-110">*bstrName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a0de-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a0de-111">**Строка System. String** , которая является именем атрибута.</span><span class="sxs-lookup"><span data-stu-id="7a0de-111">A **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="7a0de-112">*бстрвалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a0de-112">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a0de-113">**Строка System. String** , которая является значением атрибута.</span><span class="sxs-lookup"><span data-stu-id="7a0de-113">A **System.String** that is the attribute value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a0de-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a0de-114">Return value</span></span>

<span data-ttu-id="7a0de-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7a0de-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a0de-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a0de-116">Remarks</span></span>

<span data-ttu-id="7a0de-117">Перед вызовом этого метода необходимо иметь полный доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="7a0de-117">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="7a0de-118">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7a0de-118">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="7a0de-119">Пример кода, в котором используется это свойство, см. в свойстве [аттрибутекаунт](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) .</span><span class="sxs-lookup"><span data-stu-id="7a0de-119">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a0de-120">Требования</span><span class="sxs-lookup"><span data-stu-id="7a0de-120">Requirements</span></span>



| <span data-ttu-id="7a0de-121">Требование</span><span class="sxs-lookup"><span data-stu-id="7a0de-121">Requirement</span></span> | <span data-ttu-id="7a0de-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7a0de-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a0de-123">Версия</span><span class="sxs-lookup"><span data-stu-id="7a0de-123">Version</span></span><br/>   | <span data-ttu-id="7a0de-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7a0de-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7a0de-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7a0de-125">Namespace</span></span><br/> | <span data-ttu-id="7a0de-126">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="7a0de-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7a0de-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="7a0de-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7a0de-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7a0de-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a0de-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a0de-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a0de-130">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7a0de-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7a0de-131">**Ивмпплайлист. getItemInfo (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7a0de-131">**IWMPPlaylist.getItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7a0de-132">**IWMPSettings2. Медиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7a0de-132">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7a0de-133">**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7a0de-133">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





