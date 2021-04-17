---
title: IWMPSettings2 Медиаакцессригхтс, свойство
description: Свойство Медиаакцессригхтс возвращает значение, указывающее разрешения, предоставленные в настоящее время для доступа к библиотеке.
ms.assetid: c4289a2c-e343-405d-9bf5-0e97f6617916
keywords:
- Проигрыватель Windows Media для свойства Медиаакцессригхтс
- Медиаакцессригхтс свойство проигрывателя Windows Media Player, интерфейс IWMPSettings2
- Интерфейс IWMPSettings2 Windows Media Player, свойство Медиаакцессригхтс
topic_type:
- apiref
api_name:
- IWMPSettings2.mediaAccessRights
- IWMPSettings2.get_mediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96cca06b9618767e7748b4b1308ed97860c7c80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685056"
---
# <a name="iwmpsettings2mediaaccessrights-property"></a><span data-ttu-id="ffdcb-106">Свойство IWMPSettings2:: Медиаакцессригхтс</span><span class="sxs-lookup"><span data-stu-id="ffdcb-106">IWMPSettings2::mediaAccessRights property</span></span>

<span data-ttu-id="ffdcb-107">Свойство **медиаакцессригхтс** возвращает значение, указывающее разрешения, предоставленные в настоящее время для доступа к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="ffdcb-107">The **mediaAccessRights** property gets a value indicating the permissions currently granted for library access.</span></span>

<span data-ttu-id="ffdcb-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ffdcb-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffdcb-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffdcb-109">Syntax</span></span>


```CSharp
public System.String mediaAccessRights {get;}
```


```VB

Public ReadOnly Property mediaAccessRights As System.String
```





## <a name="property-value"></a><span data-ttu-id="ffdcb-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ffdcb-110">Property value</span></span>

<span data-ttu-id="ffdcb-111">**Строка System. String** , которая является одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ffdcb-111">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="ffdcb-112">Значение</span><span class="sxs-lookup"><span data-stu-id="ffdcb-112">Value</span></span> | <span data-ttu-id="ffdcb-113">Описание</span><span class="sxs-lookup"><span data-stu-id="ffdcb-113">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="ffdcb-114">нет</span><span class="sxs-lookup"><span data-stu-id="ffdcb-114">none</span></span>  | <span data-ttu-id="ffdcb-115">Только права доступа к текущему элементу.</span><span class="sxs-lookup"><span data-stu-id="ffdcb-115">Current item access rights only.</span></span> |
| <span data-ttu-id="ffdcb-116">read</span><span class="sxs-lookup"><span data-stu-id="ffdcb-116">read</span></span>  | <span data-ttu-id="ffdcb-117">Права доступа только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ffdcb-117">Read access rights only.</span></span>         |
| <span data-ttu-id="ffdcb-118">переполненные</span><span class="sxs-lookup"><span data-stu-id="ffdcb-118">full</span></span>  | <span data-ttu-id="ffdcb-119">Права доступа для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ffdcb-119">Read/Write access rights.</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="ffdcb-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ffdcb-120">Remarks</span></span>

<span data-ttu-id="ffdcb-121">Веб-страница должна сначала запросить у пользователя разрешение на чтение информации из библиотеки или запись данных в нее.</span><span class="sxs-lookup"><span data-stu-id="ffdcb-121">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="ffdcb-122">Это означает, что определенные методы, свойства и события будут недоступны из кода, если соответствующие права доступа не были предоставлены.</span><span class="sxs-lookup"><span data-stu-id="ffdcb-122">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="ffdcb-123">Для получения прав доступа приложение вызывает **IWMPSettings2. Get \_ рекуестмедиаакцессригхтс**, передавая параметр, указывающий требуемый уровень прав доступа.</span><span class="sxs-lookup"><span data-stu-id="ffdcb-123">To obtain access rights, the application calls **IWMPSettings2.get\_requestMediaAccessRights**, passing a parameter that specifies the desired access rights level.</span></span>

<span data-ttu-id="ffdcb-124">Приложения, работающие на компьютере пользователя, всегда имеют права полного доступа.</span><span class="sxs-lookup"><span data-stu-id="ffdcb-124">Applications running on the user's computer always have full access rights.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffdcb-125">Требования</span><span class="sxs-lookup"><span data-stu-id="ffdcb-125">Requirements</span></span>



| <span data-ttu-id="ffdcb-126">Требование</span><span class="sxs-lookup"><span data-stu-id="ffdcb-126">Requirement</span></span> | <span data-ttu-id="ffdcb-127">Значение</span><span class="sxs-lookup"><span data-stu-id="ffdcb-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffdcb-128">Версия</span><span class="sxs-lookup"><span data-stu-id="ffdcb-128">Version</span></span><br/>   | <span data-ttu-id="ffdcb-129">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ffdcb-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ffdcb-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ffdcb-130">Namespace</span></span><br/> | <span data-ttu-id="ffdcb-131">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="ffdcb-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ffdcb-132">Сборка</span><span class="sxs-lookup"><span data-stu-id="ffdcb-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ffdcb-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ffdcb-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffdcb-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ffdcb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffdcb-135">**Интерфейс IWMPSettings2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="ffdcb-135">**IWMPSettings2 Interface (VB and C#)**</span></span>](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ffdcb-136">**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="ffdcb-136">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





