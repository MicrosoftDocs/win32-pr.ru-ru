---
title: IWMPSettings2 Рекуестмедиаакцессригхтс, метод
description: Метод Рекуестмедиаакцессригхтс запрашивает указанный уровень доступа к библиотеке. | IWMPSettings2 Рекуестмедиаакцессригхтс, метод
ms.assetid: ea33852c-d1e0-45cf-8954-2a1e2fe51910
keywords:
- Рекуестмедиаакцессригхтс метод Windows Media Player
- Рекуестмедиаакцессригхтс метод проигрывателя Windows Media Player, интерфейс IWMPSettings2
- Интерфейс IWMPSettings2 Windows Media Player, метод Рекуестмедиаакцессригхтс
topic_type:
- apiref
api_name:
- IWMPSettings2.requestMediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c609afffc1d9b228d908d905e0eb1a6ef8741032
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688842"
---
# <a name="iwmpsettings2requestmediaaccessrights-method"></a><span data-ttu-id="d8f42-107">Метод IWMPSettings2:: Рекуестмедиаакцессригхтс</span><span class="sxs-lookup"><span data-stu-id="d8f42-107">IWMPSettings2::requestMediaAccessRights method</span></span>

<span data-ttu-id="d8f42-108">Метод **рекуестмедиаакцессригхтс** запрашивает указанный уровень доступа к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="d8f42-108">The **requestMediaAccessRights** method requests a specified level of access to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8f42-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8f42-109">Syntax</span></span>


```CSharp
public System.Boolean requestMediaAccessRights(
  System.String bstrDesiredAccess
);
```


```VB

Public Function requestMediaAccessRights( _
  ByVal bstrDesiredAccess As System.String _
) As System.Boolean
Implements IWMPSettings2.requestMediaAccessRights
```





## <a name="parameters"></a><span data-ttu-id="d8f42-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8f42-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8f42-111">*бстрдесиредакцесс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8f42-111">*bstrDesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8f42-112">**Строка System. String** , которая является одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="d8f42-112">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="d8f42-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d8f42-113">Value</span></span> | <span data-ttu-id="d8f42-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d8f42-114">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="d8f42-115">нет</span><span class="sxs-lookup"><span data-stu-id="d8f42-115">none</span></span>  | <span data-ttu-id="d8f42-116">Только права доступа к текущему элементу.</span><span class="sxs-lookup"><span data-stu-id="d8f42-116">Current item access rights only.</span></span> |
| <span data-ttu-id="d8f42-117">read</span><span class="sxs-lookup"><span data-stu-id="d8f42-117">read</span></span>  | <span data-ttu-id="d8f42-118">Права доступа только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d8f42-118">Read access rights only.</span></span>         |
| <span data-ttu-id="d8f42-119">переполненные</span><span class="sxs-lookup"><span data-stu-id="d8f42-119">full</span></span>  | <span data-ttu-id="d8f42-120">Права доступа для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d8f42-120">Read/Write access rights.</span></span>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8f42-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8f42-121">Return value</span></span>

<span data-ttu-id="d8f42-122">Значение **System. Boolean** , указывающее, были ли предоставлены запрошенные права доступа.</span><span class="sxs-lookup"><span data-stu-id="d8f42-122">A **System.Boolean** that indicates whether the requested access rights were granted.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8f42-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8f42-123">Remarks</span></span>

<span data-ttu-id="d8f42-124">Веб-страница должна сначала запросить у пользователя разрешение на чтение информации из библиотеки или запись данных в нее.</span><span class="sxs-lookup"><span data-stu-id="d8f42-124">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="d8f42-125">При вызове этого метода пользователю предлагается диалоговое окно, запрашивающее указанный уровень разрешений.</span><span class="sxs-lookup"><span data-stu-id="d8f42-125">Invoking this method prompts the user with a dialog box that requests the specified permission level.</span></span> <span data-ttu-id="d8f42-126">Это означает, что определенные методы, свойства и события будут недоступны из кода, если соответствующие права доступа не были предоставлены.</span><span class="sxs-lookup"><span data-stu-id="d8f42-126">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="d8f42-127">Текущий уровень прав доступа можно получить с помощью **IWMPSettings2. медиаакцессригхтс**.</span><span class="sxs-lookup"><span data-stu-id="d8f42-127">The current access rights level can be retrieved by using **IWMPSettings2.mediaAccessRights**.</span></span>

<span data-ttu-id="d8f42-128">Для использования этого метода приложения, работающие на компьютере пользователя, не требуются.</span><span class="sxs-lookup"><span data-stu-id="d8f42-128">Applications running on the user's computer are not required to use this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8f42-129">Требования</span><span class="sxs-lookup"><span data-stu-id="d8f42-129">Requirements</span></span>



| <span data-ttu-id="d8f42-130">Требование</span><span class="sxs-lookup"><span data-stu-id="d8f42-130">Requirement</span></span> | <span data-ttu-id="d8f42-131">Значение</span><span class="sxs-lookup"><span data-stu-id="d8f42-131">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8f42-132">Версия</span><span class="sxs-lookup"><span data-stu-id="d8f42-132">Version</span></span><br/>   | <span data-ttu-id="d8f42-133">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="d8f42-133">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d8f42-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d8f42-134">Namespace</span></span><br/> | <span data-ttu-id="d8f42-135">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="d8f42-135">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d8f42-136">Сборка</span><span class="sxs-lookup"><span data-stu-id="d8f42-136">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d8f42-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d8f42-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8f42-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8f42-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8f42-139">**Интерфейс IWMPSettings2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d8f42-139">**IWMPSettings2 Interface (VB and C#)**</span></span>](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d8f42-140">**IWMPSettings2. Медиаакцессригхтс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d8f42-140">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





